---
title: "Speicherarten von Daten"  # Titel der Seite
weight: 101  # Individuelles Gewicht 
menuTitle: "" # Falls Titel zulang ist, hier Kurztitel
tags: ["Daten", "Dateiendungen", "Speicherung", ".sav", ".txt", ".csv"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Wie bereits in Lernblock 1 besprochen, haben Dateien immer **Dateiendungen**, die auf das Lese-/Schreibformat hinweisen. Dies waren zur Erinnerung zum Beispiel `.docx` für Word-Dateien oder `.pptx` für Powerpoint-Dateien. 

Für Datensätze gibt es globale Dateiformate, die von den meisten Programmen gelesen werden können, aber auch programmspezifische Dateiformate. Für SPSS kennen wir ja schon das programmspezifische Dateiformat `.sav`. So wird auch das **Datenfenster** in SPSS gespeichert.

Wie wir gesehen haben, werden Daten in Tabellenform gespeichert, bei der die Fälle in den Zeilen und die Variablen in den Spalten stehen. Der Computer kann die verschiedenen Fälle dadurch identifzieren, dass eine neue Zeile durch einen Absatz, also einen Klick auf die *Enter-Taste*, erstellt wird. Aber woher weiß der Computer, wann eine neue Variable zu lesen ist? Dafür gibt es bei globalen Dateiformaten zwei übliche Konventionen. Die Erste ist der *Tabulator*. Das ist die Taste über der Feststelltaste. Also die Taste mit den zwei Pfeilen. Diese ist im Prinzip das Gegenstück zur *Enter-Taste*. Während letzteres einen Absatz durch eine neue Zeile erstellt, macht der *Tabulator* einen Absatz innerhalb einer Zeile. Diesen leeren Raum erkennt der Computer und weiß daher, dass er eine neue Variable lesen soll. Die Zweite ist das *Komma* `,` bei einer englischen Sprachversion (das ist auch der Standard) und ein *Semikolon* `;` bei einer deutschen Sprachversion. Immer, wenn ein solches Zeichen in einer Zeile steht, weiß der Computer, dass eine neue Variable folgt. Aber was ist mit Dezimalzahlen bei einer englischen Spracheinstellung? Im Englischen wird eine Dezimalzahl mit einem *Punkt* dargestellt. Also: `10.5`statt `10,5`. Das ist auch in englischsprachigen Textdatensätzen so. Daher gibt es keinen Konflikt um das Komma und der Computer weiß, dass eine neue Variable, also eine neue Spalte folgt. Im Deutschen ergibt sich dieses Problem nicht, denn das Trennzeichen ist ja das Semikolon (`;`).

Die beiden globalen Dateiformate sind:

- `.txt` (Textdateien, in denen Daten meist mit einem *Tabulator* getrennt sind)

- `.csv` (Textdateien, in denen Daten mit einem *Komma* getrennt sind)

Wozu muss ich das wissen? Es gibt Fälle, in denen deine Daten nicht als `.sav`vorliegen. Beispiel gefällig? Vielleicht kennst du Ilias-Umfragen, die Dozent:innen benutzen. Du kannst dir die Ergebnisse auch exportieren lassen, also in Tabellenform herunterladen, wenn du diese tiefergehend analysieren willst. Und welcher Dateityp wird dann runtergeladen? Genau: Ilias kann diese Daten nur als `.txt`oder `.csv` exportieren. Dann schauen wir uns das mal genauer an!

