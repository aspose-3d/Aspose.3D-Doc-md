---
title: So führen Sie Aspose.3D in AWS Lambda aus
type: docs
description: Integrieren Sie die Aspose.3D-Funktional ität mithilfe von Docker in Ihre Anwendung, unabhängig davon, welche Technologie sich in Ihrem Entwicklungs stapel befindet. Erfahren Sie, wie Sie Aspose.3D in einem Docker-Container verwenden
weight: 141
url: /de/net/how-to-run-aspose-3d-in-aws-lambda/
---
## AWS-Umgebung vorbereiten

1. Registrieren Sie ein AWS-Konto:
[AWS-Konto registrieren](https://aws.amazon.com/)
1. Melden Sie sich in Ihrem AWS-Konto an und fügen Sie einen IAM-Benutzer unter Ihrem Konto hinzu. Sie können auf das offizielle AWS-Dokument verweisen:
[IAM-Benutzer hinzufügen](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
1. Fügen Sie die Erlaubnis "AmazonS3FullAccess" hinzu, verwenden Sie bitte den gleichen Weg, fügen Sie EC2 und Elastic Beanstalk hinzu, vollen Zugriff für jeden.
1. Im letzten Schritt stellen Sie sicher, dass Sie den IAM-Benutzernamen, den Schlüssel, die Schlüssel-ID und die Datei "credentials.csv" erhalten. Sie müssen sie gut speichern.
Stellen Sie nun sicher, dass Ihr IAM-Benutzer über S3, EC2, Elastic Beanstalk und vollen Zugriff verfügen. Siehe:
   
**! [AWS Access](AwsAccess.png)**

## Installieren Sie AWS Toolkit für Visual Studio

1. Installieren Sie Visual Studio 2019 oder oben Version.
1. AWS Toolkit für Visual Studio herunter laden und installieren:
[AWS Toolkit](https://aws.amazon.com/visualstudio/)

## Erstellen Sie ein in AWS Lambda laufendes Projekt

1. Erstellen Sie eine ASP .NET Core-Web anwendung in Visual Studio, schreiben Sie Testcode, erhalten Sie Aspose.3D von nuget.

1. Stellen Sie sicher, dass das Test projekt auf Ihrem lokalen Computer gut läuft, und stellen Sie es dann bei AWS Elastic Beanstalk bereit:
Rechts klicken Sie auf den Projektnamen, wählen Sie "In AWS Elastic Beanstalk veröffentlichen". (Diese Option ist nur vorhanden, nachdem Sie AWS Toolkit für Visual Studio installiert haben.)
1. Sie müssen einen neuen Benutzer mit Ihrem AWS-Konto und IAM-Benutzer hinzufügen. Sie können die Datei "credentials.csv" importieren, die Sie im vorherigen Schritt erhalten haben.
1. Wenn Sie Erfolg veröffentlichen, erhalten Sie eine Link-Adresse wie: `http://testprojectaspose-test.us-west-2.elasticbeanstalk.com/`
Warten Sie 10 Minuten, bis der Link wirksam wird, dann können Sie ihn besuchen!
