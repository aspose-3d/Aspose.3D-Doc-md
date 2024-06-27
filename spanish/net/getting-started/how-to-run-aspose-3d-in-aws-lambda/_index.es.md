---
title: Cómo ejecutar Aspose.3D en AWS Lambda
type: docs
description: Integre la funcionalidad Aspose.3D en su aplicación usando Docker, independientemente de la tecnología que esté en su pila de desarrollo. Aprenda a usar Aspose.3D en un contenedor Docker
weight: 141
url: /es/net/how-to-run-aspose-3d-in-aws-lambda/
---
## Preparar el entorno de AWS

1. Registrar una cuenta de AWS:
[Registrar una cuenta de AWS](https://aws.amazon.com/)
1. Inicie sesión en su cuenta de AWS, agregue un usuario de IAM en su cuenta. Puede consultar el documento oficial de AWS:
[Agregar usuario de IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
1. Agregue el permiso "AmazonS3FullAccess", use la misma manera, agregue EC2 y Elastic Beanstalk, acceso completo para cada uno.
1. En el último paso, asegúrese de obtener el nombre de usuario de IAM, la clave, el ID de clave y el archivo "credentials.csv", debe guardarlos bien.
Ahora asegúrese de que su usuario de IAM tenga S3, EC2, Elastic Beanstalk, acceso completo. Véase:
   
**¡! [AWS Access] (AwsAccess.png)**

## Instalar AWS Toolkit para Visual Studio

1. Instale Visual Studio 2019 o una versión superior.
1. Descargue e instale AWS Toolkit para Visual Studio:
[Kit de herramientas de AWS](https://aws.amazon.com/visualstudio/)

## Crear un proyecto ejecutándose en AWS Lambda

1. Cree una aplicación web principal de ASP .NET en Visual Studio, escriba el código de prueba, obtenga Aspose.3D desde nuget.

1. Asegúrese de que el proyecto de prueba se ejecute correctamente en su máquina local y luego implemente el proyecto en AWS Elastic Beanstalk:
Haga clic con el botón derecho en el nombre del proyecto, elija "Publicar en AWS Elastic Beanstalk". (Esta opción solo existirá después de instalar AWS Toolkit for Visual Studio).
1. Tendrá que agregar un nuevo usuario con su cuenta de AWS y usuario de IAM, puede importar el archivo "credentials.csv" que obtiene en el paso anterior.
1. Publicar el éxito, obtendrá una dirección de enlace como: `http://testprojectaspose-test.us-west-2.elasticbeanstalk.com/`
¡Espere 10 minutos para que el enlace surta efecto, entonces usted puede visitarlo!
