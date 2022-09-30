---
title: Lizenzierung
description: "Aspose.3D für Python via .NET bietet verschiedene Kauf pläne oder eine kostenlose Testversion und eine vorübergehende 30-Tage-Lizenz für die Bewertung mithilfe von Lizenz-und Abonnement richtlinien."
type: docs
weight: 80
url: /de/python-net/licensing/
---
Manchmal, um das System besser zu studieren, möchten Sie so schnell wie möglich in den Code eintauchen. Um dies zu vereinfachen, bietet Aspose.3D verschiedene Kaufpläne oder eine kostenlose Testversion und eine vorübergehende 30-Tage-Lizenz zur Bewertung.

{{% alert color="primary" %}}

Beachten Sie, dass es eine Reihe allgemeiner Richtlinien und Praktiken gibt, die Ihnen helfen, unsere Produkte zu bewerten, ordnungs gemäß zu lizenzieren und zu kaufen. Sie finden sie in der["Einkaufs richtlinien und FAQ"](https://purchase.aspose.com/policies)Abschnitt.

{{% /alert %}}

## **Bewerten Aspose.3D**
Sie können ganz einfach Aspose.3D zur Auswertung herunter laden. Das Bewertungs paket ist das gleiche wie das gekaufte Paket. Die Bewertungs version wird einfach lizenziert, nachdem Sie einige Code zeilen hinzugefügt haben, um die Lizenz anzuwenden.

## **Beschränkung der Bewertungs version**
Die Bewertungs version bietet alle Funktionen mit Ausnahme der folgenden:

- Benutzer können maximal 50 3D-Dokumente in eine Szene öffnen/importieren.
- Jeder Knoten kann nicht mehr als 5 unter geordnete Knoten haben.
- Jeder Knoten kann nicht mehr als 2 angehängte Entitäten haben.
- Jede Geometrie kann nicht mehr als 2 angehängte Scheitel punkt elemente haben.
- Jeder Knoten kann nicht mehr als 1 Material haben.
- Benutzer können nur maximal 50 3D-Dokumente in einer Szene speichern.
- Benutzer sehen auch ein Bewertungs wasser zeichen in den gerenderten Bildern und allen anderen Ausgabe dateien.

{{% alert color="primary" %}} 
Wenn Sie Aspose.3D ohne ordnungs gemäße Lizenz verwenden, kann es eine `aspose.threed.TrialException` auslösen, wenn die Nutzung die nicht lizenzierten Einschränkungen erreicht hat. Sie können die Ausnahme deaktivieren, indem Sie:

* [Kaufen Sie eine voll ausgestattete Lizenz](https://purchase.aspose.com/buy).
* Fordern Sie eine 30-tägige vorübergehende Lizenz an. Weitere Informationen finden Sie unter [Wie erhalten Sie eine vorübergehende Lizenz?](https://purchase.aspose.com/temporary-license).
* Verwenden Sie manuell einen "Try/Except"-Block auf "Scene.open/save". Diese Ausnahme ist nur eine Benachricht igung. Ignorieren Sie, dass das Laden/Speichern der Szene keinen Einfluss hat.

{{% /alert %}} 


## **Über die Lizenz**
Sie können ganz einfach eine Bewertungs version von Aspose.3D für Python via .NET von seinem herunter laden[Seite herunter laden](https://pypi.org/project/aspose.3d/). Die Bewertungs version liefert absolut**Die gleichen Fähigkeiten**Als lizenzierte Version von Aspose.3D. Darüber hinaus wird die Bewertungs version einfach lizenziert, nachdem Sie eine Lizenz erworben und ein paar Code zeilen hinzugefügt haben, um die Lizenz anzuwenden.

Die Lizenz ist eine Klartext-XML-Datei, die Details wie den Produktnamen, die Anzahl der Entwickler, für die sie lizenziert ist, das Ablaufdatum des Abonnements usw. enthält. Die Datei ist digital signiert, ändern Sie die Datei also nicht. Selbst ein versehen tliches Hinzufügen eines zusätzlichen Zeilen umbruchs zum Inhalt der Datei ungültig.

Um die mit der Bewertungs version verbundenen Einschränkungen zu vermeiden, müssen Sie vor der Verwendung eine Lizenz festlegen**Aspose.3D**. Sie müssen nur einmal pro Antrag oder Prozess eine Lizenz festlegen.

## Kaufte Lizenz

Nach dem Kauf müssen Sie die Lizenz datei oder den Stream anwenden. Dieser Abschnitt beschreibt Optionen, wie dies getan werden kann, und kommentiert auch einige häufig gestellte Fragen.

{{% alert color="primary" %}}

Sie müssen die Lizenz festlegen:
* Nur einmal pro Anwendungs domäne
* Vor der Verwendung anderer Aspose.3D Klassen

{{% /alert %}}

{{% alert color="primary" %}}

Preis informationen finden Sie auf der[„ Preis informationen“](https://purchase.aspose.com/pricing/3d/family)Seite.

{{% /alert %}}

### **Einstellen einer Lizenz in Aspose.3D für Python via .NET**

Lizenzen können von verschiedenen Standorten aus angewendet werden:

* Expliziter Weg
* Der Ordner mit dem Python-Skript, der Aspose.3D für Python via .NET aufruft
* Stream
* Als gemeerte Lizenz-ein neuer Lizenzierung mechanismus

{{% alert color="primary" %}}

Verwenden Sie die Methode `set_license`, um eine Komponente zu lizenzieren.

Das mehrfache Anrufen von `set_license` ist nicht schädlich, es verschwendet nur Prozessor zeit.

{{% /alert %}}

In den folgenden Abschnitten beschreiben wir die beiden gängigen Methoden zum Einstellen der Lizenz.

#### **Anwenden einer Lizenz mithilfe einer Datei**
Die einfachste Methode zum Festlegen einer Lizenz erfordert, dass Sie die Lizenz datei in demselben Ordner platzieren, der das Python-Skript enthält, das Aspose.3D für Python aufruft, und nur den Dateinamen ohne seinen Pfad angeben.

Dieses Code-Snippet wird verwendet, um eine Lizenz datei festzulegen:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

Wenn Sie die Methode `set_license` aufrufen, sollte der Lizenz name mit dem Ihrer Lizenz datei übereinstimmen. Sie können beispiels weise den Namen der Lizenz datei in "Aspose.3D.lic. xml" ändern. Dann müssen Sie in Ihrem Code den neuen Lizenz namen (Aspose.3D.lic.xml) an die SetLicense-Methode weitergeben.

#### **Anwendung einer Lizenz aus einem Stream**
Sie können eine Lizenz aus einem Stream laden.

Dieses Code-Snippet wird verwendet, um eine Lizenz aus einem Stream anzuwenden:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license(stream)
```

#### Metered Lizenz anwenden

Mit Aspose.3D können Entwickler einen gemetzten Schlüssel anwenden. Dies ist ein neuer Lizenz mechanismus.

Der neue Lizenzierung mechanismus wird zusammen mit der bestehenden Lizenzierung methode verwendet. Diejenigen Kunden, die aufgrund der Verwendung von API-Funktionen abgerechnet werden möchten, können die gemessene Lizenzierung nutzen.

Nachdem Sie alle erforderlichen Schritte abgeschlossen haben, um diese Art von Lizenz zu erhalten, erhalten Sie die Schlüssel, nicht die Lizenz datei. Dieser Messschlüssel kann mit der speziell für diesen Zweck eingeführten Klasse `Metered` angewendet werden.

Das folgende Code beispiel zeigt, wie gemetzte öffentliche und private Schlüssel festgelegt werden:

```py
import aspose.threed as a3d

# Create an instance of CAD Metered class
metered = a3d.Metered()

# Access the set_metered_key property and pass public and private keys as parameters
metered.set_metered_key("*****", "*****")

# Get metered data amount before calling API
amountbefore = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed Before: " + str(amountbefore))

# Load the scene from disk.
scene = a3d.Scene.from_file("3D Model.fbx")
# Save as pdf
scene.save("out_pdf.pdf", a3d.FileFormat.PDF)

# Get metered data amount After calling API
amountafter = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed After: " + str(amountafter))
```

{{% alert color="primary" %}}

Bitte beachten Sie, dass Sie für die korrekte Nutzung der Metered-Lizenz über eine stabile Internet verbindung verfügen müssen, da der Metered-Mechanismus die ständige Interaktion mit unseren Diensten für korrekte Berechnungen erfordert. Weitere Einzelheiten finden Sie in der[„ Gezählte Lizenzierung FAQ“](https://purchase.aspose.com/faqs/licensing/metered)Abschnitt.

{{% /alert %}}



