---
title: Декодирование и кодирование текстур с помощью SkiaSharp
type: docs
weight: 9
url: /ru/net/decode-and-encode-texture-using-skiasharp
description: Декодирование текстур из файлов изображений с помощью SkiaSharp
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики используют внешний кодировщик и декодеры изображений для загрузки текстур или сохранения текстур в различных форматах изображений.

{{% /alert %}}


##  **Используйте следующий код для определения текстурного кодека из SkiaSharp**

{{< highlight "csharp" >}}
﻿using System;
using System.Collections.Generic;
using System.IO;
using Aspose.ThreeD.Render;
using System.Runtime.InteropServices;
using SkiaSharp;

namespace Aspose.ThreeD
{

    /// <summary>
    /// Uses SkiaSharp for encoding/decoding textures for Aspose.3D textures.
    /// </summary>
    public class SkiaSharpCodec : ITextureCodec, ITextureDecoder
    {
        class SkiaSharpEncoder : ITextureEncoder
        {
            SKEncodedImageFormat format;
            public string FileExtension { get; }
            public SkiaSharpEncoder(string ext, SKEncodedImageFormat format)
            {
                FileExtension = ext;
                this.format = format;
            }

            public void Encode(TextureData texture, Stream stream)
            {
                var bmp = ToBitmap(texture);
                using (var tmp = bmp.Encode(format, 100).AsStream())
                {
                    tmp.CopyTo(stream);
                }
            }
        }
        /// <summary>
        /// Convert TextureData to Image
        /// </summary>
        /// <param name="td"></param>
        /// <returns></returns>
        public unsafe static SKBitmap ToBitmap(TextureData td)
        {
            var info = new SKImageInfo(td.Width, td.Height, SKColorType.Rgba8888);
            var ret = new SKBitmap(info);
            var pixels = new SKColor[td.Width * td.Height];
            var pout = 0;
            using (var map = td.MapPixels(PixelMapMode.ReadOnly, PixelFormat.A8R8G8B8))
            {
                var bytes = map.Data;
                for (int y = 0; y < map.Height; y++)
                {
                    int p = map.Stride * y;
                    for (int x = 0; x < map.Width; x++, p += 4)
                    {
                        byte a = bytes[p+0];
                        byte r = bytes[p+1];
                        byte g = bytes[p+2];
                        byte b = bytes[p+3];
                        pixels[pout++] = new SKColor(r, g, b, a);
                    }
                }
            }
            ret.Pixels = pixels;
            return ret;
        }
        /// <summary>
        /// Convert Image to TextureData
        /// </summary>
        /// <param name="img"></param>
        /// <param name="reverseY"></param>
        /// <returns></returns>
        public unsafe static TextureData ToTextureData(SKBitmap img, bool reverseY)
        {
            var ret = new TextureData(img.Width, img.Height, PixelFormat.A8R8G8B8);
            if (img.ColorType == SKColorType.Rgba8888)
                CopyTo(img, ret, reverseY);
            else
            {
                using (var tmp = new SKBitmap(img.Width, img.Height, SKColorType.Bgra8888, SKAlphaType.Opaque))
                {
                    using (var canvas = new SKCanvas(tmp))
                    {
                        canvas.DrawBitmap(img, SKPoint.Empty);
                    }
                    CopyTo(tmp, ret, reverseY);
                }
            }
            return ret;

        }
        private unsafe static void CopyTo(SKBitmap bitmap, TextureData td, bool reverseY)
        {
            var src = bitmap.GetPixels();
            using (var map = td.MapPixels(PixelMapMode.WriteOnly, PixelFormat.A8R8G8B8))
            {
                var stride = 4 * bitmap.Width;
                var rows = map.Height;
                for (int y = 0; y < rows; y++)
                {
                    var sRow = src + stride * y;
                    var dRow = reverseY ? (rows - 1 - y) * stride : y * stride;
                    Marshal.Copy(sRow, map.Data, dRow, stride);
                }
            }
        }

        /// <summary>
        /// Decode texture from stream, return null if failed to decode.
        /// </summary>
        /// <param name="stream">Texture data source stream</param>
        /// <param name="reverseY">Flip the texture</param>
        /// <returns>Decoded texture data or null if not supported.</returns>
        public unsafe TextureData Decode(Stream stream, bool reverseY)
        {
            using (var bmp = SKBitmap.Decode(stream))
            {
                return ToTextureData(bmp, reverseY);
            }
        }

        /// <summary>
        /// Gets supported texture decoders.
        /// </summary>
        /// <returns></returns>
        public ITextureDecoder[] GetDecoders()
        {
            return new ITextureDecoder[] { this };

        }

        /// <summary>
        /// Gets supported texture encoders. 
        /// </summary>
        /// <returns></returns>
        public ITextureEncoder[] GetEncoders()
        {
            List<ITextureEncoder> ret = new List<ITextureEncoder>();
            ret.Add(new SkiaSharpEncoder("bmp", SKEncodedImageFormat.Bmp));
            ret.Add(new SkiaSharpEncoder("dng", SKEncodedImageFormat.Dng));
            ret.Add(new SkiaSharpEncoder("webp", SKEncodedImageFormat.Webp));
            ret.Add(new SkiaSharpEncoder("avif", SKEncodedImageFormat.Avif));
            ret.Add(new SkiaSharpEncoder("heif", SKEncodedImageFormat.Heif));
            ret.Add(new SkiaSharpEncoder("png", SKEncodedImageFormat.Png));
            ret.Add(new SkiaSharpEncoder("jpg", SKEncodedImageFormat.Jpeg));
            ret.Add(new SkiaSharpEncoder("jpeg", SKEncodedImageFormat.Jpeg));
            ret.Add(new SkiaSharpEncoder("astc", SKEncodedImageFormat.Astc));
            ret.Add(new SkiaSharpEncoder("ktx", SKEncodedImageFormat.Ktx));
            ret.Add(new SkiaSharpEncoder("gif", SKEncodedImageFormat.Gif));
            ret.Add(new SkiaSharpEncoder("ico", SKEncodedImageFormat.Ico));
            ret.Add(new SkiaSharpEncoder("pkm", SKEncodedImageFormat.Pkm));
            ret.Add(new SkiaSharpEncoder("wbmp", SKEncodedImageFormat.Wbmp));
            return ret.ToArray();
        }


    }

}

{{< /highlight >}}



##  **Зарегистрируйте в Aspose.3D**

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.SkiaSharpCodec());
{{< /highlight >}}


Когда этот кодек зарегистрирован, все поддерживаемые SkiaSharp форматы изображений могут быть использованы в TextureData.Save.





