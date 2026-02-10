---
title: Convert Msh إلى Triangle esh sh و ririmitive Shape إلى Mesh
type: docs
weight: 30
url: /ar/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: يسمح Aspose.3D for Python via .NET API للمطورين بتحويل أي كائن شبكي إلى شبكة مثلثة مع تخطيط ذاكرة مخصص للقمة. يتم تعريف تخطيط الذاكرة المخصصة للقمة باستخدام البنية أو ديناميكيا بواسطة فئة vertexdication في أمثلة التعليمات البرمجية.
---
##  **Convert esh sh إلى Triangle esh sh مع Custom Memory Layout من erertex**
يسمح [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API للمطورين بتحويل أي كائن شبكي إلى شبكة مثلثة مع تخطيط ذاكرة مخصص للقمة. يتم تعريف تخطيط الذاكرة المخصص للقمة باستخدام البنية أو ديناميكيا بواسطة فئة [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration) في أمثلة التعليمات البرمجية.

{{% alert color="primary" %}}

يخلق موضوع المساعدة هذا شبكات من الصندوق والكرة للحفاظ على الرمز شامل وقصير. يمكن للمطورين إنشاء شبكة يدويًا كما روى في موضوع المساعدة هذا: [إنشاء شبكة مكعبة 3D](/3d/ar/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

أمثلة ese hese تظهر كيفية:

- [Convert ere phere إلى ririangle esh sh مع تخطيط ذاكرة مخصص من القشرة (محددة في شاحنة S)](/3d/ar/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert ox ox إلى ririangle esh sh مع تخطيط ذاكرة مخصص من القشرة (محددة من قبل فئة eclaration erertexD)](/3d/ar/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convert Msh**
قد تتحول شبكة إيفلين Dإلى شبكة مثلث لأن أي هيكل معقد (سطح) يمكن أن يمثل حفنة من المثلثات. Tانه مثلث هو الهندسة الأكثر ذرية. Hhus يتم استخدامه كقاعدة لأي شيء تقريبا.
###  **Ccccess erertices من ririangle esh sh**
Dإيفليرز يمكن الوصول إلى نقاط الاتصال ، vertices الفعلية ، vertices قبل دمج والبايت الإجمالية من vertices في الذاكرة.

مثال elelow يحول phere إلى شبكة مثلث مع تخطيط ذاكرة مخصص.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




مثال elelow يحول الثور Bإلى شبكة مثلث مع تخطيط ذاكرة مخصص.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
##  **Convert 'إعادة صياغة' إلى 'إعادة صياغة'**
باستخدام Aspose.3D for Python via .NET ، يمكن للمطورين تحويل أي كائن بدائي إلى شبكة. تشمل الأوليات العديد من الأشياء الأساسية والأكثر استخدامًا مثل الصندوق والكرة والطائرة والأسطوانة والطوف.

{{% alert color="primary" %}}

يمكن تحويل أي فئة تقوم بتطبيق واجهة قابلة للتحويل إلى شبكة أثناء التصدير إلى أي تنسيق ملف 3D.

{{% /alert %}}
###  **Convert 'الفيرومونات' إلى 'M'**
A المجال هو كائن هندسي مستدير تماما في الفضاء ثلاثي الأبعاد التي تظهر في كل مكان من الكرات الرياضية إلى الكواكب في الفضاء. استخدام et et priphere بدائية لإنشاء شبكة.
Tانه رمز المثال أدناه تحويل ere phere إلى شبكة.

{{< highlight "python" >}}
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Sphere class
convertible = Sphere()
#  Convert a Sphere to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert 'oxox' إلى' M'**
يصف ox ox ox مجموعة متنوعة من الحاويات والأوعية للاستخدام الدائم كتخزين ، أو للاستخدام المؤقت ، في كثير من الأحيان لنقل المحتويات. استخدام et et priox بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل الثور Bإلى شبكة.

{{< highlight "python" >}}
from aspose.threed.entities import Box

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Box class
convertible = Box()
#  Convert a Box to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert 'Plane 'إلى' M'**
طائرة A تمتد بلا حدود دون سمك. An مثال على طائرة هو طائرة التنسيق. تستخدم ets ets حارة Pبدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل حارة Pإلى شبكة.

{{< highlight "python" >}}
from aspose.threed.entities import Plane

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Plane class
convertible = Plane()
#  Convert a Plane to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert 'Cylinder' إلى' M'**
اسطوانة A هي واحدة من الأشكال الهندسية المنحنية الأساسية ، والسطح الذي شكلتها النقاط على مسافة ثابتة من خط مستقيم معين ، محور الاسطوانة. It يمكن استخدامها في العديد من الأماكن ، على سبيل المثال كعمود أمام المنزل أو كسيارة driveshaft. Ets ets استخدام priيليندر بدائية لخلق شبكة. Tهو رمز المثال أدناه تحويل ylinder Cإلى شبكة.

{{< highlight "python" >}}
from aspose.threed.entities import Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Cylinder class
convertible = Cylinder()
#  Convert a Cylinder to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert 'Torus' إلى 'M'**
A torus هو سطح الثورة الناتجة عن دوار دائرة في الفضاء ثلاثي الأبعاد حول محور متوافق مع الدائرة. If محور الثورة لا تلمس الدائرة ، والسطح لديه شكل حلقة ويسمى توروس الثورة. استخدام et et Torus بدائية لإنشاء شبكة. Tهو رمز المثال أدناه تحويل ororus إلى شبكة.

{{< highlight "python" >}}
from aspose.threed.entities import Torus

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Torus class
convertible = Torus()
#  Convert a Torus to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
