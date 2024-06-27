---
title: Licensing
type: docs
weight: 60
url: /de/java/licensing/
description: Sie können einfach Aspose.3D for Java aus Aspose Repository herunter laden/installieren. Der Bewertungs download entspricht dem gekauften Download. Die Bewertungs version wird einfach lizenziert, wenn Sie einige Code zeilen hinzufügen, um die Lizenz anzuwenden.
---
##  **Bewerten Aspose.3D**
Sie können einfach Aspose.3D for Java von [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) herunter laden/installieren. Der Bewertungs download entspricht dem gekauften Download. Die Bewertungs version wird einfach lizenziert, wenn Sie einige Code zeilen hinzufügen, um die Lizenz anzuwenden.

Die Bewertungs version bietet alle Funktionen mit Ausnahme der folgenden:

- Benutzer können nur maximal 50 3D-Dokumente in eine Szene öffnen/importieren.
- Benutzer können nur maximal 50 3D-Dokumente in einer Szene speichern.
- Benutzer sehen auch ein Bewertungs wasser zeichen in den gerenderten Bildern und allen anderen Ausgabe dateien.
- Jeder Knoten kann nicht mehr als 5 unter geordnete Knoten haben.
- Jeder Knoten kann nicht mehr als 2 angehängte Entitäten haben.
- Jede Geometrie kann nicht mehr als 2 angehängte Scheitel punkt elemente haben.
- Jeder Knoten kann nicht mehr als 1 Material haben.

{{% alert color="primary" %}} 

Wenn Sie Aspose.3D ohne eine ordnungs gemäße Lizenz verwenden, kann ein**com.aspose.threed.TrialException**Wenn die Nutzung die nicht lizenzierten Einschränkungen erreicht hat, können Sie die Ausnahme deaktivieren, indem Sie:

* [Kaufen Sie eine voll ausgestattete Lizenz](https://purchase.aspose.com/buy).
* Fordern Sie eine 30-tägige Lizenz an, siehe [Wie bekomme ich eine vorübergehende Lizenz?](https://purchase.aspose.com/temporary-license) Weitere Informationen.
.
* Rufen Sie `com.aspose.threed.TrialException.setSuppressTrialException(true)` vor Ihren `open`/`save`-Methoden an, die `TrialException` werden während des `open`/`save`-Anrufs auf der Szene nicht erhöht, aber die oben genannten Einschränkungen werden nicht aufgehoben.
* Verwenden Sie manuell einen `try/catch`-Block auf `Scene.open/save`. Diese Ausnahme ist nur eine Benachricht igung. Ignorieren Sie, dass das Laden/Speichern der Szene keine Auswirkungen hat.

{{% /alert %}} 
##  **Eine Lizenz beantragen**
Die Lizenz ist eine einfache XML-Datei, die Details wie den Produktnamen, die Anzahl der Entwickler, für die sie lizenziert ist, das Ablaufdatum des Abonnements usw. enthält. Die Datei ist digital signiert. Ändern Sie die Datei daher nicht. Selbst wenn versehen tlich ein zusätzlicher Zeilen umbruch in die Datei hinzugefügt wird, wird diese ungültig. Sie müssen eine Lizenz festlegen, bevor Sie Operationen mit Dokumenten ausführen. Stellen Sie sicher, dass Sie dies tun, bevor Sie ein Scene-Objekt erstellen.

Lizenzen können von verschiedenen Standorten aus angewendet werden:

- Expliziter Weg
- Der Ordner, der die JAR-Datei Aspose.3D enthält.
- Eine eingebettete Ressource in der JAR mit der Bezeichnung Aspose.3D JAR.

Verwenden Sie die `License.setLicense`-Methode, um die APIs zu lizenzieren. Oft ist der einfachste Weg, eine Lizenz festzulegen, die Lizenz datei in den gleichen Ordner wie Aspose.3D JAR zu legen und nur den Dateinamen ohne Pfad anzugeben.
###  **Lizenz mit Datei oder Stream-Objekt anwenden**
In diesem Beispiel versucht Aspose.3D, die Lizenz datei in dem Ordner zu finden, der die JARs Ihrer Anwendung enthält.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingFile.java" >}}

Initial isiert eine Lizenz aus einem Stream.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingStreamObject.java" >}}
###  **Einschl ießlich der Lizenz datei als eingebettete Ressource**
Sie können die LIC-Datei einfach in den Ordner `resources` Ihres Projekts kopieren. Der Wiederaufbau des Projekts sollte die einbetten. Lic-Datei in die Anwendung. Jar-Datei. Danach können Sie die Lizenz anwenden, indem Sie den folgenden Code verwenden:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-FileAsEmbeddedResource.java" >}}
###  **Validieren Sie die Lizenz**
Es ist möglich zu überprüfen, ob die Lizenz ordnungs gemäß eingestellt wurde oder nicht. Die Lizenz klasse verfügt über das Feld isLicensed, das true zurückgibt, wenn die Lizenz ordnungs gemäß eingestellt wurde.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ValidateLicense.java" >}}
##  **Metered Lizenz anwenden**
Aspose.3D ermöglicht es Entwicklern, einen gemetzten Schlüssel anzuwenden. Es ist ein neuer Lizenzierung mechanismus. Der neue Lizenzierung mechanismus wird zusammen mit der bestehenden Lizenzierung methode verwendet. Kunden, die basierend auf der Nutzung der API-Funktionen in Rechnung gestellt werden möchten, können die gemeerte Lizenzierung verwenden. Weitere Informationen finden Sie im Abschnitt [Gezählte Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered).

Eine neue Klasse `Metered` wurde eingeführt, um den gemetzten Schlüssel anzuwenden. Im Folgenden finden Sie den Beispielcode, der zeigt, wie der gemetzte öffentliche und private Schlüssel festgelegt wird.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-PublicAndPrivateKeys.java" >}}
##  **Wann eine Lizenz anzuwenden ist**
Befolgen Sie diese einfachen Regeln:

- Die Lizenz muss nur einmal pro Anwendungs domäne festgelegt werden.
- Sie müssen die Lizenz festlegen, bevor Sie andere Aspose.3D Klassen verwenden.
- License anrufen. Mehrmalige Set License ist nicht schädlich, sondern verschwendet einfach Prozessor zeit.

Wenn Sie eine Klassen bibliothek entwickeln, können Sie License.SetLicense von einem statischen Konstruktor Ihrer Klasse aufrufen, der Aspose.3D verwendet. Der statische Konstruktor wird ausgeführt, bevor eine Instanz Ihrer Klasse erstellt wird, um sicher zustellen, dass die Lizenz für Aspose.3D richtig eingestellt ist.
##  **Sie können den Namen der Lizenz datei ändern**
Der Name der Lizenz datei muss nicht 'Aspose.3D.LIC' sein. Sie können es in alles umbenennen, was Sie mögen, und diesen Namen verwenden, wenn Sie License.SetLicense aufrufen.
##  **Ausnahme Lizenz dateiname kann nicht gefunden werden**
Wenn Sie eine Lizenz kaufen und herunter laden, nennt die Website Aspose die Lizenz datei `Aspose.3D.LIC`. Sie laden die Lizenz datei mit Ihrem Browser herunter. Einige Browser erkennen die Lizenz datei als XML und hängen eine an. Xml-Erweiterung, damit der vollständige Name der Datei auf Ihrem Computer `Aspose.3D.lic.XML` wird.

Wenn Microsoft Windows zum Beispiel so konfiguriert ist, dass Erweiterungen bekannter Dateitypen ausgeblendet werden (leider ist dies bei den meisten Windows Installationen standard mäßig), erscheint Ihnen die Lizenz datei als `Aspose.3D.LIC` im Windows Explorer. Sie werden wahr schein lich denken, dass dies der echte Dateiname ist, und rufen Sie Lizenz an. SetLicense gibt es `Aspose.3D.LIC`, aber es gibt keine solche Datei, daher die Ausnahme.

Um das Problem zu lösen, benennen Sie die Datei um, um das Unsichtbare zu entfernen. Xml-Erweiterung. Wir empfehlen Ihnen außerdem, die Option "Erweiterungen ausblenden" in Microsoft Windows zu deaktivieren.

##  **Verwenden mehrerer APIs ab Aspose**
Wenn Sie mehrere Aspose-APIs in Ihrer Anwendung verwenden, z. B. Aspose.3D und Aspose. Zellen, hier sind einige nützliche Tipps.

- Legen Sie die Lizenz für jede Aspose API separat fest. Selbst wenn Sie eine einzige Lizenz datei für alle APIs haben, z. B. `Aspose.Total.lic`, müssen Sie `License.setLicense` für jede Aspose API, die Sie in Ihrer Bewerbung verwenden, separat anrufen.
- Verwenden Sie den Namen der voll qualifizierten Lizenz klasse. Jeder Aspose API hat eine Lizenz klasse in seinem Namens raum. Zum Beispiel hat Aspose.3D `com.aspose.3d.License` und Aspose.Cells hat `com.aspose.cells.License` Klasse. Durch die Verwendung des voll qualifizierten Klassen namens können Sie Verwirrung darüber vermeiden, welche Lizenz für welches Produkt angewendet wird.
