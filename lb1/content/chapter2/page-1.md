---
title: "Daten in SPSS eingeben"
weight: 201
menuTitle: "Dateneingabe"
tags: ["Datenfenster", "Primärdaten", "Sekundärdaten", "Downloads", "Datentabelle", "Skalenniveaus"]
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Wir unterscheiden zwischen Primär- und Sekundärdaten in der empirischen Sozialforschung. Sekundärdaten sind erhobenen und bereits aufgearbeitete fertige Datensätze, die wir von anderen Forscher:innen erhalten. In SPSS bearbeitest du meistens bereits erhobene Daten, sogenannte **Sekundärdatensätze**.  Wie wir mit Sekundärdaten umgehen, wird im zweiten Lernblock dargestellt. Um aber das **Datenfenster** besser zu verstehen, wirst du auf dieser Seite die Schritte von der Datenerhebung zum Datensatz lernen. 

Wir wollen jetzt erstmal selbst einen Datensatz erstellen. Dazu gibt es zwei zentrale Schritte in SPSS. Zuerst erstellen wir eine Variablenbeschreibung in der **Variablenansicht**. Danach geben wir in der **Datenansicht** die Daten ein. In SPSS wird beides im Datenfenster dargestellt.

Im weiteren Verlauf nutzen wir einen fiktiven Trainingsdatensatz *Panem Social Survey*, der angelehnt an den [European Social Survey](https://europeansocialsurvey.com) ist. Vorteil ist, dass du erstmal mit einem deutlich kleineren Trainingsdatensatz üben kannst, bevor wir mit richtigen (größeren) Datensätzen in Präsenz arbeiten. 

Den Datensatz und das Codebook des **PSS** kannst du hier unter `pss.sav` herunterladen:

{{%attachments style=\"grey\" title=\"Data sets\" /%}}

Ebenso findest du in den Attachments eine PDF mit dem Namen `from-survey-to-data.pdf`. Lade diese herunter und schau sie dir an!

In der Datei ist ein Auszug von vier Fragen (Variablen aus dem Datensatz), die in diesem fiktiven Datensatz erhoben wurden. **Tipp:** Im Codebook erhältst du genauere Informationen zu der Art der Messung der einzelnen Variablen. 

{{% expand \"Überlege dir jetzt einmal kurz, welches Skalenniveau die einzelnen Fragen (Variablen) haben und wie du sie in der Variablenansicht umsetzen würdest. Falls du dir mit Skalenniveaus noch unsicher bist, scrolle runter und lies den Abschnitt zur Wiederholung von Skalenniveaus.\" %}}

Die ID-Frage ist auf nominalen Skalenniveau, es können lediglich Unterschiede zwischen den Ausprägungen festgestellt werden. 

Das Geschlecht wird auf nominalem Skalenniveau gemessen. 

Das Alter ist eindeutig auf metrischem Skalenniveau.

Das Haushaltseinkommen wird ordinal abgefragt. Es gibt Unterschiede zwischen den Ausprägungen und eine klare Rangfolge, die Abstände sind aber nicht gleich! 

Zuletzt wird noch die Zufriedenheit mit der Demokratie in Panem abgefragt. Dies ist eindeutig auf ordinalem Skalenniveau, da es mehr als zehn Ausprägungen sind, kann man dies auch als pseudometrisches Skalenniveau interpretieren. 
{{% /expand %}}

Wie du jetzt sicher schon verstanden hast, ist ein Datensatz nichts anderes als eine Sammlung mehrerer Variablen von befragten Personen, die zusammen verarbeitet werden. Die Informationen über die Personen werden in Tabellenform gespeichert bzw. gelesen. Diese Datentabellen haben zwei Dimensionen: **Zeilen** und **Spalten**.  

Dies können wir hier auch am fertigen Beispiel sehen. So einen Datensatz werden wir auf den nächsten Seiten Schritt für Schritt selbst erstellen. 

![Datenfenster](../img/Datenfenster.png)

{{% expand \"Was kannst du in der Tabelle erkennen? Was ist in den Spalten und was ist in den Zeilen?\" %}}
Du hast es richtig erkannt! In einer Datentabelle sind in der Spalte die Variablen abgebildet und in den Zeilen die Fälle. Eine Besonderheit ist die ersten Zeile, da diese keine Antworten enthält, sondern die Namen der Variablen!

![Zeilen und Spalten](../gif/Datenfenster.gif)
{{% /expand %}}

{{% expand \"In welchem Einkommensdezil befindet sich die Person mit der ID-Nummer 10020?\" %}}
Im 7. Dezil, richtig! In den Zellen der Datentabelle befinden sich also die entsprechenden Werte einer befragten Person zu der entsprechenden Variable. 

Prima, du kannst jetzt also eine Datentabelle bzw. einen Datensatz verstehen!
{{% /expand %}}

Du hast jetzt verstanden, wie eine Datentabelle aufgebaut ist, was sich in den Zeilen, Spalten und Zellen befindet. In den nächsten zwei Seiten werden wir nun selbst einen Datensatz erstellen. 

### Was waren Skalenniveaus nochmal?

Skalenniveau ist ein Begriff, der die Eigenschaften von Merkmalen der Variablen beschreibt. Es bestimmt, welche mathematischen Operationen mit den Variablen getätigt werden können. Kann man einen Durchschnitt aus Postleitzahlen berechnen? Das ergibt offensichtlich keinen Sinn. Welche Berechnungen wir durchführen können, hängt vom Skalenniveau der Variablen ab. Folgende Skalenniveaus sind für die Arbeit mit SPSS wichtig:

1. **Nominalskala**. Variablen haben ein nominales Skalenniveau, wenn sie unterscheidbare Merkmale haben, diese aber nicht in eine sinnvolle Rangfolge gebracht werden können. Dazu gehört zum Beispiel die Variable *Postleitzahl*.

1. **Ordinalskala**. Variablen haben ein ordinales Skalenniveau, wenn sie unterscheidbare Merkmale haben und diese auch in eine sinnvolle Rangfolge gebracht werden können. Der Bildungsabschluss ist ein gutes Beispiel: Es ist klar, dass das Abitur einen formal höheren Bildungsabschluss als die Mittlere Reife darstellt und auch, dass das Bachelorstudium einen formal höheren Bildungsabschluss als das Abitur darstellt. Bei ordinalem Skalenniveau kann diese Rangfolge zwischen Werten zwar erfolgen, aber der Abstand zwischen den Merkmalen kann nicht sinnvoll interpretierbar ist. Der Abstand zwischen Abitur und Mittlere Reife ist zum Beispiel nicht derselbe wie der zwischen Bachelorstudium und Abitur, obwohl beide direkt aufeinander folgen. 

1. **metrisches Skalenniveau**. Das ist eine Oberkategorie für die *Intervall-* und die *Verhältnisskala*. Variablen haben ein metrisches Skalenniveau, wenn sie unterscheidbare Merkmale haben, diese auch in eine sinnvolle Rangfolge gebracht werden können und der Abstand zwischen den Merkmalen interpretiert werden kann. Einkommen ist ein gutes Beispiel: Der Unterschied zwischen Person A mit 1.500 Euro und Person B mit 2.000 Euro ist derselbe wie der Abstand zwischen Person C mit 30.000 Euro und Person D mit 30.500 Euro, nämlich genau 500 Euro.