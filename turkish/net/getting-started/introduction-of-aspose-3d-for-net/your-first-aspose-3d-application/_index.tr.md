---
title: İlk Aspose.3D uygulamanız
type: docs
weight: 30
url: /tr/net/your-first-aspose-3d-application/
description: Create, edit and save your first 3d file in any supported formats using Aspose.3D for .NET to experience its simplicity and power in C#.
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---
{{% alert color="primary" %}}

This tutorial explains how to create your first application using Aspose.3D's simple API. This simple application creates a 3d file in a specified 3D scene.

{{% /alert %}}

##  **Uygulama nasıl oluşturulur**

Aşağıdaki adımlar, uygulamayı Aspose kullanarak oluşturur. 3D API:

1. Create an instance of the [Scene](https://reference.aspose.com/3d/net/aspose.threed/scene/) class.
1. Eğer bir lisansınız varsa, o zaman [Uygula](/3d/tr/net/licensing/).
Değerlendirme sürümünü kullanıyorsanız, lisans ile ilgili kod satırlarını atlayın.
1. Yeni bir 3D dosyası oluşturun veya mevcut bir 3D dosyasını açın.
1. Access the scene contents in the 3D file.
1. Değiştirilmiş 3D dosyasını oluşturun.

Yukarıdaki adımların uygulanması aşağıdaki örneklerde gösterilmiştir.

###  **Yeni bir sahne belgesi nasıl oluşturulur**

Aşağıdaki örnek, sıfırdan yeni bir 3D sahne dosyası oluşturur. İlk olarak, 3D sahne oluşturun ve ardından dosyayı FBX formatında kaydedin.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

###  **Mevcut bir dosya nasıl açılır**

The following example opens an existing 3D template file named "document.fbx" and then saves the 3D scene or document to a stream in various supported 3D formats.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
