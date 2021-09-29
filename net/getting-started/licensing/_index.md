---
title: Licensing
type: docs
weight: 60
url: /net/licensing/
---

## **Evaluation Version Limitations**
A free evaluation version of Aspose.3D for .NET can be downloaded from the downloads section of Aspose's website at: [Download Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
### **Limitation**
The evaluation version provides all the features except the following:

- Users can only open/import maximum of 50 3D documents to a Scene.
- Each node can have no more than 5 child nodes.
- Each node can have no more than 2 attached entities.
- Each geometry can have no more than 2 attached vertex elements.
- Each node can have no more than 1 material.
- Users can only save a maximum of 50 3D documents to a Scene.
- Users will also see an evaluation watermark in the rendered images and all other output files.

{{% alert color="primary" %}} 
If you're using Aspose.3D without a proper license, there could trigger an **Aspose.ThreeD.TrialException** when the usage reached the unlicensed restrictions, you can turn the exception off by:

* [Buy a full featured license](https://purchase.aspose.com/buy).
* Request a 30 days temporary license, please refer to [How to get a Temporary License?](https://purchase.aspose.com/temporary-license) For more information.
.
* Set **Aspose.ThreeD.TrialException.SuppressTrialException** to true, the  TrialException will not be raised during the Open/Save call on Scene, but the above restrictions will not be lifted.
* Manually use a try/catch block on Scene.Open/Save, this exception is just a notification, ignore it will not affect the scene loading/saving.

{{% /alert %}} 

## **Apply License using File or Stream Object**
The license can be loaded from a [file](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) or [stream object](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET will try to find the license in the following locations:

1. Explicit path.
1. The folder that contains Aspose.3D.dll.
1. The folder that contains the assembly that called Aspose.3D.dll.
1. The folder that contains the entry assembly (your .exe).
1. An embedded resource in the assembly that called Aspose.3D.dll.

The easiest way to set a license is to put the license file in the same folder as the Aspose.3D.dll file and specify the file name, without a path, as shown in the example below.

{{% alert color="primary" %}} 

If you are using any other Aspose for .NET API along with Aspose.3D for .NET, please specify the namespace for the license like Aspose.ThreeD.License.

{{% /alert %}} 
### **Loading a License from File**
The easiest way to apply a license is to put the license file in the same folder as the Aspose.3D.dll file and specify just the file name without a path.

{{% alert color="primary" %}} 

When you call the SetLicense method, the license name that you pass should be that of the license file. For example, if you change the license file name to "Aspose.3D.lic.xml" pass that filename to threeD.SetLicense(…) method.

{{% /alert %}} 

**Example:**

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**Loading a License  from a Stream Object**
The following example shows how to load a license from a stream.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **Apply License using Embedded Resource**
One way of applying a license is to set it [using a file or stream object](). Another neat way of packaging the license with your application and making sure it will not be lost is to include it as an embedded resource into one of the assemblies that calls the component's DLL (included in Aspose.3D).

To include the license file as an embedded resource:

1. In Visual Studio .NET, include the license (.lic) file into the project by selecting **File**, then **Add Existing Item** and finally **Add**.
1. Select the file in the Solution Explorer.
1. Set the **Build Action** to **Embedded Resource** in the Properties window.
1. To access the license embedded in the assembly (as an embedded resource), just add the license file as an embedded resource to the project and pass the name of the license file to the SetLicense method. The License class automatically finds the license file in the embedded resources. There's no need to call the GetExecutingAssembly and GetManifestResourceStream methods of the System.Reflection.Assembly class in the Microsoft .NET Framework.

The following code snippet is used to set the license.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **Apply Metered License**
Aspose.3D for .NET API allows developers to apply metered license. It is a new licensing mechanism. The new licensing mechanism will be used along with existing licensing method. Those customers who want to be billed based on the usage of the API features can use the metered licensing. For more details, please refer to [Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered) section.

A new class [Metered](https://apireference.aspose.com/3d/net/aspose.threed/metered) has been added to apply metered key. This code example demonstrates how to set metered public and private keys:

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
