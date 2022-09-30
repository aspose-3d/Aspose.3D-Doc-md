---
title: FAQs
type: docs
weight: 170
url: /de/python-net/faqs/
description: Häufig gestellte Fragen zu Aspose.3D für. Netz.
---
#### **F: Wie animiert man die besondere Eigenschaft FBX oder eines anderen 3D-Formats, die nicht in Aspose.3D definiert wurde?**
** A **: Erstellen Sie eine dynamische Eigenschaft für das Zielobjekt und führen Sie eine Eigenschaft animation für die dynamische Eigenschaft durch. Da die Eigenschaft vom konkreten Dateiformat abhängt, kann Aspose.3D nicht garantieren, dass die Animation funktioniert, wenn Sie die Szene in einem anderen Format speichern Typ.
#### **F: Warum funktioniert die Animation im Root-Knoten der Szene nicht, wenn sie auf die Datei FBX serial isiert wird?**
** A **: Im Format FBX können Sie nicht auf die Eigenschaften des Stamm knotens zugreifen, sodass die Animation nicht funktioniert.
#### **F: Warum habe ich die Asset-Informationen in der Szene geändert und versucht, die generierte FBX-Datei in 3ds max zu importieren. Diese Informationen sind alle verloren gegangen?**
** A **: 3Ds MAX oder eine andere Software können nur FBX-Datei importieren, aber nicht die FBX-Datei öffnen, was bedeutet, dass Sie mehrere FBX in eine Szene importieren können, wenn die Asset-Informationen auf die aktuelle Szene angewendet werden können, dann Ihre ursprünglichen Szenen informationen können durch Importieren übers chrieben werden. Das ist also die Design richtlinie von 3Ds MAX, um die Asset-Informationen der Szene nicht zu importieren.
