---
title: Aws lambda Aspose.3D nasıl çalıştırılır
type: docs
description: Integrate Aspose.3D functionality into your application using Docker regardless of what technology is in your development stack. Learn how to use Aspose.3D in a Docker container
weight: 141
url: /tr/net/how-to-run-aspose-3d-in-aws-lambda/
---
## Aws ortamını hazırlayın

1. Bir aws hesabı kaydedin:
[Aws hesabını kaydet](https://aws.amazon.com/)
1. Aws hesabınıza giriş yapın, hesabınızın altına bir iam kullanıcısı ekleyin. Aws resmi belgesine başvurabilirsiniz:
[Iam kullanıcısı ekle](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
1. “Amazons3fullac.” izni ekleyin, lütfen aynı şekilde kullanın, ec2 ve elastik fasulye sapı ekleyin, her biri için tam erişim.
1. Son adımda, iam kullanıcı adı, anahtar, anahtar kimliği ve “cre. als.csv” dosyasını aldığınızdan emin olun, bunları iyi kaydetmeniz gerekir.
Şimdi iam kullanıcılarınızın s3, ec2, elastik fasulye sapı, tam erişime sahip olduğundan emin olun. Bakın:
   
**! [Aws access((awsaccess.png)**

## Görsel stüdyo için aws araç setini yükleyin

1. Görsel studio 2019 veya üstü sürümünü yükleyin.
1. Görsel stüdyo için aws araç setini indirin ve yükleyin:
[Aws araç seti](https://aws.amazon.com/visualstudio/)

## Aws lambda çalıştıran bir proje oluşturun

1. Görsel stüdyoda asp .NET çekirdek web uygulaması oluşturun, test kodunu yazın, Aspose alın. 3D nuget.

1. Test projesinin yerel makinenizde iyi çalıştığından emin olun, daha sonra elastik fasulye sapına dağıtın:
Proje adını sağ tıklayın, "aws elastik beanstalk için yayınla" ı seçin. (Bu seçenek sadece görsel stüdyo için aws araç setini yükledikten sonra mevcut olacaktır).
1. Aws hesabınız ve iam kullanıcınız ile yeni bir kullanıcı eklemeniz gerekecek, önceki adımda aldığınız "cre. als.csv" dosyasını içe aktarabilirsiniz.
1. Başarı yayınlayın, aşağıdaki gibi bir bağlantı adresi alacaksınız: `http://testprojectaspose-test.us-west-2.elasticbeanstalk.com/`
Bağlantının etkili olması için 10 dakika bekleyin, sonra ziyaret edebilirsiniz!
