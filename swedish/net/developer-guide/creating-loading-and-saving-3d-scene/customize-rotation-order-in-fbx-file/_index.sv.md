---
title: Anpassa roterande ordning i FBX filen
type: docs
weight: 10
url: /sv/net/customize-rotation-order-in-fbx-file
description: Genom att använda Aspose.3D for .NET, kan utvecklare definiera de infödda egenskaperna FBX som RotationOrder.
---
{{% alert color="primary" %}}

Använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/), Ibland kräver utvecklare finkontroll över formatspecifika funktioner, såsom att ändra `RotationOrder` i exportören FBX. Även om det kanske inte finns en offentlig API som direkt exponerar denna funktionalitet, Aspose. 3D for .NET tillhandahåller sätt att uppnå sådana anpassningar genom dess flexibla arkitektur.
{{% /alert %}}



Så här kan du hantera det här i Aspose.3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

I detta exempel:

1. Skapa en scen från en RVM-fil.
1. Besök alla nod i scenen.
1. Ange egen egenskap: Metoden SetProperty används för att ställa in egenskapen `RotationOrder`. visa hur interna mekanismer kan utnyttjas för att kontrollera formatspecifika funktioner som inte direkt exponeras av allmänheten API.
1. Spara scenen: Scenen sparas med den anpassade `RotationOrder`.

Genom att använda sådan teknik, Aspose. 3D låter utvecklare finjustera och styra specifika funktioner i 3D-format, se till att detaljerade och exakta krav uppfylls i olika 3D-program.