---
title: "Deskriptive Statistik"  # Titel der Seite
weight: 201  # Individuelles Gewicht 
menuTitle: "Allgemein" # Falls Titel zulang ist, hier Kurztitel
tags: ["Univariat", "Häufigkeiten", "FREQUENCIES"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonShare href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonShare %}} 

{{% buttonShare href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonShare %}}

{{% buttonShare href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonShare %}}

{{% buttonShare href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonShare %}}

{{% buttonShare href="https://twitter.com/share?url=" icon="fab fa-x-twitter" %}} {{% /buttonShare %}}

{{% buttonShare href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonShare %}}

{{% button href="https://bmc.link/bpkleerw" icon="fa-solid fa-beer-mug-empty" %}} {{% /button %}}

## Deskriptive Häufigkeiten auszählen

{{%attachments style=\"grey\" title=\"Datensatz\" /%}}

Als erstes probieren wir aber das vorhin gelernte aus und laden nun den Datensatz `pss` in SPSS.
Der erste Schritt zur Datenanalyse ist in der Regel die Sichtung und Auszählung der Variablen im Datensatz. Hier schaust du dir **absolute und relative Häufigkeiten** an. Auch weitere Informationen zu den Variablen kannst du so bequem herausfinden. Sind sie **numerisch** oder eine **Zeichenfolge**? Was ist ihr **Skalenniveau**? Welches **Skalierungsverfahren** wurde angewendet? Wie viele **Ausprägungen** hat die Variable? Im Laufe der Zeit wirst du ein geschultes Auge entwickeln und siehst recht schnell, mit welchen Variablen, welche statistischen Operationen möglich sind.

Den Befehl dazu, `FREQUENCIES`, kennst du bereits. Schauen wir uns noch einmal systematisch an.

{{< tabs groupId="sav" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/freq.gif)


{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
FREQUENCIES VARIABLES = wkhtot trstlgl.
```

`FREQUENCIES` ist der Hauptbefehl. Hier werden die Häufigkeiten für die Variable `wkhtot`und `trstlgl`angezeigt. Besonders sind hier einige Abkürzungen, die häufig gebraucht werden.

```{SPSS}
FREQUENCIES VARIABLES = wkhtot to trstlgl.
```
Durch `to` werden dir nicht nur zwei Variablen angezeigt, sondern alle Variablen, die in der Variablenansicht zwischen `wkhtot` und `trstlgl`liegen. So kannst du dir bequem mehrere Variablen anzeigen lassen.

```{SPSS}
FREQUENCIES VARIABLES = ALL.
```
Durch `ALL` werden dir alle Variablen des Datensatzes angezeigt.

```{SPSS}
fre wkhtot trstlgl.
fre wkhtot to trstlgl.
fre all.
```

Die Abkürzung `fre` kennst du auch bereits. Sie ersetzt `FREQUENCIES VARIABLES`.
{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/freq.png)

Hier siehst du eine exemplarische Häufigkeiten-Tabelle. Dunkelgrau siehst du deine Ausprägungen, sowohl gültige als auch fehlende Werte. Diese Tabelle ist sehr intuitiv zu lesen. Bei den Prozentzahlen musst du aber darauf achten, worauf sich diese Beziehen. **Prozente** bezieht sich auf deine **gesamte Stichprobe**. Also auch fehlende Fälle. In unserem Beispiel sind das 5000 Befragte. Also kannst du nur folgende Aussage treffen: "Von **allen Befragten** gaben 4,6% den Wert 8 im Vertrauen gegenüber Parteien an". **Gültige Prozente** bezieht sich auf deine **gültigen Fällen**. Das sind in unserem Beispiel 4983 Befragte. Folgende Aussage kannst du tätigen: "4,7% von allen **gültigen Fällen** vertrauen den Parteien mit dem Wert 8 auf der Skala". Die **kumulierten Prozente** addieren immer aufsteigend die gültigen Prozente. Besonders zu Beginn kommt es hierbei zu Interpretationsfehlern. Lass dich dadurch nicht verwirren.

{{% /tab %}}
{{< /tabs >}}

Jetzt kannst du dir bereits Häufigkeitstabellen einzelner Variablen ausgeben lassen, und somit einzelne Variablen beschreiben. Wir werden jetzt erst Variablen rekodieren bzw. berechnen und danach uns deskriptive Maße ausgeben lassen.