---
title: Apply Visual Effects on Saving 3D Views
type: docs
weight: 10
url: /net/apply-visual-effects-on-saving-3d-views/
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), developers may apply visual effects on 3D Views before saving in the image. These visual effects are also known as the post-processing effects or filters those are applied in real-time to everything displayed in the 3D View.

{{% /alert %}}
## **Apply Visual Effects on 3D View**
The [GetPostProcessing](http://www.aspose.com/api/net/3d/aspose.threed.render/renderer/methods/getpostprocessing) method of the [Renderer](http://www.aspose.com/api/net/3d/aspose.threed.render/renderer) class allows to create any supported visual effect. The Renderer class offers a [PostProcessings](http://www.aspose.com/api/net/3d/aspose.threed.render/renderer/properties/postprocessings) member to apply various filters, the Add method of the PostProcessings class allows to incorporate a filter before rendering.
### **Programming Sample**
This code example applies visual effect on a 3D view.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
