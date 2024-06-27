---
title: Hur man kör Aspose.3D i AWS
type: docs
description: Integrera Aspose.3D funktionalitet i programmet med Docker oavsett vilken teknik som finns i utvecklingsstacken. Lär dig hur du använder Aspose.3D i en Dockerbehållare.
weight: 141
url: /sv/net/how-to-run-aspose-3d-in-aws-lambda/
---
## Förbered AWS-miljön

1. Registrera ett AWS-konto:
[Register AWS account](https://aws.amazon.com/)
1. Logga in på ditt AWS-konto, lägg till en IAM-användare under ditt konto. Du kan hänvisa till AWS:s officiella dokument:
[Add IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
1. Lägg tillåtelse “AmazonS3FullAccess”, vänligen använd samma sätt, lägg till EC2 och Elastic Beanstalk, full tillgång för varje.
1. Vid det sista steget, se till att du får IAM användarnamn, Key, Key ID, och “credentials. csv” fil, du måste spara dem väl.
Se nu till att din IAM-användare har S3, EC2, Elastic Beanstalk, full tillgång. Se:
   
**! [Aws Access.png)**

## Installera AWS-verktygslåda för Visual StudioName

1. Installera Visual Studio 2019 eller ovanför version.
1. Ladda ner och installera AWS Toolkit för Visual Studio:
[AWS Toolkit](https://aws.amazon.com/visualstudio/)

## Skapa ett projekt som kör i AWS Lambda

1. Skapa en ASP.NET Kärnwebbprogram i Visual Studio, skriva testkod, få Aspose.3D från nuget.

1. Se till att testprojektet fungerar bra på din lokala maskin, sedan distribuera den till AWS Elastic Beanstalk:
Högerklicka på projektnamnet, välj "Publicera till AWS Elastic Beanstalk". (Detta alternativ kommer endast att finnas när du installerar AWS Toolkit för Visual Studio).
1. Du måste lägga till en ny användare med ditt AWS-konto och IAM-användare, du kan importera "credentials. csv "fil som du får i föregående steg.
1. Publicera framgång, får du en länkadress som: `http://testprojectaspose-test.us-west-2.elasticbeanstalk.com/`.
Vänta 10 minuter för att länken får effekt, då kan du besöka den!
