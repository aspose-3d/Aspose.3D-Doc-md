---
title : "Cast and Receive Shadows on 3D Geometries" 
description : "" 
weight : 12054 
toc : false
type: docs
url: /net/developerguide/rendering/cast+and+receive+shadows+on+3d+geometries/
---

# Aspose.3D for .NET : Cast and Receive Shadows on 3D Geometries


Generally, some 3D file formats can store shadow related settings in geometry like FBX. Using [Aspose.3D for .NET](http://www.aspose.com/3d-component-suite.aspx), developers can render an image by mapping shadows from the viewpoint of a light source. The image quality depends on the light source, elevation angle and distance between the camera and geometric objects.

## Cast and Receive Shadow

By default, all objects in the scene cast shadows from a light source. Developers may also receive shadows on a per object basis in the object surface. This code example reveals how to set the position of light and camera objects. It also creates a plane and places three objects with different colors and shadow settings.

All geometries has `CastShadows = true` and `ReceiveShadows=true`, the shadows of red box and torus casted to the plane, the red box won't receive shadows and blue box won't cast shadows.

### Programming Sample

This code example casts and Receives shadows on 3D geometries.

**  
Render Result**

![RenderPicture](20119577.png)

