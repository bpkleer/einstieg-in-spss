---
title: "Kreuzabellen"  # Titel der Seite
weight: 101  # Individuelles Gewicht 
menuTitle: "Kreuztabellen" # Falls Titel zulang ist, hier Kurztitel
tags: ["Kreuztabellen", "Randhäufigkeit", "absolute Häufigkeiten"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-x-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Bevor du dich an die Berechnung von Zusammenhangsmaßen machst, erstellst du zuerst Tabellen, damit wir bivariate Verteilungen untersuchen können. Durch die Kreuztabelle lassen sich bereits mögliche vermutete Zusammenhänge zwischen zwei Variablen sichtbar machen. Dies ist auch für die grafische Darstellung relevant. Üblicherweise verwenden wir **kategoriale und/oder ordinale Variablen** für die Kreuztabellen. Bei metrischen Variablen gibt es schlichtweg zu viele Zeilen, Spalten und Zellen, um diese sinnvoll zu interpretieren. Daher werden metrische Variablen vor der Darstellung in einer Kreuztabelle oft gruppiert: Zum Beispiel wird das Alter in Altersgruppen rekodiert. 

Für eine einfache Kreutzabelle arbeiten wir mit dem `CROSSTABS`-Befehl. Schau dir diesen Screenshot an. Wie würdest du die Kreuztabelle beschreiben?

![Crosstab](../img/crosstab.png)

Wie jede Tabelle, beinhaltet die Kreuztabelle in SPSS **Zeilen**, **Spalten** und **Zellen**. Anders als bei den *Pivot-Tabellen*, die wir bisher kennengelernt haben, ist das Besondere hier, dass jeder **Zeile** und jeder **Spalte** einer Variablenausprägung zugeordnet ist. Die Anzahl der Zeilen und Spalten resultiert aus der Anzahl der Ausprägungen der verwendeten Variable. Hat die Variable in den Zeilen vier Ausprägungen, gibt es vier Zeilen. Hat die Variable in den Spalten drei Ausprägungen, hat die Kreuztabelle drei Spalten. Jede **Zelle** beinhaltet, die Fallzahl der Fälle, die **sowohl** die jeweilige Ausprägung in der Zeilenvariable **als auch** die jeweilige Ausprägung der Spaltenvariable ausgewählt hat. Den rechten und unteren Rand einer Kreuztabelle nennt man **Randhäufigkeit**. Das sind im Prinzip nur die univariaten Häufigkeiten der jeweiligen Variable. Überprüfe das mit dem `FREQUENCIES` Befehl schnell. 

{{< tabs groupId="Crosstab" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/crosstab.gif)

{{% /tab %}}
{{% tab name="Syntax" %}}
```{spss}
CROSSTABS
  /TABLES=edu BY gndr
  /CELLS=COUNT.

```
Neu ist der Hauptbefehl `CROSSTABS`. Im Unterbefehl `/TABLES` definierst du Spalten- und Zeilenvariable. Die Logik ist immer dieselbe. Zuerst kommt die Zeilenvariable und dann die Spaltenvariable. Also `/TABLES=Zeilenvariable by Spaltenvariable`. Den Unterbefehl `/CELLS` schauen wir uns auf der nächsten Seite genauer an. 

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/outputcross.png)

Eine Zelle würdest du beispielsweise so Interpretieren: 360 Fälle sind weiblich **und** haben einen Bildungsabschluss erster Stufe.

{{% /tab %}}
{{< /tabs >}}

In einer Kreuztabelle werden nur die Fälle mit einbezogen, die sowohl bei der Zeilenvarible als auch bei der Spaltenvariable gültige Werte aufweisen. Das kannst du an dieser Tabelle ablesen. 

![Missings](../img/crossmissings.png)

{{% expand \"Wie viele gültige Fälle haben wir? Wie viele NA's?\" %}}
4648 Fälle haben bei beiden Variablen einen gültigen Wert. 352 Fälle sind Missings.
{{% /expand %}}

Jetzt kannst du Kreuztabellen mit absoluten Häufigkeiten untersuchen. Häufig interessieren wir uns jedoch für relative Häufigkeiten. Das lernst du im nächsten Schritt.
