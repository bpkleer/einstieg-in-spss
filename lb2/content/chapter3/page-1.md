---
title: "Kategoriale Variable"  # Titel der Seite
weight: 301  # Individuelles Gewicht 
menuTitle: "kategoriale Variable" # Falls Titel zulang ist, hier Kurztitel
tags: ["Grafik", "Kreisdiagramm", "Säulendiagramm", "Kategoriale Variablen"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-x-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Bestimmt hast du oft das Gefühl, dass du mit den errechneten Zahlen nichts anfangen kannst. Sie sind oft nicht intuitiv interpretierbar und müssen durch viel Text erklärt werden. Daher ist es eine wichtige Kompetenz, mathemtische Ergebnisse grafisch darstellen zu können. Sie lösen das Problem. Sie sind intuitiver interpretierbarer und fassen Ergebnisse einfach zusammen. Hier lernen wir drei Grafiktypen kennen, die wir einfach in SPSS erstellen lassen können. Für **kategoriale Variablen**, also Variablen die *nominal* oder *ordinal* sind, eignet sich das **Kreisdiagramm** und das **Säulendiagramm**. Für **metrische Variablen** eignet sich das **Histogramm** gut. Ebenso können **Boxplots** die verschiedenen deskriptiven Maße bei **metrischen Variablen** gut darstellen. Wieso wir hier wieder beim Skalenniveau unterscheiden müssen, liegt an der Anlage des Diagramms. Wir gehen darauf gleich näher ein. 

## Das Kreisdiagramm 

Ein Kreisdiagramm eignet sich insbesondere für **nominale Variablen**. Hier ist den Betrachter:innen klar, dass es keine Hierarchie zwischen den Ausprägungen gibt. Prinzipiell kannst du sie aber auch für ordinale Variablen nutzen. Beim Kreisdiagramm können bis zu **sechs Ausprägungen** visualisiert werden. Hast du eine Variable mit mehr Ausprägungen, musst du diese erst zusammenfassen, z.B. mit dem [`RECODE`-Befehl](https://lehre.bpkleer.de/spss101/lb2/chapter2/page-2/).

{{< tabs groupId="Kreis" >}}
{{% tab name="Klickweg" %}}
![Pie](../gif/pie.gif)
{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
FREQUENCIES VARIABLES=gndr
  /PIECHART FREQ
  /ORDER=ANALYSIS.
```
Auch hier kannst du mit `FREQUENCIES` arbeiten. Neu ist der Unterbefehl `/PIECHART`, also Kuchendiagramm. Nach `/PIECHART`folgt der Paramter `FREQ`. Das bedeutet, dass SPSS **absolute Häufigkeiten** darstellen soll. Alternativ könntest du mit dem Paramter `PERCENT` arbeiten. Dann werden **relative Häufigkeiten** visualisiert. Beim Kreisdiagramm macht das aber keinerlei Unterschied. 
{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Pie](../img/pie.png)

In einem Kreisdiagramm (oder auch *pie chart*) können also die Anteile einzelner Ausprägungen an der Gesamtmenge schnell interpretiert werden.

{{% /tab %}}
{{< /tabs >}}

## Das Säulendiagramm 

Ein Säulendiagramm eignet sich insbesondere für **ordinale Variablen**. Oftmals wird das Säulendiagramm auch Balkendiagramm genannt (wie im SPSS-Menü). Beim Säulendiagramm werden Säulen entlang der X-Achse aufgetragen. Dadurch könnte den Betrachter:innen suggeriert werden, dass es eine Hierarchie zwischen den Ausprägung gibt. Die Höhe der Säulen kann an der Y-Achse abgelesen werden. Prinzipiell kannst du sie aber auch für nominale Variablen nutzen. Beim Säulendiagramm können bis zu **zehn Ausprägungen** dargestellt werden. 

{{< tabs groupId="Bar" >}}
{{% tab name="Klickweg" %}}
![Bar](../gif/bar.gif)
{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
FREQUENCIES VARIABLES=edu
  /BARCHART PERCENT
  /FORMAT=AVALUE
  /ORDER=ANALYSIS.
```
Auch hier kannst du mit `FREQUENCIES` arbeiten. Neu ist der Unterbefehl `/BARCHART`, also Balkendiagramm. Nach `/BARCHART` kannst du ebenfalls mit dem Parameter `FREQ` oder `PERCENT` arbeiten. Das entscheidet darüber, welche Werte auf der Y-Achse dargestellt werden sollen. Entweder **absolute Häufigkeiten** (`FREQ`) oder **relative Häufigkeiten** (`PERCENT`). Das entscheidest du, je nach Forschungsinteresse. An der dargestellten Höhe der Balken ändert dieser Parameter jedoch nichts.

Du kannst hier auch einstellen, in welcher Reihenfolge die Balken dargestellt werden sollen. Das macht `/FORMAT`. SPSS bietet vier Möglichkeiten. `DFREQ` sortiert die Balken **absteigend nach Häufigkeit** (also Höhe der Balken). Der größte Balken ist also rechts, der kleinste links. `AFREQ` sortiert die Balken **aufsteigend nach Häufigkeit**. Der größte Balken ist hier links, der kleinste rechts. Diese beiden Einstellungen sollten nur für nominale Variablen genutzt werden. Bei ordinalen Variablen sollte die Ordnung der Ausprägungen berücksichtigt werden!

`DVALUE` sortiert die Balken **absteigend nach Codewert**. Der höchste Code ist also links, der kleinste rechts. `AVALUE`sortiert die Balken **aufsteigend nach Codewert**. Der kleinste Code ist also links, der größte ist rechts. Sofern eine Ordnung in der Variable vorliegt, sollte diese auch so dargestellt werden und aufsteigend nach Codewert sortiert werden (`AVALUE`).
{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Bar](../img/bar.png)

Beachte vor der Interpretation des Balkendiagrammes immer die Y-Achse und die X-Achse. Werden Prozentwerte oder absolute Häufigkeiten gezeigt? Wie sind die Balken geordnet?

{{% /tab %}}
{{< /tabs >}}

Gehen wir nun auf der nächsten Seite weiter zur Darstellung metrischer Variablen.