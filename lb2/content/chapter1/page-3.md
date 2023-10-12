---
title: "Import von .sav"  # Titel der Seite
weight: 103  # Individuelles Gewicht 
menuTitle: ".sav-Datei" # Falls Titel zulang ist, hier Kurztitel
tags: ["Daten", "Dateiendungen", ".sav", "Datenimport", "GET"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-x-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}
{{%attachments style=\"grey\" title=\"Datensatz\" /%}}

Wie du schon gelernt hast, ist `.sav` die Endung von Datendateien in SPSS. Wenn du noch einmal nachschauen willst, was das ist, musst du [hier](https://lehre.bpkleer.de/spss101/lb1/chapter1/page-2/) klicken. So speicherst du auch das Datenfenster samt Datenansicht (die eigentliche Datentabelle) und Variablenansicht (das Datengerüst mit spezifischen Informationen zu den Daten) ab. Dem entsprechend ist es auch super einfach, `.sav`-Dateien in SPSS zu laden. Dann fangen wir mal an!

{{< tabs groupId="sav" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/sav.gif)

{{% /tab %}}
{{% tab name="Syntax" %}}
```{SPSS}
GET 
 /FILE="Z:/Hier_muss_Dein_Dateipfad_stehen.sav".
```
Dieser Befehl ist deutlich einfacher als bei globalen Datendateien.

`GET` ist der Hauptbefehl. Für SPSS eigene Dateien reicht das vollkommen aus. Du musst auch nicht weiter spezifizieren, mit welchem Dateityp SPSS rechnen muss.
`/FILE` verweist auf den Speicherort, wo SPSS die Daten finden kann - also auf den Pfad der Datei.

{{% /tab %}}
{{% tab name="Ergebnis Datenansicht" %}}

![Ergebnis](../img/savdaten.png)

{{% /tab %}}
{{% tab name="Ergebnis Variablenansicht" %}}

![Ergebnis](../img/savvariablen.png)

{{% /tab %}}
{{< /tabs >}}

Super, jetzt weißt du, wie du Daten mit verschiedenen Dateiendungen in SPSS importierst. Jetzt können wir weitermachen. Auf den nächsten Seiten werden wir erste deskriptive Ergebnisse produzieren. Los geht's!

