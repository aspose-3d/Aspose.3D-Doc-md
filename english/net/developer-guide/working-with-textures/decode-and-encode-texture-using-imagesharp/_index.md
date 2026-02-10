---
title: Decode and encode texture using ImageSharp
type: docs
weight: 11
url: /net/decode-and-encode-texture-using-imagesharp
description: Decode texture from image files using ImageSharp
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers use external image encoder and decoders to load textures or save textures into different image formats.

{{% /alert %}}

## **Implement a texture codec using ImageSharp**

Use the following class to define texture encoders and texture decoder:

{{< highlight "csharp" >}}
﻿using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.ThreeD.Utilities;
using Aspose.ThreeD.Render;
using SixLabors.ImageSharp;
using SixLabors.ImageSharp.PixelFormats;
using System.Runtime.InteropServices;
using SixLabors.ImageSharp.Formats;

namespace Aspose.ThreeD
{

    /// <summary>
    /// Uses ImageSharp for encoding/decoding textures for Aspose.3D textures.
    /// </summary>
    public class ImageSharpCodec : ITextureCodec, ITextureDecoder
    {
        class Encoder<T> : ITextureEncoder where T:IImageEncoder, new()
        {
            public string FileExtension { get; }
            public Encoder(string ext)
            {
                FileExtension = ext;
            }

            public void Encode(TextureData texture, Stream stream)
            {
                var bmp = ToBitmap(texture);
                var encoder = new T();
                bmp.Save(stream, encoder);
            }
        }
        /// <summary>
        /// Convert TextureData to Image
        /// </summary>
        /// <param name="td"></param>
        /// <returns></returns>
        public unsafe static Image<Bgra32> ToBitmap(TextureData td)
        {
            using(var map = td.MapPixels(PixelMapMode.ReadOnly, PixelFormat.A8R8G8B8))
            {
                var ret = new Image<Bgra32>(td.Width, td.Height);
                ret.ProcessPixelRows(accessor =>
                {
                    fixed (byte* p = map.Data)
                    {
                        for (int y = 0; y < ret.Height; y++)
                        {
                            var offset = y * map.Stride;
                            var src = new Span<Bgra32>(p + offset, map.Stride);
                            var dst = accessor.GetRowSpan(y);
                            src.CopyTo(dst);
                        }
                    }
                });
                return ret;
            }
        }
        /// <summary>
        /// Convert Image to TextureData
        /// </summary>
        /// <param name="img"></param>
        /// <param name="reverseY"></param>
        /// <returns></returns>
        public unsafe static TextureData ToTextureData(Image<Bgra32> img, bool reverseY)
        {
            var ret = new TextureData(img.Width, img.Height, PixelFormat.A8R8G8B8);
            using (var map = ret.MapPixels(PixelMapMode.WriteOnly))
            {
                img.ProcessPixelRows(accessor =>
                {
                    fixed (byte* src = map.Data)
                    {
                        for (int y = 0; y < img.Height; y++)
                        {
                            var offset = 0;
                            if (reverseY)
                                offset = (map.Height - y - 1) * map.Stride;
                            else
                                offset = y * map.Stride;
                            var dst = new Span<Bgra32>(src + offset, map.Stride);
                            var row = accessor.GetRowSpan(y);
                            row.CopyTo(dst);
                        }
                    }
                });
            }
            return ret;

        }

        /// <summary>
        /// Decode texture from stream, return null if failed to decode.
        /// </summary>
        /// <param name="stream">Texture data source stream</param>
        /// <param name="reverseY">Flip the texture</param>
        /// <returns>Decoded texture data or null if not supported.</returns>
        public unsafe TextureData Decode(Stream stream, bool reverseY)
        {
            using (var img = Image.Load<Bgra32>(stream))
            {
                return ToTextureData(img, reverseY);
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
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Bmp.BmpEncoder>("bmp"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Png.PngEncoder>("png"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Jpeg.JpegEncoder>("jpg"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Jpeg.JpegEncoder>("jpeg"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Pbm.PbmEncoder>("pbm"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Gif.GifEncoder>("gif"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Tga.TgaEncoder>("tga"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Tiff.TiffEncoder>("tif"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Tiff.TiffEncoder>("tiff"));
            ret.Add(new Encoder<SixLabors.ImageSharp.Formats.Webp.WebpEncoder>("webp"));
            return ret.ToArray();
        }


    }

}

{{< /highlight >}}


## **Register it into Aspose.3D**

Now let's register it into Aspsoe.3D:

{{<highlight csharp>}}
    Aspose.ThreeD.Render.TextureCodec.RegisterCodec(new Aspose.ThreeD.ImageSharpCodec());
{{</highlight>}}


When this codec has been registered, all ImageSharp supported image formats can be used in TextureData.Save.

