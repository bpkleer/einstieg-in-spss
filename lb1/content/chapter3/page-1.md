---
title: "Das Syntax-Fenster"  # Titel der Seite
weight: 301  # Individuelles Gewicht 
menuTitle: "Syntax-Fenster" # Falls Titel zulang ist, hier Kurztitel
tags: ["Syntax", "Befehle", "Frequencies", "Kommentare", "Hilfe", "Befehlssyntaxreferenz"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Schauen wir uns nun ein anderes Fenster von SPSS an - das Syntaxfenster. 

{{% expand \"Welche Funktion hatte nochmal das Syntaxfenster? Mit welchem Dateiformat kann es gespeichert werden?\" %}}
In einem Syntaxfenster können mit einer Programmiersprache diverse Funktionen ausgeführt werden. Diese Datei kann dann als (Code-)Skript gespeichert werden. Das spart wie du im Verlauf des Kurses sehen wirst lange Klickwege. Ein sauberer Programmiercode führt zu besseren Ergebnissen!
Das Syntaxfenster wird im `.sps`-Dateiformat gespeichert.
{{% /expand %}}

Ein neues Syntaxfenster öffnest du, in dem du auf `Datei`, dann `Neu`und dann `Syntax` klickst. 

![Syntax öffnen](../img/syntaxöffnen.png)

Das Syntaxfenster ist zunächst ein leeres Feld, in dem du Text eingeben kannst. SPSS erkennt dabei festgelegte Befehle und führt diese aus. Jeder **Hauptbefehl** erscheint dir *Blau* im Syntaxfenster. Mit einem Hauptbefehl wird die Operation, die wir durchführen möchten, festgelegt. Meistens gibt es zu jedem Hauptbefehl noch diverse **Unterbefehle**. Diese werden *Grün* angezeigt. Diese spezifizieren den Befehl und sagen SPSS, was genau gemacht werden soll. Zusätzlich muss noch definiert werden, womit gearbeitet werden soll. Diese **Parameter** werden dir *Rot* dargestellt.

{{% expand \"Schau dir diesen Screenshot an. Was kannst du erkennen? Kannst du schon sagen, welche Operation hier ausgeführt wird?\" %}}
Befehle sind in der Regel englische Begriffe. Meistens kannst du so auch ohne tiefes Wissen zur Programmiersprache erahnen, welche Operation durchgeführt wird. `FREQUENCIES` ist der **Hauptbefehl**, er ist *blau*. `FREQUENCIES` ist englisch für *Häufigkeiten*. Mit diesem Befehl kannst du dir also die absoluten und relativen Häufigkeiten ausgeben lassen, also wie oft die Ausprägungen der Variable im Datensatz vorkommen. Mit dem **Parameter** `VARIABLES` wird SPSS klar, mit welchen Variablen SPSS arbeiten muss. Diese folgen nach dem `=`. Dieser Befehl gibt dir also die Häufigkeiten der Bildungsabschlüsse in PANEM aus. Ziemlich cool, oder?

Woher weiß SPSS, in welcher Reihenfolge die Ausprägungen angezeigt werden sollen? Jedem Bildungsabschluss ist eine Zahl zugeordnet. In *Grün* siehst du den **Unterbefehl** `/ORDER`. Zusammen mit dem **Parameter** `ANALYSIS` machst du SPSS klar, dass er die Bildungsabschlüsse aufsteigend nach den zugeordneten Zahlen sortieren soll. 

Der Frequencies-Befehl ist der vielleicht wichtigste und am häufigsten benutzte Befehl in SPSS. Wenn du dir eine Variable schnell ausgeben lassen möchtest, kannst du auch eine beliebte Abkürzung benutzen. `fre edu.`liefert dir denselben Output.
{{% /expand %}}

![Syntax Frequencies](../img/syntaxfreq.png)

**Wichtig:** Jeder Befehl endet mit einem `.`. Wird der Punkt am Ende des Befehls vergessen, kommt es häufig zu Fehlern. SPSS liest nämlich den Text im Syntaxfenster von links nach rechts, von oben nach unten. Ohne Punkt weiß SPSS nicht, dass der Befehl zu Ende ist. Es wird also weiter gelesen, sodass es deswegen oft zu Fehlern kommt. Zu Beginn ist dies der häufigste Fehler, aber auch mit der häufigeren Anwendung schleicht sich dieser Fehler im Code-Schreiben immer mal wieder ein. Es ist also eine erste Möglichkeit bei Ausgabe eines Fehlers, die Syntax zu prüfen (z.B. ob der Punkt vergessen wurde). Versuche daher beim Programmieren darauf zu achten.

Damit wir alle unsere Schritte nachvollziehen können, sollten wir unsere Code ausführlich kommentieren. **Kommentare** beginnen mit einem `*`. Wenn SPSS das Sternchen erkennt, weiß es, dass der darauffolgende Text keine für SPSS lesbaren Befehle enthält. Ein Kommentar kann über mehrere Zeilen gehen. Daher ist es wichtig, dass du auch am Ende des Kommentars einen `.` setzt. Durch den Punkt weiß SPSS auch hier, dass der Kommentar fertig ist und der eigentliche Code jetzt folgt.

![Syntax Kommentar](../img/syntaxkom.png)

Super, jetzt haben wir die Grundlagen der Syntax verstanden! Aber wie können wir den geschriebenen Code jetzt ausführen? Dafür markieren wir den auszuführenden Befehl und gehen einfach auf den grünen Ausführungspfeil. Alternativ kannst du auch nach der Markierung `Strg + R`, bzw. `Cmd + R`drücken. Es öffnet sich automatisch das Ausgabefenster. In diesem Fenster generiert SPSS eine Tabelle, die alle wichtigen Informationen beinhaltet. In der Regel benutzen wir das Ausgabefenster also nur, um uns das Ergebnis unserer Operation anzuschauen und zu interpretieren.

![Syntax Ausführen](../gif/Syntax.gif)

{{% expand \"Und so sieht das Ausgabefenster aus:\" %}}
![Ausgabefenster](../img/ausgabeedu.png)
{{% /expand %}}

{{% expand \"Gut, fassen wir zum Schluss zusammen: Welche Vorteile bietet die Syntax?\" %}}
1. Bei vielen ähnlichen Operationen ist die Verwendung von Syntax empfehlenswert, da du den Befehl einfach kopieren kannst.
1. Du kannst dein Vorgehen protokollieren und nachvollziehbarer machen.
1. Du kannst Ergebnisse speichern und immer wieder neu berechnen lassen.
1. Bringt eine sinnvolle Reihenfolge in deine Analyse.
1. Du kannst schnell Details deiner Operation ändern.
1. Du kannst schneller Fehler finden
{{% /expand %}}

Wie wir gesehen haben, ist das Syntaxfenster ein tolles Tool für die Arbeit mit quantitativen Daten. Du kannst alle relevanten Operationen auch über die Menüleiste, die dir oben vielleicht aufgefallen sind, tätigen. Jedoch bietet das einfach zu wenige Vorteile, ist nicht dokumentierbar und ist oft umständlicher. Daher werden wir vor allem mit der Syntax arbeiten. Falls du Lust hast dich vertieft in die Befehle einzuarbeiten, gibt es da eine tolle Möglichkeit. Über den Reiter `Hilfe` und dann `Befehlssyntaxreferenz` kannst du die komplette Befehlssyntax nachschlagen.

![Befehlssyntaxreferenz](../img/befehlssyntax.png)

Jetzt hast du die nötige Grundlage, um einzelne Operationen und Befehle zu lernen. Fangen wir gleich mal damit an! 

