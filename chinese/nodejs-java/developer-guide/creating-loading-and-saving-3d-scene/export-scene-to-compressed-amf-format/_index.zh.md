---
title: 将场景导出为压缩的 AMF 格式
type: docs
weight: 60
url: /zh/nodejs-java/export-scene-to-compressed-amf-format/
description: Aspose.3D for Node.js via Java 提供了AmfSaveOptions类，允许您根据需要设置压缩的布尔值。
---
#  **将场景导出为压缩的 AMF 格式**
Aspose.3D for Node.js via Java 提供 `AmfSaveOptions` 类，允许您根据需要设置压缩的布尔值。默认情况下，该值设置为true。以下代码段显示了生成压缩的 AMF 格式文件的完整功能:

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

var box=new aspose.threed.Box();

var node=scene.getRootNode().createChildNode(box);

node.getTransform().setScale(new aspose.threed.Vector3(12, 17, 12));
node.getTransform().setTranslation(new aspose.threed.Vector3(10, 1, 0));

var opt =new aspose.threed.AmfSaveOptions();
opt.setEnableCompression(false);

scene.save("test.amf");

{{< /highlight >}}
