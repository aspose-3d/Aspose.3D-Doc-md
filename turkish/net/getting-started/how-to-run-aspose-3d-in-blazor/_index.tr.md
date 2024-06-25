---
title: Blazor Aspose.3D nasıl çalıştırılır
type: docs
weight: 138
url: /tr/net/how-to-run-aspose-3d-in-blazor/
description: Learn how to How to Run Aspose.3D in Blazor.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Overview

Blazor is a web application framework developed by Microsoft that allows client-side web applications to be written using C# and .NET. Blazor is distinguished by its use of WebAssembly technology, which enables applications running in the browser to use high-performance native code. Blazor uses a componentized architecture, allowing developers to divide the UI into independent components, thereby achieving code reusability and maintainability. Blazor supports cross-platform development and can run on a variety of modern browsers and devices, including desktop, mobile, and embedded devices.

In general, Blazor provides a modern way to build web applications, enabling developers to build high-performance, interactive, and maintainable web applications using C# and .NET technologies in the browser.

## İlk blazor uygulaması Aspose.3D

Bu örnekte, basit bir blazor sunucu uygulaması oluşturduk, bir 3d dosya oluşturduk ve dosya içeriğinin ekran görüntüsünü aldık ve bir web sayfasında görüntüledik. Proje oluşturma işlemi sırasında, blazor uygulamasının docker'da oluşturulabilmesi ve çalıştırılabilmesi için "docker" seçeneğini kontrol etmek gibi ihtiyaçlarımıza göre yapılandırabiliriz.

### İlk blazor uygulamasını oluşturun

Let's use the VS2022 tool as an example to create the first blazor application with Aspose.3D, follow the steps below:
1. İlgili proje şablonunu seçmek için blazer anahtar kelimesini kullanarak dosya-> yeni-> proje ve filtreyi seçin.
<br>
<img src="1.png" width=80% />
1. Proje adını "blazortest" e ayarlayın ve yolu seçin.
<br>
<img src="2.png" width=80% />
1. Projede kullanılan kütüphaneleri ve diğer seçenekleri yapılandırın. Son olarak, ilk blazer projenizi oluşturmak için "oluştur" düğmesine tıklayın.
<br>
<img src="3.png" width=80% />
1. Projeye girdikten sonra, projenin altındaki "bağımlılıkları" tıklayın ve NuGet paketlerini yönetin... Aspose.3D kütüphanesini eklemek için.
<br>
<img src="4.png" width=80% />
1. Filtrelemek için anahtar kelimeleri girin ve en son Aspose.3D kütüphanesini yükleyin.
<br>
<img src="5.png" width=80% />
1. Gerekli kütüphaneyi düzenlemek ve içe aktarmak için "index. razor" dosyasını çift tıklayın. Bazı veriler ve resimler ekleyin.
<br>
<img src="5.png" width=80% />
1. Projeyi derleyin ve çalıştırın ve aşağıdaki sonuçları alacaksınız.
<br>
<img src="7.png" width=80% />

### İlk blazor uygulamasında örnek kod

Aşağıdaki örnek kod dizine dahildir. tıraş bıçağı dosyası:
```
@page "/"
@using Aspose.ThreeD;
@using Aspose.ThreeD.Entities;
@using Aspose.ThreeD.Utilities;

<PageTitle>Index</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<SurveyPrompt Title="How is Blazor working for you?" />

<img src="@imageUrl" />

@code
{
    private string imageUrl="https://docs.aspose.com/3d/net/working-with-cylinder/working-with-cylinder_1.png";

    public Index()
    {
        CreateFile();
    }

    private void CreateFile()
    {
        // Create a scene
        Scene scene = new Scene();

        // Initialize cylinder
        var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

        // Set OffsetTop
        cylinder1.OffsetTop = new Vector3(5, 3, 0);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

        // Intialze second cylinder without customized OffsetTop
        var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder2);

        // Save
        scene.Save("CustomizedOffsetTopCylinder.obj");
    }
}

```