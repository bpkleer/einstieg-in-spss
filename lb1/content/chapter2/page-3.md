---
title: "Eingabe der Daten in die Datenansicht"  # Titel der Seite
weight: 203  # Individuelles Gewicht 
menuTitle: "Datenansicht" # Falls Titel zulang ist, hier Kurztitel
tags: ["Datenansicht" , "Datentabellen", "Dateneingabe", "Primärdaten", "userdefinierter fehlender Wert", "systemdefinierter fehlender Wert"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonShare href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonShare %}} 

{{% buttonShare href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonShare %}}

{{% buttonShare href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonShare %}}

{{% buttonShare href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonShare %}}

{{% buttonShare href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonShare %}}

{{% buttonShare href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonShare %}}

{{% button href="https://bmc.link/bpkleerw" icon="fa-solid fa-beer-mug-empty" %}} {{% /button %}}

Wir haben nun das Datengerüst geschaffen und machen nun mit dem zweiten Schritt weiter. Wechseln wir dafür in die **Datenanischt**.

![Wechsel in die Datenansicht](../gif/datenansicht1.gif)

{{% expand \"Warum haben die Variablen in einer Datentabelle alle dieselbe Länge?\" %}}
Alle Befragten erhalten dieselben Fragen. Selbst wenn spezifische Fragengruppen nur einem Teil der Befragten präsentiert wurden, haben die anderen Befragten auch einen Wert auf dieser Variable. Nämlich einen fehlenden Wert (`.`). Das geschieht auch, wenn Personen es ablehnen einzelne Fragen zu beantworten. 
{{% /expand %}}

## Eingabe der einzelnen Daten
Haben alle unsere Befragten den Fragebogen ausgefüllt, können wir nach Erstellung des Datengerüsts die Daten aus den Fragebögen in SPSS zu übertragen. Jeder Fragebogen stellt einen Fall dar. In der *Datenansicht* erhält jeder Fall eine eigene Zeile. Jede Spalte ist eine Variable. Diese wurde vorher in der Variablenansicht näher definiert. In jeder Zelle der Datenansicht findest du das Merkmal eines Falles für eine Variable. Um die Daten nun einzutragen, klicken wir einfach auf die Zelle, die wir ausfüllen wollen.

![Zeilen und Spalten](../img/zeilenspalten.png)

Wenn du das blaue Feld ausfüllen möchtest, musst du den dritten Fragebogen suchen (rote Zeile) und die Antwort auf die Variable `age` suchen (grüne Spalte). 

{{% expand \"In welcher Spalte auf dem Screenshot darfst du Buchstaben, Zahlen und Sonderzeichen benutzen?\" %}}
Das geht nur bei der Variable `gndr`. Das erkennst du auch an dem Icon. Numerische Variablen haben ein gelbes Lineal. Zeichenfolgevariablen werden mit drei farbigen Punkten und einem `a` gekennzeichnet. 
{{% /expand %}}

Bleibt nach dem Eintragen der Daten in die Datenansicht eine Zelle leer, füllt SPSS diese automatisch mit einem **systemdefinierten fehlenden Wert**. Diese kannst du an einem `.` (Punkt) erkennen. Du kannst die Punkte auch per Hand eintragen.

Fälle kannst du auch jederzeit hinzufügen und verschieben. Achte aber darauf, dass du nicht mit deinen Fragebögen durcheinander kommst. Nicht vergessen: Jeder Fragebogen erhält ausschließlich eine Zeile.

![Dateneingabe](../gif/dateneingabe.gif)

{{% expand \"In welcher Zelle finden wir einen systemdefinierten fehlenden Wert und in welcher Zelle finden wir einen userdefinierten fehlenden Wert?\" %}}
Den systemdefinierten fehlenden Wert findest du beim sechsten Fall bei der Variable `income`. Hier hat die Person, die das Video aufgenommen hat, wohl vergessen, die Zelle auszufüllen...
Den userdefinierten fehlenden Wert findest du beim achten Fall bei der Variable `stfdem`. Anscheinend wollte diese Person auf die Frage nicht antworten, interessant...
{{% /expand %}}

Jetzt haben wir einen ersten Datensatz erstellt, mit dem wir jetzt erste Befehle in SPSS durchführen können. Wie wir mit bereits erhobenen Daten umgehen, lernst du im [Lernmodul 2](https://lehre.bpkleer.de/statsplus).