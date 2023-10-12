---
title: "Das Datengerüst in der Variablenansicht"  # Titel der Seite
weight: 202  # Individuelles Gewicht 
menuTitle: "Variablenansicht" # Falls Titel zulang ist, hier Kurztitel
tags: ["Datengerüst" , "Variablenansicht", "Primärdaten", "Dateneingabe"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

{{% buttonGit href="https://bmc.link/bpkleerw" icon="fa-solid fa-beer-mug-empty" %}} {{% /buttonGit %}}

Bevor wir nun die einzelnen Variablen eingeben, erstellen wir das Datengerüst in SPSS. 

Variablen können verschiedene Eigenschaften haben. Dazu bietet das SPSS **Datenfenster** eine umfassende Ansicht. Du kannst sie jederzeit hinzufügen und verschieben. Für deine eigene Übersicht ist es aber besser, wenn du das in einer sinnvollen Reihenfolge machst.

Wie du dem Video entnehmen kannst, können wir, nachdem wir auf **Variablenansicht** geklickt haben, zu jeder Variable diverse Informationen eingeben. Wir machen dies beispielhaft an den vier vorher genannten Variablen: `ID`, `Geschlecht`, `Alter`, `Haushaltseinkommen` und `Zufriedenheit mit der Demokratie`. Schau dir dazu noch einmal das Codebuch an. Wie wurden diese Variablen in der Variablenansicht umgesetzt?

![Datengrüst](../gif/variablenansicht.gif)

{{% expand \"Warum wurde bei der Variable `ID` die Dezimalstellen auf `0`gesetzt?\" %}}
Es gibt keine halben, viertel oder achtel Fälle. Daher brauchen wir keine Dezimalstellen. Immer, wenn wir keine Dezimalstellen brauchen, ist es eleganter, diese dann auch auf `0`zu setzen.
{{% /expand %}}

{{% expand \"Warum hat SPSS bei der Variable `gndr`das Messniveau automatisch auf *nominal* eingestellt?\" %}}
Da das Geschlecht hier nicht mit Zahlen, sondern mit Buchstaben eingetragen wird, definieren wir diese Variable als *Zeichenfolge*. SPSS geht bei Buchstaben nicht davon aus, dass diese in eine sinnvolle Reihenfolge geordnet werden können. Deshalb legt SPSS automatisch das Messniveau auf *nominal* fest.
{{% /expand %}}

{{% expand \"Welches Messniveau könnten wir bei der Variable `age` zusätzlich eintragen?\" %}}
Das Alter ist eine metrische Variable, siehe unten.
{{% /expand %}}

{{% expand \"Warum reicht es, wenn wir bei der Variable `stfdem`nur die Ausprägungen `0`und `10`definieren?\" %}}
Ist der Variablentyp numerisch, sortiert SPSS automatisch die Zahlen entsprechend ihrer Reihenfolge. Achtung: Das macht SPSS auch bei nominalen Variablen. Lasst euch dadurch nicht aus dem Konzept bringen! In diesem Fall aber können wir das nutzen: Auch wenn wir nicht jeder Zahl ein empirisches Relativ zugeordnet haben, sortiert SPSS diese automatisch in die richtige Reihenfolge.
{{% /expand %}}

{{% expand \"Warum müssen wir die `-9`sowohl bei `Werte` definieren, als auch bei `Fehlend`?\" %}}
Bei der Spalte `Werte`definieren wir, dass immer dann, wenn eine befragte Person die Antwort auf die Frage verweigert hat, diesem Fall der Wert  `-9`zugeordnet wird. Das reicht für SPSS aber nicht. SPSS ist nur durch den zusätzlichen Eintrag in die Spalte `Fehlend` klar, dass es sich hierbei um einen durch die User:innen festgelegten fehlenden Wert handelt. 
{{% /expand %}}

Hier nochmals die Auflistung der Eigenschaften von Variablen in SPSS:

1. **Variablenname**. Dies ist wichtig, da dieser später genutzt wird, um die Variable in Funktionen aufzurufen. Es gibt verschiedene Konventionen, wichtig ist aber, dass dieser nicht zu lang oder kompliziert ist (am besten nur Kleinbuchstaben).

1. **Variablentyp**. Hier legen wir die Art der Daten dieser Variable fest, damit SPSS diese korrekt lesen kann. Wenn wir die Merkmale einer Variable nur mit Zahlen beschreiben wollen, verwenden wir den Typ **numerisch**. Hier ist SPSS darauf eingestellt, nur Zahlen zu lesen. Es kann aber sein, dass wir die Merkmale einer Variable in Textform speichern wollen. Zum Beispiel, wenn wir bei einer deutschlandweiten Erhebung das Bundesland jeder Befragten in unseren Datensatz aufnehmen wollen. Hier verwenden wir den Variablentyp **Zeichenfolge**.

1. **Spaltenformat** legt fest, wie viele Zeichen (das können Zahlen, Buchstaben oder Sonderzeichen sein) die Werte umfassen, die in einer Variable eingegeben werden. 

1. **Dezimalstellen** legt fest, wie viele Zeichen für Nachkommastellen vorgesehen sind.

1. **Beschriftung** beschreibt die Variablen ausführlicher. Hier ist es wichtig, intersubjektiv nachvollziehbar die Variable zu beschreiben, damit du auch später weißt, was die Variable erhoben hat.

1. **Werte**, hier können die kodierten Werte eingesehen werden.

1. **Fehlende Werte**, das sind Kodierungen, die in Wirklichkeit keine gültigen Antworten/Daten repräsentieren.

Weiterhin gibt es einige Einstellungen, die wir vornehmen könnnen, aber keine relevanten Bedeutungen für unsere Analysen haben. Dazu gehören:

1. **Spalten** legt fest, wie breit eine Spalte in der Datenansicht dagestellt wird.

1. **Ausrichten** legt die Ausrichtung in der Datenansicht fest. Die Daten können linksbündig, rechtsbündig oder in der Mitte der Zelle dargestellt werden.

1. **Maß** legt das Skalenniveau der Variablen fest. 

1. Bei **Rolle** kann für spezielle Analysezwecke die Wirkungsweise der Variablen für künfite Analysen vordefiniert werden. Die Rollenzuweisung betrifft nur ein paar Dialogfelder, die Rollen unterstützen.

Nachdem wir nun das Datengerüst festgelegt haben, können wir im nächsten Schritt die Daten eingeben.