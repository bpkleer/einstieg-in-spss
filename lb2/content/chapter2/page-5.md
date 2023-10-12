---
title: "Streumaße"  # Titel der Seite
weight: 205  # Individuelles Gewicht 
menuTitle: "Streumaße" # Falls Titel zulang ist, hier Kurztitel
tags: ["Univariate Statistik", "Streumaße", "DESCRIPTIVES", "FREQUENCIES"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonShare href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonShare %}} 

{{% buttonShare href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonShare %}}

{{% buttonShare href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonShare %}}

{{% buttonShare href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonShare %}}

{{% buttonShare href="https://twitter.com/share?url=" icon="fab fa-x-twitter" %}} {{% /buttonShare %}}

{{% buttonShare href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonShare %}}

{{% button href="https://bmc.link/bpkleerw" icon="fa-solid fa-beer-mug-empty" %}} {{% /button %}}

## Grundlegende Kenngrößen der Streumaße

Die meisten Streumaße beziehen sich auf das **arithmetische Mittel**. Sie geben relativ zum arithemtischen Mittel an, wie weit alle Fälle im Durchschnitt vom Mittelwert abweichen. Weil das arithemtische Mittel eine wichtige Voraussetzung ist, benötigst du für Streumaße streng genommen mindestens das **metrische Skalenniveau**.

1. Die **Varianz** beschreibt, wie die Fälle um den Mittelwert *variieren*. 

1. Die **Standardabweichung** ist die Quadratwurzel der Varianz. Sie beschreibt ebenso wie die Varianz, wie die Fälle um dem Mittelwert variieren. Du kannst die Standardabweichung mit der ursprünglichen Einheit deiner Variable interpretieren. Eine Standardabweichung von 400 bei einem durchschnittlichen Einkommen von 2000€, bedeuetet also, dass die durchschnittliche Abweichung der Befragten zum Mittelwert 400€ beträgt.

Weiterhin gibt es noch Streumaße, die die kleinste und die größte realisierte Ausprägung beschreiben.

1. Das **Minimum** ist die kleinste realisierte Ausprägung.

1. Das **Maximum** ist die größte realisierte Ausprägung.

## Streumaße mit dem `DESCRIPTIVES`-Befehl

Wir können uns Streumaße wie Lagemaße ausgeben. Es ändern sich nur die *Parameter*. 

{{< tabs groupId="desc_lage" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/descriptives2.gif)


{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
DESCRIPTIVES VARIABLES=trstplt
  /STATISTICS=STDDEV VARIANCE MIN MAX.
```
Den Haupt- und Unterbefehl kennen wir ja schon. Die Parameter lauten für die **Standardabweichung** `STDDEV`, für die **Varianz** `VARIANCE`, für das **Minimum** `MIN` und für das **Maximum** `MAX`.

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/descriptives2.png)

Das Minimum beträgt 0, das Maximum 10. Die Standardabweichung beträgt 1,882, die Varianz 3,541


{{% /tab %}}
{{< /tabs >}}

## Streumaße mit dem `FREQUENCIES`-Befehl

Auch beim `FREQUENCIES`-Befehl ändern sich nur die Parameter, easy. 

{{< tabs groupId="freq_lage" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/statistics2.gif)


{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
FREQUENCIES VARIABLES=trstplt
  /STATISTICS=STDEV VARIANCE MIN MAX
  /ORDER=ANALYSIS.
```
Alle Befehle und Parameter kennst du bereits. So einfach kann Syntax sein. 

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/statistics2.png)

Auch hier wird dir wieder die Pivot-Tabelle und die Statistiktabelle ausgegeben werden. Die Maßzahlen und die Interpretation sind natürlich genauso wie bei der Variante mit `DESCRIPTIVES`.
{{% /tab %}}
{{< /tabs >}}

## Geht auch alles auf einmal?

Wie schön wäre es doch, wenn es einen einfachen Befehl gäbe, mit dem du bequem alle univariaten Maßzahlen auf einmal ansehen könntest. Aber den gibt es doch! Sein Syntax-Befehl `EXAMINE VARIABLES` wirkt auf den ersten Blick recht kompliziert, per Klickweg kannst du dir aber sehr einfach alle Maßzahlen anzeigen lassen.

{{< tabs groupId="examine" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/examine.gif)


{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
EXAMINE VARIABLES=wkhtot
  /PLOT NONE
  /STATISTICS DESCRIPTIVES
  /CINTERVAL 95
  /NOTOTAL.
```
Nach `EXAMINE VARIABLES` folgt die Variable, die du analyseieren willst. Einen Plot brauchen wir erstmal nicht, daher wählen wir `/PLOT NONE`. Mit `/STATISTICS DESCRIPTIVES` weiß SPSS, dass deskriptive Statistiken ausgegeben werden sollen. Nach `/CINTERVAL` folgt das Konfidenzintervall, dass du hier definieren kannst.

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/examine.png)

Hier siehst du keine Pivot-Tabelle, sondern eine Aufzählung der Maßzahlen. Das ist auch die einzige Möglichkeit den Interquartilsabstand in SPSS zu berechnen. 
{{% /tab %}}
{{< /tabs >}}

So, das war es nun zur deskriptiven Statistik. Im letzten Kapitel dieses Lernblocks lernst du noch Grafiken mit SPSS zu erstellen.