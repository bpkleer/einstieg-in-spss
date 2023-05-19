---
title: "Import von .txt und .csv"  # Titel der Seite
weight: 102  # Individuelles Gewicht 
menuTitle: "Text-Import" # Falls Titel zulang ist, hier Kurztitel
tags: ["Daten", "Dateiendungen", ".txt", ".csv", "Datenimport", "GET DATA"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Als erstes werden wir globale Datensatz-Dateiformate importieren. Dies sind `.txt` und `.csv` wie du auf der letzten Seite sehen konntest. 

{{%attachments style=\"grey\" title=\"Datensatz\" /%}}

Bevor du dich mit den Datenimport befasst, ist es wichtig, dass du dir die Datensätze genauer anschaust. Lade sie dafür herunter und öffne sie im Editor. Achte auf folgende Besonderheiten:

1. Welches Zeichen trennt die Variablen? Tabulator `tab`, Semikolon `;` oder Komma `,`?

1. Durch welches Zeichen wird Text gekennzeichnet? Hochkommata `'` oder Anführungszeichen `"` oder gibt es so ein Zeichen gar nicht?

1. Durch welches Zeichen werden Dezimalzahlen gekennzeichnet? Durch einen Punkt`.`oder Komma `,`?

1. In welcher Zeile ist der erste Fall? 

1. Gibt es eine Spalte mit den Variablennamen?

## Import einer .txt-Datei

Eine `.txt`-Datei ist eine reine Textdatei, in der Daten mit einem Tabulator getrennt sind (siehe Screenshot). Auch hier ist das Format in der Konvention, dass in der Spalte Variablen eingetragen sind und in den Zeilen die Fälle. In der Regel stellt die erste Zeile keinen Fall dar, sondern beinhaltet wie im Beispiel die Variablennamen. Schau dir den Screenshot an und mach dir Notizen zu den wichtigsten Eigenschaften dieser Datei entsprechend den oben genannten Stichpunkten.

![Beispiel .txt-Datei](../img/txt.png)
Im Beispiel haben wir also einen Datensatz mit vier Variablen: `age`, `duration`, `grade` und `exam`. 

{{% expand \"Überlege einmal kurz, was die Variablen wohl bedeuten könnten?\" %}}
In der Regel versuchen Forschende Variablen möglichst eindeutig zu benennen. **age** beinhaltet das Alter der Befragten, **duration** die Zeitdauer, die die Person für die Prüfung benötigt hat, **grade** die Note, die die Person in der jeweiligen Prüfung erhalten hat und **exam** beinhaltet, um welche Prüfung es sich handelt. 
{{% /expand %}}

Wie immer hast du bei SPSS die Möglichkeit das über einen Klickweg oder über die Syntax zu lösen. Wenn du Dateien mit der Syntax in SPSS einlesen lassen möchtest, musst du dir in Erinnerung rufen, was ein Dateipfad ist. Wenn du das nicht mehr weißt, geh zurück in den [Lernblock 1](https://lehre.bpkleer.de/statsplus/lb1). Vergewissere dich ebenso, wenn du die Daten über den Klickweg importieren willst, wo du deine Daten gespeichert hast.

{{< tabs groupId="txt" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/txt.gif)

Der Datenimport ist einer der wenigen Fälle, bei denen der Klickweg wohl bequemer ist als die Syntax.
{{% /tab %}}
{{% 

tab name="Syntax" %}}
```{SPSS}
GET DATA /TYPE=TXT
 /FILE="Z:/Hier_muss_Dein_Dateipfad_stehen.txt"
 /ENCODING='UTF8'
 /DELCASE=VARIABLES 4
 /DELIMITERS="\t"
 /ARRANGEMENT=DELIMITED
 /FIRSTCASE=2
 /DATATYPEMIN PERCENTAGE=95.0
 /VARIABLES=
 age AUTO
 duration AUTO
 grade AUTO
 exam AUTO
 /MAP.
```
Wie du siehst ist das ein ziemlich langer Befehl. Fassen wir in Kürze die wichtigsten Punkte zusammen.

`GET DATA` ist der Hauptbefehl. Ihn wirst du in diesem Kapitel häufig sehen. Er sagt SPSS, dass es Daten importieren soll.

`/TYPE` ist der Unterbefehl der SPSS klar macht, welcher Dateityp importiert werden soll. Bei Datentabellen mit der Endung `.txt`musst du hier `TXT`eintippen.

`/FILE` verweist auf den Speicherort, wo SPSS die Daten finden kann.

Hier folgen noch einige Befehle, die den einzelnen Klickstationen auf dem Klickweg entsprechend. Mit `/DELCASE` erklärst du SPSS, dass ein Fall (englisch *CASE*) vier Variablen entspricht. Unter `/DELIMITERS` wird das Trennzeichen definiert. Hier ist es durch `"\t"` der Tabulator. Das letzte, was wichtig ist, ist der `/FIRSTCASE=2`Befehl. Er macht klar, dass der erste Fall in der zweiten Zeile zu finden ist. Denn in der ersten Zeile befinden sich ja die Variablennamen!

{{% /tab %}}
{{% tab name="Ergebnis Datenansicht" %}}

![Ergebnis](../img/ergebnisdaten.png)

{{% /tab %}}
{{% tab name="Ergebnis Variablenansicht" %}}

![Ergebnis](../img/ergebnisvariablen.png)

{{% /tab %}}
{{< /tabs >}}

Wenn du einmal den Datenimport von `.txt`-Dateien verstanden hast, findest du den Datenimport von `.csv`-Dateien sicher leicht. Schauen wir uns das als nächstes an.

## Import einer .csv-file

Schau dir hier die *csv*-Datei im Editor an. Mach dir auch hierzu Stichpunkte zu den wichtigsten Eigenschaften. Was fällt dir im Unterschied zur *txt*-Datei auf?

![csv](../img/csv.png)

Um eine *.csv-file* zu laden, wenden wir einen einfacheren Klickweg an. Die Syntax sieht ähnlich aus.

{{< tabs groupId="csv" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/csv.gif)

{{% /tab %}}
{{% tab name="Syntax" %}}

```{SPSS}
GET DATA /TYPE=TXT
 /FILE="Z:/Hier_muss_Dein_Dateipfad_stehen.csv"
 /ENCODING='UTF8'
 /DELIMITERS=","
 /QUALIFIER='"'
 /ARRANGEMENT=DELIMITED
 /FIRSTCASE=2
 /DATATYPEMIN PERCENTAGE=95.0
 /VARIABLES=
 V1 AUTO
 age AUTO
 duration AUTO
 grade AUTO
 exam AUTO
 /MAP.
```
Schau dir die Syntax an. Was fällt dir im Vergleich zur Syntax für *.txt-files* auf?

{{% /tab %}}
{{% tab name="Ergebnis Datenansicht" %}}

![Ergebnis](../img/csvdaten.png)

{{% /tab %}}
{{% tab name="Ergebnis Variablenansicht" %}}

![Ergebnis](../img/csvvariablen.png)

{{% /tab %}}
{{< /tabs >}}

Ein kleines Quiz zur Syntax von *csv-files*.

{{% expand \"Was bedeutet das Komma `,` bei DELIMITERS?" %}}
Hier definierst du das Trennzeichen zwischen den Variablen. Hier ist das ein Komma `,`.
{{% /expand %}}

{{% expand \"Was bedeutet der Befehl `/QUALIFIER`" %}}
Das erkennst du am Zeichen, was angegeben ist. Das Anführungszeichen `"` markiert Text in der .csv Datei. Hier definierst du also, wo SPSS in der Datendatei einen Text lesen soll.
{{% /expand %}}

{{% expand \ "Welche Funktion hat die Variable `V1`" %}}
Der Datensatz enthält eine ID-Variable. Sie wurde von SPSS als `V1` benannt. 
{{% /expand %}}
