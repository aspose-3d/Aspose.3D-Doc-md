---
title: Come eseguire Aspose.3D for Java in Docker
type: docs
description: Esegui Aspose.3D for Java in un contenitore Docker per Linux.
weight: 139
url: /it/java/how-to-run-aspose-3d-in-docker/
---
I microservizi, in combinazione con la containerizzazione, consentono di combinare facilmente le tecnologie. Docker consente di integrare facilmente Aspose.3D funzionalità nell'applicazione, indipendentemente dalla tecnologia presente nello stack di sviluppo.

Nel caso in cui ti rivolgi ai microservizi o se la tecnologia principale nello stack non è .NET, C++ o Java, ma hai bisogno di Aspose.3D funzionalità, o se usi già Docker nello stack, potresti essere interessato a utilizzare Aspose.3D for Java in un contenitore Docker.

## Prerequisiti

- Docker deve essere installato sul tuo sistema.

## Crea un'applicazione Java

In questo esempio, crei un'applicazione Java che crea un semplice file 3d, lo salva e lo legge. L'applicazione può quindi essere costruita ed eseguita in Docker.

### Creazione dell'applicazione Java

Crea un'applicazione Java in Eclipse usando il codice seguente. In questo esempio, usiamo Aspose.3D for Java per creare un piano nella scena 3d e impostare il vettore e salvarlo in formato obj.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene
Scene scene = new Scene();
// Initialize Plane
Plane plane = new Plane();
// Set Vector
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save(MyDir+"ChangePlaneOrientation.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

### Trasforma la domanda da Java in un pacchetto di barattoli

La figura seguente mostra un modo per creare un pacchetto di barattoli utilizzando il menu "Esporta" in Eclipse.

**! [Crea un barattolo usando Eclipse] (MakeJar.png)**

Ora che abbiamo scritto un programma Java utilizzando Aspose.3D for Java, abbiamo ricevuto un pacco barattolo. La prossima volta faremo un dockerfile.

### Configurazione di un Dockerfile

Il prossimo passo è creare e configurare il Dockerfile.

1. Crea il Dockerfile e posizionalo accanto al pacchetto jar. Conserva questo nome file senza estensione (l'impostazione predefinita).
2. Nel Dockerfile, specificare:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### Costruire ed eseguire l'applicazione in Docker

Ora l'applicazione può essere costruita ed eseguita in Docker. Apri il prompt dei comandi preferito, cambia la directory nella cartella con il Dockerfile ed esegui il seguente comando:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

Dopo aver eseguito il comando sopra, otterrai l'output del file 3D. A questo punto, un programma Java è stato eseguito con successo in Linux Docker.
