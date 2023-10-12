---
title: "Basics"  # Titel der Seite
menuTitle: "Basics" # Falls Titel zulang ist, hier Kurztitel
weight: 101  # Individuelles Gewicht 
tags: ["Datei", "Dateimanagement", "Dateipfad"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonShare href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonShare %}} 

{{% buttonShare href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonShare %}}

{{% buttonShare href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonShare %}}

{{% buttonShare href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonShare %}}

{{% buttonShare href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonShare %}}

{{% buttonShare href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonShare %}}

{{% button href="https://bmc.link/bpkleerw" icon="fa-solid fa-beer-mug-empty" %}} {{% /button %}}

In der praktischen Datenanalyse, in der wir Berechnungen nicht händisch durchführen (wie z. B. in der Vorlesung zu Statistik), nutzen wir die Rechenleistung eines Computers, um Daten zu bearbeiten, einfache Berechnungen oder auch kompliziertere statische Modelle zu berechnen. Wir verwenden dabei Daten, die wir in Dateien gespeichert haben. Doch was sind eigentlich nochmal Dateien und wie lassen sich diese finden?

**Daten** werden in der Regel als **Dateien** an einem *lokalen* Ort auf dem Computer (Desktop oder Laptop) oder Tablet gespeichert. *Lokal* meint dabei, dass die Dateien physisch auf deinem Rechner abgelegt sind. Das Gegenteil sind Dateien, die zum Beispiel in einer Cloud (wie der Hessenbox) gespeichert sind und nur temporär bei der Bearbeitung der Dateien lokal gespeichert werden.

Dateien haben immer eine Endung, die den Typ der Datei festlegt. So haben Word-Dokumente in der Regel die Endung *.docx* bzw. Powerpoint-Dateien die Endung *.pptx*. Auch Bilddateien haben festgelegte Endungen wie *.jpg* oder *.png*. Die Endung einer Datei gibt Aufschluss, wie diese Datei zu lesen ist, bzw. mit welchem Programm die Datei geöffnet wird. Dies ist meist in den automatischen Einstellungen (in Windows oder Mac) festgelegt.

Eine zweite Information, die wir über Dateien benötigen, wenn wir mit diesen arbeiten möchten, ist der *Pfad*. Der *Pfad* ist sozusagen die Wohnadresse der Datei. Jede Datei ist an einem bestimmten lokalen Ort gespeichert und dazu gibt es immer eine eindeutige Adresse, mit der die Datei ansprechbar bzw. auffindbar ist. Das ist auf dem Tablet eventuell schwer nachvollziehbar, am Desktop/Laptop wird dies aber schnell klar.

Ich habe zum Beispiel die Datei **syllabus.pdf** (Kursplan dieses Kurses) lokal auf meinem Computer gespeichert. Doch wie finden wir heraus, wo wir die Datei gespeichert haben?

Der erste Schritt ist sicher im Finder (Mac) oder Explorer (Windows) danach zu suchen. Haben wir die Datei gefunden, können wir auch den eindeutigen Pfad anzeigen lassen.

Auf dem Mac-Rechner sieht das wie folgt aus: ![Beispiel Pfad](../img/path.png)

Analog sieht es auf dem Windows-Rechner wie folgt aus: ![Beispiel Pfad Win](../img/path-win.png)

Die Adresse der Datei ist nicht unbedingt direkt sichtbar. Sie befindet sich bei Mac am unteren Ende des Fensters bzw. bei Windows am oberen Ende des Fenster. Durch Rechtsklick kann man aus dem Finder als auch dem Explorer den Pfad kopieren und hat somit die eindeutige Adresse einer Datei.

Auf dem Mac-Rechner ist die Adresse (Pfad) im Beispiel:

    /Users/jlug/Documents/Teaching/syllabus.pdf

Auf dem Windows-Rechner ist die Adresse (Pfad) im Beispiel:

    D:\g31442\Teaching\syllabus.pdf

Einen wichtigen Unterschied sehen wir jetzt hier schon. Bei Windows-Rechnern mit deutscher Spracheinstellung wird ein Backslash `\` zur Unterscheidung von Ordnern genutzt, bei Mac-Rechnern ein einfacher Slash `/`. Das liegt an den Spracheinstellungen meines Windows-Rechners, der auf eine deutsche Systemsprache eingestellt ist. Für SPSS ist es jedoch egal, ob du den Dateipfad mit einfachen Slash oder Backslash angibst. Es ist wichtig, dass du diesen ersten Schritt verstanden hast. Am besten probierst du einmal selbst aus, den Dateifpad von einer beliebigen Datei in ein Word-Dokument zu kopieren. Aus den Pfaden heraus lassen sich die Datendateien öffnen bzw. die Dateien aus SPSS speichern.
