---
title: Arbeiten mit linearer Extrusion
type: docs
weight: 110
url: /de/python-net/working-with-linear-extrusion/
description: Aspose.3D for Python via .NET bietet die LinearExtrusion-Klasse, die als Eingabe eine 2D-Form annimmt und die Form in der 3. Dimension erweitert.
---
#  **Lineare Extrusion durchführen**
Aspose.3D for Python via .NET bietet eine `LinearExtrusion`-Klasse, die eine 2D-Form als Eingabe annimmt und die Form in der 3. Dimension erweitert. Das folgende Code-Snippet zeigt, wie eine lineare Extrusion durchgeführt wird:



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
#  **"Slices" in der linearen Extrusion**
Aspose.3D for Python via .NET bietet `slices` Eigentum der `LinearExtrusion` Klasse. Die `slices`-Eigenschaft definiert die Anzahl der Zwischen punkte entlang des Pfades der Extrusion. Das folgende Code-Snippet zeigt, wie die Eigenschaft `slices` in der linearen Extrusion verwendet wird:



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
#  **"Zentrum" in der linearen Extrusion**
Aspose.3D for Python via .NET bietet `center` Eigentum der `LinearExtrusion` Klasse. Wenn die `center`-Eigenschaft auf `True` festgelegt ist, reicht der Extrusion bereich von-Höhe/2 bis Höhe/2, andernfalls ist die Extrusion von 0 bis Höhe. Das folgende Code-Snippet zeigt, wie die Eigenschaft `center` in der linearen Extrusion verwendet wird:



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
#  **'Twist' in der linearen Extrusion**
Aspose.3D for Python via .NET bietet `twist` Eigentum der `LinearExtrusion` Klasse. Die Eigenschaft `twist` behandelt den Grad der Rotation, während die Form extrudiert wird. Das folgende Code-Snippet zeigt, wie die Eigenschaft `twist` in der linearen Extrusion verwendet wird:



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
#  **'Twist _ offset' in der linearen Extrusion**
Aspose.3D for Python via .NET bietet `twist_offset` Eigentum der `LinearExtrusion` Klasse. `twist_offset` Eigenschaft übersetzt Offset beim Drehen der Extrusion. Das folgende Code-Snippet zeigt, wie die Eigenschaft `twist_offset` in der linearen Extrusion verwendet wird:



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
#  **"Richtung" in der linearen Extrusion**
Aspose.3D for Python via .NET bietet `direction` Eigentum der `LinearExtrusion` Klasse. Die Eigenschaft `direction` definiert die Richtung der Extrusion. Das folgende Code-Snippet zeigt, wie die Eigenschaft `direction` in der linearen Extrusion verwendet wird:



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
