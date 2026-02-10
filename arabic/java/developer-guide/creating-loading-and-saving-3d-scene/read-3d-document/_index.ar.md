---
title: اقرأ مستند 3D
type: docs
weight: 30
url: /ar/java/read-3d-document/
description: Aspose.3D for Java API يدعم قراءة أنواع مختلفة من مستندات 3D.
---
##  **قائمة التنسيقات المدعومة بقيمة 3D (استيراد)**
Aspose.3D for Java API يدعم قراءة أنواع مختلفة من مستندات 3D. تساعد المنشئات المتوفرة لفئة `Scene` في القيام بذلك وتقبل سلسلة مسار ملف صالحة. تنسيقات الملفات المقروءة المدعومة هي كما يلي:

1. FBX 7.5 (ASCII ، ثنائي)
1. FBX 7.4 (ASCII ، ثنائي)
1. FBX 7.3 (ASCII ، ثنائي)
1. FBX 7.2 (ASCII ، ثنائي)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCI I ، inary inary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

تكتشف مُنشئات فئة المشهد تنسيق المستند 3D داخليًا.
##  **استيراد مستند 3D**
Aspose.3D for Java API يدعم استيراد أنواع مختلفة من مستندات 3D لأغراض التعديل والإضافة والمعالجة.
###  **قراءة مشهد 3D: عينات برمجة**
{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.open(MyDir + "document.fbx");
{{< /highlight >}}
##  **العمل مع خصائص 3D**
Aspose.3D API يتيح لك قراءة خصائص المشهد 3D باستخدام عقد الطفل للمشهد. توضح عينة الكود التالية استخدام هذه الميزة.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
String dataDir = RunExamples.getDataDir();
Scene scene = new Scene(dataDir+ "EmbeddedTexture.fbx");
Material material = scene.getRootNode().getChildNodes().get(0).getMaterial();
PropertyCollection props = material.getProperties();
//List all properties using for loop
for (Property prop:props)
{
    System.out.println("Name" + prop.getName() + " Value = " + prop.getValue());
}
//or using ordinal for loop
for (int i = 0; i < props.size(); i++)
{
    Property prop = props.get(i);
    System.out.println("Name" + prop.getName() + " Value = " + prop.getValue());
}
//Get property value by name
Object diffuse = (Vector3)props.get("Diffuse");
System.out.println(diffuse);
//modify property value by name
props.set("Diffuse", new Vector3(1, 0, 1));
//Get property instance by name
Property pdiffuse = props.findProperty("Diffuse");
System.out.println(pdiffuse);
//Since Property is also inherited from A3DObject
//It's possible to get the property of the property
System.out.println("Property flags = " + pdiffuse.getProperty("flags"));
//and some properties that only defined in FBX file:
System.out.println("Label = " + pdiffuse.getProperty("label"));
System.out.println("Type Name = " + pdiffuse.getProperty("typeName"));
//so traversal on property's property is possible
for (Property pp: pdiffuse.getProperties())
{
	System.out.println("Diffuse. " + pp.getName() + " = " + pp.getValue());
}

{{< /highlight >}}


