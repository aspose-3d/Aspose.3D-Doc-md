---
title: Comment exécuter Aspose.3D dans AWS Lambda
type: docs
description: Intégrez la fonctionnalité Aspose.3D dans votre application à l'aide de Docker, quelle que soit la technologie de votre pile de développement. Apprenez à utiliser Aspose.3D dans un conteneur Docker
weight: 141
url: /fr/net/how-to-run-aspose-3d-in-aws-lambda/
---
## Préparer l'environnement AWS

1. Enregistrez un compte AWS:
[Enregistrer un compte AWS](https://aws.amazon.com/)
1. Connectez-vous à votre compte AWS, ajoutez un utilisateur IAM sous votre compte. Vous pouvez vous référer au document officiel AWS:
[Ajouter un utilisateur IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
1. Ajouter la permission "AmazonS3FullAccess", s'il vous plaît utiliser de la même manière, ajouter EC2 et Elastic Beanstalk, accès complet pour chacun.
1. À la dernière étape, assurez-vous d'obtenir le nom d'utilisateur IAM, la clé, l'ID de clé et le fichier «credentials.csv», vous devez bien les enregistrer.
Maintenant, assurez-vous que votre utilisateur IAM a S3, EC2, Elastic Beanstalk, un accès complet. Voir:
   
**! [Accès AWS] (AwsAccess.png)**

## Installer AWS Toolkit pour Visual Studio

1. Installez Visual Studio 2019 ou une version ultérieure.
1. Téléchargez et installez AWS Toolkit pour Visual Studio:
[Boîte à outils AWS](https://aws.amazon.com/visualstudio/)

## Créer un projet en cours d'exécution dans AWS Lambda

1. Créez une application Web principale ASP .NET dans Visual Studio, écrivez le code de test, obtenez Aspose.3D à partir de nuget.

1. Assurez-vous que le projet de test fonctionne bien sur votre machine locale, puis déployez-le sur AWS Elastic Beanstalk:
Cliquez avec le bouton droit sur le nom du projet, choisissez "Publier sur AWS Elastic Beanstalk". (Cette option n'existe qu'une fois que vous avez installé AWS Toolkit pour Visual Studio).
1. Vous devrez ajouter un nouvel utilisateur avec votre compte AWS et votre utilisateur IAM, vous pouvez importer le fichier "credentials.csv" que vous obtenez à l'étape précédente.
1. Publier succès, vous obtiendrez une adresse de lien comme: `http://testprojectaspose-test.us-west-2.elasticbeanstalk.com/`
Attendez 10 minutes pour que le lien prenne effet, alors vous pouvez le visiter!
