---
title: Декодирование и кодирование текстуры с помощью System.Drawing
type: docs
weight: 7
url: /ru/net/decode-and-encode-texture-using-system-drawing
description: Декодирование текстуры из файлов изображений с помощью System.Drawing
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики используют внешний кодировщик и декодеры изображений для загрузки текстур или сохранения текстур в различных форматах изображений.

{{% /alert %}}

##  **Реализовать текстурный кодек с помощью System.Drawing**

Используйте следующий класс для определения кодировщиков текстур и декодеров текстур:

{{< highlight "csharp" >}}
﻿using System;
using System.Collections.Generic;
using System.IO;
using System.Drawing;
using System.Drawing.Imaging;
using Aspose.ThreeD.Render;
using System.Runtime.InteropServices;

namespace Aspose.ThreeD
{
    /// <summary>
    /// Uses System.Drawing for encoding/decoding textures for Aspose.3D textures.
    /// </summary>
    public class GdiPlusCodec : ITextureCodec, ITextureDecoder
    {
        class GdiPlusEncoder : ITextureEncoder
        {
            public string FileExtension { get; }
            private ImageCodecInfo encoder;
            public GdiPlusEncoder(ImageCodecInfo encoder, string ext)
            {
                this.encoder = encoder;
                FileExtension = ext;
            }

            public void Encode(TextureData texture, Stream stream)
            {
                var bmp = ToBitmap(texture);
                bmp.Save(stream, encoder, null);
            }
        }
        /// <summary>
        /// Convert <see cref="TextureData"/> to <see cref="Bitmap"/>
        /// </summary>
        /// <param name="td"></param>
        /// <returns></returns>
        public static Bitmap ToBitmap(TextureData td)
        {
            using (var map = td.MapPixels(PixelMapMode.ReadOnly, Render.PixelFormat.A8R8G8B8))
            {
                var ret = new Bitmap(td.Width, td.Height, System.Drawing.Imaging.PixelFormat.Format32bppArgb);
                var bits = ret.LockBits(new Rectangle(0, 0, td.Width, td.Height), ImageLockMode.WriteOnly, System.Drawing.Imaging.PixelFormat.Format32bppArgb);
                for (int y = 0; y < td.Height; y++)
                {
                    var srcOffset = y * map.Stride;
                    var destination = bits.Scan0 + y * bits.Stride;
                    Marshal.Copy(map.Data, srcOffset, destination, map.Stride);
                }
                ret.UnlockBits(bits);
                return ret;
            }
        }

        /// <summary>
        /// Convert <see cref="Bitmap"/> to <see cref="TextureData"/>
        /// </summary>
        /// <param name="img"></param>
        /// <param name="reverseY"></param>
        /// <returns></returns>
        public static TextureData ToTextureData(Bitmap img, bool reverseY)
        {
            var ret = new TextureData(img.Width, img.Height, Render.PixelFormat.A8R8G8B8);
            var bits = img.LockBits(new Rectangle(0, 0, img.Width, img.Height), ImageLockMode.ReadWrite, System.Drawing.Imaging.PixelFormat.Format32bppArgb);
            using (var map = ret.MapPixels(PixelMapMode.WriteOnly))
            {
                for (int y = 0; y < map.Height; y++)
                {
                    IntPtr srcPtr = bits.Scan0;
                    if(reverseY)
                        srcPtr += (map.Height - y - 1) * bits.Stride;
                    else
                        srcPtr += y * bits.Stride;
                    var dstOffset = y * map.Stride;
                    Marshal.Copy(srcPtr, map.Data, dstOffset, map.Stride);
                }
            }
            img.UnlockBits(bits);
            return ret;
        }
        /// <summary>
        /// Decode texture from stream, return null if failed to decode.
        /// </summary>
        /// <param name="stream">Texture data source stream</param>
        /// <param name="reverseY">Flip the texture</param>
        /// <returns>Decoded texture data or null if not supported.</returns>
        public TextureData Decode(Stream stream, bool reverseY)
        {
            using (var img = (Bitmap)Image.FromStream(stream))
            {
                var ret = ToTextureData(img, reverseY);
                return ret;
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
            foreach (var encoder in ImageCodecInfo.GetImageEncoders())
            {
                if (encoder.FilenameExtension == null)
                    continue;
                var exts = encoder.FilenameExtension.Split(';');
                foreach(var fileExt in exts)
                {
                    var ext = fileExt;
                    int p = ext.IndexOf('.');
                    if (p != -1)
                        ext = ext.Substring(p + 1);
                    ret.Add(new GdiPlusEncoder(encoder, ext.ToLowerInvariant()));
                }
            }
            return ret.ToArray();
        }
    }
}

{{< /highlight >}}


##  **Зарегистрируйте в Aspose.3D**

Теперь давайте зарегистрируем его в Aspsoe.3D:

{{< highlight "csharp" >}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.GdiPlusCodec());
{{< /highlight >}}


Когда этот кодек зарегистрирован, все форматы изображений, поддерживаемые System.Drawing, могут быть использованы в TextureData.Save.

