---
title: Trabajando con extrusión lineal
type: docs
weight: 110
url: /es/python-net/working-with-linear-extrusion/
description: Aspose.3D for Python via .NET ofrece la clase LinearExtrusion, que toma una forma 2D como entrada y extiende la forma en la tercera dimensión.
---
#  **Realización de extrusión lineal**
Aspose.3D for Python via .NET ofrece la clase `LinearExtrusion`, que toma una forma 2D como una entrada y extiende la forma en la 3ª dimensión. El siguiente fragmento de código muestra cómo realizar la extrusión lineal:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
extrusion = LinearExtrusion(profile, 10)
extrusion.slices = 100
extrusion.center = True
extrusion.twist = 360.0
extrusion.twist_offset = Vector3(10, 0, 0)
#  Perform Linear extrusion by passing a 2D profile as input and extend the shape in the 3rd dimension
extrusion = extrusion
#  Create a scene
scene = Scene()
#  Create a child node by passing extrusion
scene.root_node.create_child_node(extrusion)
#  Save 3D scene
scene.save("out"  + "LinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Rebanas' en extrusión lineal**
Aspose.3D for Python via .NET ofrece la propiedad `slices` de la clase `LinearExtrusion`. La propiedad `slices` define el número de puntos intermedios a lo largo de la trayectoria de la extrusión. El siguiente fragmento de código muestra cómo usar la propiedad `slices` en la extrusión lineal:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(15, 0, 0)
extrusion = LinearExtrusion(profile, 2)
extrusion.slices = 2 
#  Slices parameter defines the number of intermediate points along the path of the extrusion
#  Perform linear extrusion on left node using slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 2)
extrusion2.slices = 10 
#  Perform linear extrusion on right node using slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "SlicesInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Center' en extrusión lineal**
Aspose.3D for Python via .NET ofrece la propiedad `center` de la clase `LinearExtrusion`. Si la propiedad `center` está establecida en `True`, el rango de extrusión es de-Height/2 a Height/2; de lo contrario, la extrusión es de 0 a Height. El siguiente fragmento de código muestra cómo usar la propiedad `center` en extrusión lineal:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(15, 0, 0)
extrusion = LinearExtrusion(profile, 2)
extrusion.slices = 2 
#  Slices parameter defines the number of intermediate points along the path of the extrusion
#  Perform linear extrusion on left node using slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 2)
extrusion2.slices = 10 
#  Perform linear extrusion on right node using slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "SlicesInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Twist' en extrusión lineal**
Aspose.3D for Python via .NET ofrece la propiedad `twist` de la clase `LinearExtrusion`. `twist` controla el grado de rotación mientras se extruye la forma. El siguiente fragmento de código muestra cómo usar la propiedad `twist` en la extrusión lineal:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create rifht node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(15, 0, 0)
extrusion = LinearExtrusion(profile, 10)
extrusion.twist = 0.0
extrusion.slices = 100 
#  Twist property defines the degree of the rotation while extruding the profile
#  Perform linear extrusion on left node using twist and slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 10)
extrusion2.twist = 90.0
extrusion2.slices = 100 
#  Perform linear extrusion on right node using twist and slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "TwistInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Twist _ offset' en Extrusión lineal**
Aspose.3D for Python via .NET ofrece la propiedad `twist_offset` de la clase `LinearExtrusion`. La propiedad `twist_offset` convierte el desplazamiento al girar la extrusión. El siguiente fragmento de código muestra cómo usar la propiedad `twist_offset` en la extrusión lineal:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(18, 0, 0)
extrusion = LinearExtrusion(profile, 10)
extrusion.twist = 360.0
extrusion.slices = 100 
#  TwistOffset property is the translate offset while rotating the extrusion.
#  Perform linear extrusion on left node using twist and slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 10)
extrusion2.twist = 360.0
extrusion2.slices = 100
extrusion2.twist_offset = Vector3(3, 0, 0)
#  Perform linear extrusion on right node using twist, twist offset and slices property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "TwistOffsetInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
#  **'Dirección' en extrusión lineal**
Aspose.3D for Python via .NET ofrece la propiedad `direction` de la clase `LinearExtrusion`. `direction` La propiedad define la dirección de la extrusión. El siguiente fragmento de código muestra cómo usar la propiedad `direction` en la extrusión lineal:



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import LinearExtrusion
from aspose.threed.profiles import RectangleShape
from aspose.threed.utilities import Vector3

shape = RectangleShape()
shape.rounding_radius = 0.3

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize the base profile to be extruded
profile = shape
#  Create a scene
scene = Scene()
#  Create left node
left = scene.root_node.create_child_node()
#  Create right node
right = scene.root_node.create_child_node()
left.transform.translation = Vector3(8, 0, 0)
extrusion = LinearExtrusion(profile, 10)
extrusion.twist = 360.0
extrusion.slices = 100 
#  Direction property defines the direction of the extrusion.
#  Perform linear extrusion on left node using twist and slices property
left.create_child_node(extrusion)
extrusion2 = LinearExtrusion(profile, 10)
extrusion2.twist = 360.0
extrusion2.slices = 100
extrusion2.direction = Vector3(0.3, 0.2, 1)
#  Perform linear extrusion on right node using twist, slices, and direction property
right.create_child_node(extrusion2)
#  Save 3D scene
scene.save("out"  + "DirectionInLinearExtrusion.obj", FileFormat.WAVEFRONT_OBJ)

{{< /highlight >}}
