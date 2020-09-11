---
title: Aspose.3D for .NET 17.01 Release Notes
type: docs
weight: 120
url: /net/aspose-3d-for-net-17-01-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for [Aspose.3D for .NET 17.1.0](https://www.nuget.org/packages/Aspose.3D/17.1.0).

{{% /alert %}} 
## **Other Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|THREEDNET-227|Add support of importing the PLY models.|New feature|
### **Public API and Backwards Incompatible Changes**
See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).
#### **Adds a PLY format entry in the Aspose.ThreeD.FileFormat Class**
We have added a PLY (Polygon File Format) entry for the importing purposes.
#### **Adds Aspose.ThreeD.Formats.PLY.PlyLoadOptions Class**
It specifies load settings to load a PLY model into the Aspose.3D API. This load option class has only a FlipCoordinateSystem property, which also exists in load options classes of other file formats.
#### **Adds Aspose.ThreeD.GlobalTransform Class**
The GlobalTransform class provides exactly the same interface like Transform but all its properties are read-only. It is useful for the global transform purposes.
#### **Adds a GlobalTransform property to Aspose.ThreeD.Node Class**
It allows to access the node's global transform. This is useful to transform the scene into the user's custom file format.
#### **Adds Polygons property to Aspose.ThreeD.Entities.Mesh Class**
It allows to get all polygons inside the mesh, each polygon is an array of polygon vertex index. Before this property, we have to use foreach syntax to enumerate each polygon which is inefficient.
#### **Removes CreateStream member from Aspose.ThreeD.Formats.IOConfig Class**
This was marked as obsolete in version 16.11.0, the new interface FileSystem was introduced in version 16.11.0 which provides more extensibilities.
### **Usage Examples**
Please check the list of help topics added in the Aspose.3D Wiki docs:

1. [Create and Read an Existing 3D Scene](http://docs.asposeptyltd.com/docs/display/3dnet/Create+and+Read+an+Existing+3D+Scene)
1. [Specify the Load Options of PLY Models](http://docs.asposeptyltd.com/docs/display/3dnet/Specify+3D+File+Load+Options#Specify3DFileLoadOptions-UseofthePlyLoadOptions)
1. [Save 3D Meshes in Custom Binary Format](http://docs.asposeptyltd.com/docs/display/3dnet/Save+3D+Meshes+in+Custom+Binary+Format)
