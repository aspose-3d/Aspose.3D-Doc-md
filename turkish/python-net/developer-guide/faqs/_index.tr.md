---
title: FAQs
type: docs
weight: 170
url: /tr/python-net/faqs/
description: Frequently asked questions about Aspose.3D for .net.
---
####  **Q: How to animate FBX or other 3D format’s special property that wasn’t defined in Aspose.3D?**
* A **: hedef nesne üzerinde dinamik bir özellik oluşturun ve dinamik özellik üzerinde özellik animasyonu gerçekleştirin, çünkü özellik beton dosya formatına bağlıdır, Aspose.3D sahneyi farklı bir format türüne kaydederken animasyonun çalışabileceğini garanti edemez.
####  **Q: Why animation on scene’s root node is not working when serialized to FBX file?**
* A **: FBX formatı, kök düğümünün özelliklerine erişmenize izin vermez, böylece animasyon çalışmaz.
####  **Q: Why I changed the asset info on scene, and try to import the generated FBX file to 3ds max, those information were all lost?**
*A**: 3Ds MAX or some other softwares can only import FBX file, but not open the FBX file, that means it allows you to import multiple FBX inside one scene, if the asset info can be applied to the current scene, then your original scene info may be overwritten by importing, so that’s 3Ds MAX’s design policy to not import the scene’s asset info.
