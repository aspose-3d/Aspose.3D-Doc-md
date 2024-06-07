---
title: FAQs
type: docs
weight: 190
url: /net/faqs/
description: Frequently asked questions about Aspose.3D for .net.
---

#### **Q: How to animate FBX or other 3D format’s special property that wasn’t defined in Aspose.3D?**
**A**: Create a dynamic property on the target object, and perform property animation on the dynamic property, since the property depends on concrete file format, Aspose.3D can’t guarantee the animation can work when you save the scene to a different format type.
#### **Q: Why animation on scene’s root node is not working when serialized to FBX file?**
**A**: The FBX format doesn’t allow you to access the properties of the root node, so the animation will not work.
#### **Q: Why I changed the asset info on scene, and try to import the generated FBX file to 3ds max, those information were all lost?**
**A**: 3Ds MAX or some other softwares can only import FBX file, but not open the FBX file, that means it allows you to import multiple FBX inside one scene, if the asset info can be applied to the current scene, then your original scene info may be overwritten by importing, so that’s 3Ds MAX’s design policy to not import the scene’s asset info.


#### **Q: A node consists of multiple meshes (for the glass, the frame, etc). All those meshes are in the entity list of the node. How to add a material to all of those nodes (the material is just the color)?**
**A**: The best solution should create sub nodes for each mesh, and assign different material to each sub node.