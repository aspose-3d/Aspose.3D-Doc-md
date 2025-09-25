---
title: كشف التحويل الهندسي
type: docs
weight: 50
url: "/ar/nodejs-java/expose-geometric-transformation/"
description: Aspose.3D لـ Node.js عبر Java يتيح تعريض التحويل الهندسي لمشهد ثلاثي الأبعاد. يمكنك تقييم التحويل العام باستخدام طريقة evaluateGlobalTransform.
---

# **كشف التحويل الهندسي**
يتيح Aspose.3D for Node.js via Java كشف التحويل الهندسي لمشهد ثلاثي الأبعاد. يمكنك تقييم التحويل العام باستخدام طريقة `evaluateGlobalTransform`. يوضح المقتطف البرمجي التالي كيفية كشف التحويل الهندسي.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize scene object
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder =new aspose.threed.Cylinder();

// Create ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Get Geometric Translation
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// The first Console.WriteLine will output the transform matrix that includes the geometric transformation
// while the second one will not.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}