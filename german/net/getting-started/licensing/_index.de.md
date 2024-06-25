---
title: Licensing
type: docs
weight: 60
url: /de/net/licensing/
description: Übersicht über Licensing Anforderungen und Einschränkungen der Bewertungs version für die Verarbeitung von 3D Dateiformaten in C#.
---
Übersicht über Licensing Anforderungen und Einschränkungen der Bewertungs version für die Verarbeitung von 3D Dateiformaten in C#.

##  **Einschränkungen der Bewertungs version**
Eine kostenlose Bewertungs version von Aspose.3D for .NET kann aus dem Download-Bereich der Aspose-Website unter: [Herunter laden Aspose.3D API](https://www.nuget.org/packages/Aspose.3D) herunter geladen werden.
###  **Beschränkung**
Die Bewertungs version bietet alle Funktionen mit Ausnahme der folgenden:

- Benutzer können nur maximal 50 3D-Dokumente in eine Szene öffnen/importieren.
- Jeder Knoten kann nicht mehr als 5 unter geordnete Knoten haben.
- Jeder Knoten kann nicht mehr als 2 angehängte Entitäten haben.
- Jede Geometrie kann nicht mehr als 2 angehängte Scheitel punkt elemente haben.
- Jeder Knoten kann nicht mehr als 1 Material haben.
- Benutzer können nur maximal 50 3D-Dokumente in einer Szene speichern.
- Benutzer sehen auch ein Bewertungs wasser zeichen in den gerenderten Bildern und allen anderen Ausgabe dateien.

{{% alert color="primary" %}} 
Wenn Sie Aspose.3D ohne eine ordnungs gemäße Lizenz verwenden, könnte es eine `Aspose.ThreeD.TrialException` auslösen, wenn die Nutzung die nicht lizenzierten Einschränkungen erreicht hat. Sie können die Ausnahme deaktivieren, indem Sie:

* [Kaufen Sie eine voll ausgestattete Lizenz](https://purchase.aspose.com/buy).
* Fordern Sie eine 30-tägige Lizenz an, siehe [Wie bekomme ich eine vorübergehende Lizenz?](https://purchase.aspose.com/temporary-license) Weitere Informationen.
.
* Setzen Sie `Aspose.ThreeD.TrialException.SuppressTrialException` auf `true`. Die `TrialException` werden während des `Open/Save`-Anrufs auf der Szene nicht erhöht, aber die oben genannten Einschränkungen werden nicht aufgehoben.
* Verwenden Sie manuell einen `try/catch`-Block auf `Scene.Open/Save`. Diese Ausnahme ist nur eine Benachricht igung. Ignorieren Sie, dass das Laden/Speichern der Szene keine Auswirkungen hat.

{{% /alert %}} 

##  **Lizenz mit Datei oder Stream-Objekt anwenden**
Die Lizenz kann von [Datei](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) oder [Stream-Objekt](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject) geladen werden. Aspose.3D for .NET wird versuchen, die Lizenz an den folgenden Orten zu finden:

1. Expliziter Weg.
1. Der Ordner, der Aspose.3D.dll enthält.
1. Der Ordner, der die Assembly mit dem Namen Aspose.3D.dll enthält.
1. Der Ordner, der die Entry Assembly enthält (Ihr. Exe).
1. Eine eingebettete Ressource in der Assembly mit dem Namen Aspose.3D.dll.

Der einfachste Weg, eine Lizenz festzulegen, besteht darin, die Lizenz datei in den gleichen Ordner wie die Datei Aspose.3D.dll zu legen und den Dateinamen ohne Pfad anzugeben, wie im folgenden Beispiel gezeigt.

{{% alert color="primary" %}} 

Wenn Sie andere Aspose for .NET API zusammen mit Aspose.3D for .NET verwenden, geben Sie bitte den Namens raum für die Lizenz wie `Aspose.ThreeD.License` an.

{{% /alert %}} 
###  **Laden einer Lizenz aus der Datei**
Der einfachste Weg, eine Lizenz anzuwenden, besteht darin, die Lizenz datei in denselben Ordner wie die Datei Aspose.3D.dll zu legen und nur den Dateinamen ohne Pfad anzugeben.

{{% alert color="primary" %}} 

Wenn Sie die `SetLicense`-Methode aufrufen, sollte der Lizenz name, den Sie übergeben, der der Lizenz datei sein. Wenn Sie beispiels weise den Namen der Lizenz datei in "Aspose.3D.lic.xml" ändern, geben Sie diesen Dateinamen an die Methode `threeD.SetLicense(…)` weiter.

{{% /alert %}} 

**Beispiel:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
###  ` `**Laden einer Lizenz aus einem Stream-Objekt**
Das folgende Beispiel zeigt, wie eine Lizenz aus einem Stream geladen wird.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
##  **Lizenz mit Embedded Resource anwenden**
Eine Möglichkeit, eine Lizenz zu beantragen, besteht darin, sie für [Verwendung einer Datei oder eines Stream-Objekts]() festzulegen. Eine weitere Möglichkeit, die Lizenz mit Ihrer Anwendung zu verpacken und sicher zustellen, dass sie nicht verloren geht, besteht darin, sie als eingebettete Ressource in eine der Baugruppen aufzunehmen, die die DLL der Komponente aufruft (enthalten in Aspose.3D).

So schließen Sie die Lizenz datei als eingebettete Ressource ein:

1. In Visual Studio .NET, fügen Sie die Lizenz datei (.lic) in das Projekt ein, indem Sie**Datei**, Dann**Vorhandene Artikel hinzufügen**Und schließlich**Hinzufügen**.
1. Wählen Sie die Datei im Solution Explorer aus.
1. Stellen Sie die**Aktion bauen**Zu**Eingebettete Ressource**Im Eigenschaften fenster.
1. Um auf die in die Assembly eingebettete Lizenz zuzugreifen (als eingebettete Ressource), fügen Sie einfach die Lizenz datei als eingebettete Ressource zum Projekt hinzu und geben Sie den Namen der Lizenz datei an die SetLicense-Methode weiter. Die Lizenz klasse findet die Lizenz datei automatisch in den eingebetteten Ressourcen. Es ist nicht erforderlich, die Get Executing Assembly-und Get Manifest Resource Stream-Methoden der Klasse System.Reflection.Assembly im Microsoft .NET Framework aufzurufen.

Das folgende Code-Snippet wird verwendet, um die Lizenz festzulegen.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
##  **Metered Lizenz anwenden**
Aspose.3D for .NET API ermöglicht es Entwicklern, eine gemeerte Lizenz zu beantragen. Es ist ein neuer Lizenzierung mechanismus. Der neue Lizenzierung mechanismus wird zusammen mit der bestehenden Lizenzierung methode verwendet. Kunden, die basierend auf der Nutzung der API-Funktionen in Rechnung gestellt werden möchten, können die gemeerte Lizenzierung verwenden. Weitere Informationen finden Sie im Abschnitt [Gezählte Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered).

Eine neue Klasse [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) wurde hinzugefügt, um den gemetzten Schlüssel anzuwenden. Dieses Code beispiel zeigt, wie gemetzte öffentliche und private Schlüssel festgelegt werden:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
