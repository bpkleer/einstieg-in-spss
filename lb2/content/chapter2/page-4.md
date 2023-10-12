---
title: "Lagemaße"  # Titel der Seite
weight: 204  # Individuelles Gewicht 
menuTitle: "Lagemaße" # Falls Titel zulang ist, hier Kurztitel
tags: ["Univariate Statistik", "Lagemaße", "DESCRIPTIVES", "FREQUENCIES"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-x-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Jetzt können wir unsere Variablen so bearbeiten, dass wir sie auch statistisch untersuchen können. Fangen wir deshalb mit der deskriptiven Statistik an. **Lagemaße** und **Streumaße** sind statistische Maßzahlen, die die **univariate Verteilung** beschreiben. Univariat meint dabei, dass wir uns immer nur eine Variable einzeln anschauen. Verteilung meint dabei, dass wir die Häufigkeiten je nach Ausprägung der Variable betrachten. Diese Maßzahlen versuchen dabei, Strukturen dieser Verteilung der Häufigkeiten bei einer Variable quantitativ zu beschreiben.

## Lagemaße vs. Streumaße

![Pivot](../img/pivot.png)

Schau dir die Verteilungen dieser Pivot-Tabelle an. Ausprägung `1` haben 67 Befragte in Panem ausgewählt. Ausprägung `2` haben 141 Befragte ausgewählt, und so weiter. Es gibt zwei Herangehensweisen, wie wir die Verteilung der Stichprobe (4989 gültige Fälle) entlang den elf gültigen Ausprägungen beschreiben können.

**Lagemaße** beschreiben wie sich die Befragten entlang der Ausprägungen verteilen. Sie geben eine Antwort auf die Frage, wo die meisten Beobachtungen liegen. Es macht einen inhaltlichen Unterschied, ob der Schwerpunkt der Befragten eher beim Pol *vertraue überhaupt nicht* oder *vertraue voll und ganz* liegt. Bei ersterem könnten wir die Aussage tätigen, dass die Bewohner:innen Panems den Politiker:innen eher nicht vertrauen. Bei Zweiterem könnten wir die Aussage tätigen, dass die Bewohner:innen Panems den Politiker:innen eher voll und ganz vertrauen.

**Streumaße** beschreiben wie die Fälle um den Mittelwert der Verteilung abweichen. Im Prinzip sagen sie aus, wie aussagekräftig der Mittelwert ist. Wenn das Streumaß hoch ist, weichen viele Fälle vom Mittelwert ab. Das deutet auf eine **heterogene Stichprobe** hin. Es gäbe in Panem unterschiedliche Meinungen zum Vertrauen in Politiker:innen. Wenn das Streumaß gering ist, weichen wenige Fälle vom Mittelwert ab. Das deutet auf eine **homogene Stichprobe** hin. Es gäbe in Panem eher eine einheitliche Meinung zum Vertrauen in Politiker:innen.

## Grundlegende Kenngrößen der Lagemaße

Es gibt zwei Arten der Lagemaße. Die ersten beschreiben die mittlere Tendenz einer Verteilung. 

1. Der **Modus** benennt die Ausprägung mit höchster Häufigkeit. Er ist für **alle Skalenniveaus** geeignet. Eine Verteilung ist **unimodal**, wenn es eine einzige Ausprägung gibt, die die häufigsten Fälle hat. Eine Verteilung ist **bimodal**, wenn zwei Ausprägungen jeweils die gleichhöchste Häufigkeit aufweisen. Gibt es mehr als zwei Ausprägungen, die die höchste Anzahl aufweisen, ist die Verteilung **multimodal**.

1. Der **Median** ist die Ausprägung, die die Verteilung in zwei gleich große Hälften teilt. Genau 50% der Befragten sind kleiner als die Ausprägung und 50% der Befragten sind größer als die Ausprägung. Das setzt voraus, dass das numerische Relativ in eine feststehende Reihenfolge gebracht werden kann. Daher ist mindestens das **ordinale Skalenniveau** notwendig. Der Median wird auch **zentraler Wert** genannt.

1. Das **arithmetische Mittel** berechnet den **Durchschnitt**. Du weißt sicher, dass für einen Durchschnitt alle Werte der (gültigen) Fälle addiert werden müssen und dann durch die (gültige) Fallzahl geteilt werden muss. Die Division ist nur unter der Annahme gleicher Abstände zwischen den numerischen Relativen mathematisch möglich. Daher benötigt das arithemtische Mittel strenggenommen mindestens ein **metrisches Skalenniveau**.

Die zweite Art der Lagemaße beschreibt die Verteilung der Befragten entlang den Ausprägungen einer Variable ohne den Schwerpunkt, das Mittel der Verteilung direkt zu bestimmen. 

1. **Quantil**. Alle gültigen Befragten ergeben 100% der Verteilung. Logisch, oder? Wir können jetzt untersuchen welche Werte n% der gültigen Befragten teilen. Ein Quantil ist also ein Parameter, der angibt wie viel Prozent der Verteilung unter einem Wert liegen. Die Idee ist dieselbe wie beim Median. Dieser ist im Prinzip das 50% Quantil. Nehmen wir beispielsweise ein 2% Quantil an. Beim 2% Quantil schauen wir uns die numerischen Werte an, bei denen die Stichprobe in 49 2%-Einheiten (das entspricht mathematisch 99,78 Fälle) geteilt wird. Ein Quantil kann einen beliebigen Prozentwert annehmen. 

1. **Quartil** ist ebenso ein spezielles Quantil. Hier wird die Stichprobe nicht wie beim Median halbiert, sondern geviertelt. Jeder Wert, der die Stichprobe in ein Viertel (25%, hier 1247,25 Befragte) teilt, ist ein Quartil. 

1. **Perzentil** ist das Quantil für 1%. Jeder Wert, der ein Prozent der Stichprobe teilt, ist ein Perzentil. 

1. **Interquartilabstand** ist der Abstand zwischen dem dritten und dem ersten Quartil. Also gibt er das Intervall an, in dem 50% der Werte der Verteilung liegen. 

## Lagemaße mit dem `DESCRIPTIVES`-Befehl

Jetzt kennen wir die Theorie, dann können wir uns schonmal anschauen, wie das in SPSS umgesetzt werden kann. 

{{< tabs groupId="des_lage" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/descriptives1.gif)


{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
DESCRIPTIVES VARIABLES = trstplt
/STATISTICS = MEAN.
```
Beim `DESCRIPTIVES` Befehl definierst du nach dem Parameter `VARIABLES` die Variablen, die du analysieren willst. Der ganze Zauber passiert nach dem `/STATISTICS` Unterbefehl. Für Lagemaße gibt es hier leider nur die Möglichkeit den Mittelwert mit `MEAN` auszugeben. 

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/descriptives1.png)

Als Output erhälst du nur eine kleine Tabelle, die dir den Mittelwert zeigt. Eine Interpretation könnte lauten: Das mittlere Vertrauen in Politiker:innen beträgt in der Stichprobe 4,73 auf eine Skala von 0 bis 10.
{{% /tab %}}
{{< /tabs >}}

## Lagemaße mit dem `FREQUENCIES`-Befehl

Alle weiteren Lagemaße kannst du mit `FREQUENCIES` aufrufen.

{{< tabs groupId="freq_lage" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/statistics1.gif)


{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
FREQUENCIES VARIABLES=trstplt
  /NTILES=4
  /STATISTICS=MEAN MEDIAN MODE
  /ORDER=ANALYSIS.
```
Den Hauptbefehl kennen wir ja schon. Neu hinzugekommen sind zwei Unterbefehle. Unter `/NTILES` kannst du bei Bedarf die **Quantile** definieren, wie du möchtest. Steht da `4` erhälst die **Quartile**. Steht da `2` erhälst du den **Median**. Steht da `10` erhälst du **Dezile**. Beim Ergebnis werden exemplarisch die Quartile interpretiert.

Bei `FREQUENCIES` kannst du unter `/STATISTICS` mehr Parameter auswählen. Dazu gehören bei den Lagemaßen `MEAN` für das **arithmetische Mittel**, `MEDIAN` für den **Median** und `MODE` für den **Modus**.

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/statistics1.png)

Wie du im Video sehen konntest, erhälst du als Output sowohl eine Pivot-Tabelle als auch eine Statistiktabelle. Hier ist nur ein Screenshot der Statistiktabelle. Der Median liegt beim Wert 5. Dieser Wert teilt die Stichprobe in zwei gleich große Hälften. Der Modus liegt ebenfalls bei 5. Die fünfte Ausßrägung wurde also durch die meisten Befragten ausgewählt

{{% /tab %}}
{{< /tabs >}}

So, Lagemaße kannst du dir nun bereits ausgeben lassen. Auf der nächsten Seite lassen wir uns dann Streumaße ausgeben!