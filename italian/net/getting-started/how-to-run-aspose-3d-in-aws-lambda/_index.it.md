---
title: Come eseguire Aspose.3D in AWS Lambda
type: docs
description: Integra Aspose.3D funzionalità nell'applicazione utilizzando Docker indipendentemente dalla tecnologia presente nello stack di sviluppo. Scopri come utilizzare Aspose.3D in un contenitore Docker
weight: 141
url: /it/net/how-to-run-aspose-3d-in-aws-lambda/
---
## Preparare l'ambiente AWS

1. Registra un account AWS:
[Registra l'account AWS](https://aws.amazon.com/)
1. Accedi al tuo account AWS, aggiungi un utente IAM sotto il tuo account. È possibile fare riferimento al documento ufficiale AWS:
[Aggiungi utente IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
1. Aggiungi l'autorizzazione "AmazonS3FullAccess", usa lo stesso modo, aggiungi EC2 e Elastic Beanstalk, accesso completo per ciascuno.
1. All'ultimo passaggio, assicurati di ottenere il nome utente IAM, la chiave, l'ID chiave e il file "credentials.csv", devi salvarli bene.
Ora assicurati che il tuo utente IAM abbia S3, EC2, Elastic Beanstalk, accesso completo. Vedi:
   
**! [AWS Access] (AwsAccess.png)**

## Installare AWS Toolkit per Visual Studio

1. Installa Visual Studio 2019 o versione superiore.
1. Scaricare e installare AWS Toolkit per Visual Studio:
[Kit di strumenti AWS](https://aws.amazon.com/visualstudio/)

## Creare un progetto in esecuzione in AWS Lambda

1. Crea un'applicazione Web principale ASP .NET in Visual Studio, scrivi codice di test, ottieni Aspose.3D da nuget.

1. Assicurati che il progetto di test funzioni bene sul tuo computer locale, quindi distribuiscilo su AWS Elastic Beanstalk:
Fare clic con il pulsante destro del mouse sul nome del progetto, scegliere "Pubblica su AWS Elastic Beanstalk". (Questa opzione esiste solo dopo l'installazione di AWS Toolkit per Visual Studio).
1. Dovrai aggiungere un nuovo utente con il tuo account AWS e utente IAM, puoi importare il file "credentials.csv" che ottieni nel passaggio precedente.
1. Pubblicazione riuscita, otterrai un indirizzo di collegamento come: `http://testprojectaspose-test.us-west-2.elasticbeanstalk.com/`
Attendi 10 minuti affinché il link abbia effetto, quindi puoi visitarlo!
