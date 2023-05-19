---
title: "Daten sortieren"  # Titel der Seite
weight: 303  # Individuelles Gewicht 
menuTitle: "Sortieren" # Falls Titel zulang ist, hier Kurztitel
tags: ["SORT", "SPLIT FILE"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

In manchen Fällen wollen wir uns verschiedene Subgruppen gleichzeitig anschauen. Dafür bietet SPSS einen Befehl an, der bei jeder Analyse das Ergebnis nach den verschiedenen Subgruppen, die uns interessieren, sortiert ausgibt.

### Der Syntax-Befehl

Schauen wir uns dafür an, ob es in PANEM unterschiede hinsichtlich der Geschlechter in der Links-Rechts-Selbsteinschätzung gibt. Hierfür brauchst du als **Hauptbefehl** `SORT CASES`. Nach dem `BY`gibst du die Variable die uns interessiert, hier `gndr`, an. Wenn du diesen Befehl benutzt, sortiert SPSS deine Fälle im Datensatz entsprechend der Variable `gndr`. Das kannst du in der **Datenansicht** überprüfen. Anschließend brauchst du einen weiteren **Hauptbefehl**, nämlich `SPLIT FILE`. Nach einem `LAYERED BY` **Parameter** gibst du die Variable `gndr` an. Dank `SPLIT FILE` weiß SPSS, dass alle Ergebnisse entsprechend der Variable `gndr` geschichtet dargestellt werden sollen. Möchtest du deine Ergebnisse wieder ohne Schichtung anscheuen, beendest du das mit dem Befehl `SPLIT FILE OFF`.


{{< tabs groupId="sort" >}}
{{% tab name="Klickweg" %}}
![Filter](../gif/sort.gif)
{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
SORT CASES BY gndr.
SPLIT FILE LAYERED BY gndr.

fre lrscale.

SPLIT FILE OFF.

```
{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis Filter](../img/sortergebnis.png)

{{% /tab %}}
{{< /tabs >}}

{{% expand \"Hast du gut aufgepasst? Woran erkennst du im Datenfenster, dass du korrekt sortiert hast?\" %}}
Ich passe immer auf! Unten rechts steht dann *Aufteilen nach ...* .
{{% /expand %}}

{{< tabs groupId="Aufgabe" >}}
{{% tab name="Aufgabe" %}}
Aufgabe: Unterscheiden sich die Geschlechter hinsichtlich des Bildungsabschlusses in PANEM?
Schaue dir dafür die Variable *edu* sortiert an. Versuche es bitte erst alleine. Anschließend darfst du dir die Lösungssyntax anschauen.
{{% /tab %}}
{{% tab name="Lösungssyntax" %}}
```{SPSS}
SORT CASES BY gndr.
SPLIT FILE LAYERED BY gndr.

fre edu.

SPLIT FILE OFF.
```
{{% /tab %}}
{{< /tabs >}}



Du hast in diesen Lernbuch den Sprung in das kalte Wasser gewagt, die Oberfläche von SPSS kennengelernt und erste Syntax-Befehle zur Sortierung und Filterung deiner Daten gemeistert. Jetzt bist du bereit für die nächsten Schritte. Super! 