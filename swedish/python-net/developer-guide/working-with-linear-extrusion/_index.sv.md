---
title: Arbeta med linjär extrusion
type: docs
weight: 110
url: /sv/python-net/working-with-linear-extrusion/
description: Aspose.3D for Python via .NET erbjuder LinearExtrusion klass, som tar en 2D-form som inmatning och utökar formen i den tredje dimensionen.
---
#  **Utför linjär extrusion**
Aspose.3D for Python via .NET erbjuder `LinearExtrusion` klass, som tar en 2D-form som inmatning och utökar formen i den tredje dimensionen. Följande kod snutt visar hur man utför linjär extrusion:



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
#  **'Slices' i linjär extrusion**
Aspose.3D for Python via .NET erbjuder `slices` egendom för `LinearExtrusion` klassen. `slices` egenskapen definierar antalet mellanliggande punkter längs sökvägen för utpressningen. Följande kodsnutt visar hur egenskapen `slices` används i linjär extrusion:



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
#  **'Centrum' i linjär extrusion**
Aspose.3D for Python via .NET erbjuder `center` egendom för `LinearExtrusion` klassen. Om egenskapen `center` är inställd till `True`, är extruderingsområdet från -Höjd/2 till höjd/2, annars. extruderingen är från 0 till höjd. Följande kodsnutt visar hur egenskapen `center` används i linjär extrusion:



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
#  **'Twist' i linjär extrusion**
Aspose.3D for Python via .NET erbjuder `twist` egendom för `LinearExtrusion` klassen. `twist` egenskapen hanterar rotationens grad medan formen extruderas. Följande kodsnutt visar hur egenskapen `twist` används i linjär extrusion:



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
#  **'Twist_offset' i linjär utpressning**
Aspose.3D for Python via .NET erbjuder `twist_offset` egendom för `LinearExtrusion` klassen. Egenskapen `twist_offset` översätter förskjutning vid rotering av extruderingen. Följande kodsnutt visar hur egenskapen `twist_offset` används i linjär extrusion:



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
#  **'Riktning' i linjär extrusion**
Aspose.3D for Python via .NET erbjuder `direction` egendom för `LinearExtrusion` klassen. `direction` egenskapen definierar riktningen för extruderingen. Följande kodsnutt visar hur egenskapen `direction` används i linjär extrusion:



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
