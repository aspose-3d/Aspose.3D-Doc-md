---
title: Din första Aspose.3D-applikation
type: docs
weight: 30
url: /sv/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

Den här guiden förklarar hur man skapar en första applikation med Asposes enkla API för 3D. Denna enkla applikation skapar en 3D-fil i en specificerad 3D-scen.

{{% /alert %}}

## **Hur man skapar applikationen**

Följande steg skapar applikationen med Aspose.3D API:

1. Skapa en instans av klassen [Scene](https://reference.aspose.com/3d/sv/python-net/aspose.threed/scene/).
1. Om du har en licens, [tillämpa den](/3d/sv/python-net/licensing/).
   Om du använder utvärderingsversionen kan du hoppa över kodrader som rör licens.
1. Skapa en ny 3D-fil eller öppna en befintlig 3D-fil.
1. Få tillgång till sceninnehållet i 3D-filen.
1. Generera den modifierade 3D-filen.

Implementeringen av ovanstående steg demonstreras i exemplen nedan.

### **Hur man skapar ett nytt scendokument**

Följande exempel skapar en ny 3D-scenfil från grunden. Börja med att skapa en 3D-scen och spara sedan filen i FBX-format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}

### **Hur man öppnar en befintlig fil**

Följande exempel öppnar en befintlig 3D-mallfil vid namn "document.fbx".

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
