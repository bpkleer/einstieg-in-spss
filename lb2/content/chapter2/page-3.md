---
title: "Berechnen von Variablen"  # Titel der Seite
weight: 203  # Individuelles Gewicht 
menuTitle: "Compute-Befehl" # Falls Titel zulang ist, hier Kurztitel
tags: ["Indizes", "COMPUTE", "Subtraktion", "Addition", "Variablenbenennung"]  # Tags hiereinsetzen; Kurzwort, was auf der Seite passsiert
---

{{% buttonGit href="https://gitlab.ub.uni-giessen.de/methoden-politik/einstieg-in-spss/issues/new?issue[title]=" icon="fas fa-bug" %}} {{% /buttonGit %}} 

{{% buttonGit href="mailto:?subject=Schau%20dir%20das%20mal%20an%3A%20" icon="fas fa-paper-plane" %}} {{% /buttonGit %}}

{{% buttonGit href="https://t.me/share/url?url=" icon="fab fa-telegram" %}} {{% /buttonGit %}}

{{% buttonGit href="https://api.whatsapp.com/send?text=" icon="fab fa-whatsapp" %}} {{% /buttonGit %}}

{{% buttonGit href="https://twitter.com/share?url=" icon="fab fa-x-twitter" %}} {{% /buttonGit %}}

{{% buttonGit href="https://www.facebook.com/sharer/sharer.php?u=" icon="fab fa-facebook" %}} {{% /buttonGit %}}

Manche Umcodierungen können wir nicht durchführen, indem wir die Reihenfolge der Ausprägungen ändern oder diese durchführen. Manchmal wollen wir eine neue Variable aus einer alten berechnen. Das machen wir oft bei **Indizes**. 

## Exkurs: Indizes

**Indizes** werden vor allem gebildet, wenn ein Konstrukt als Ganzes, ohne Rücksicht auf seine Dimensionen, durch einen einzigen Wert einer neuen Variable repräsentiert werden soll. Sie dienen somit vor allem zur Komplexitiätsreduktion. **Skalen** sind Sonderfälle von Indizes, sie erfassen mehrere Items einer Dimension, z.B. Ausländerfeindlichkeit. Sie müssen durch spezielle Verfahren (z.B. Faktorenanalysen) auf Eindimensionalität geprüft werden.

## Der `COMPUTE`-Befehl

Mit `COMPUTE` wird aus einer oder mehreren bestehenden Variablen eine neue berechnet. Im Prinzip folgt auf einen `COMPUTE`-Befehl immer eine Formel zur Berechnung einer neuen Zielvariable. Die grundlegende Struktur sieht wie folgt aus:

```{spss}
COMPUTE Zielvariable = Formel
```

Als Formel bietet SPSS alles mögliche an. Das siehst du im unten gezeigten Klickweg. Beschränken wir uns im Folgenden auf die Subtraktion und Addition von Variablen. 

![Klickweg](../gif/compute.gif)

## Subtraktion von Variablen

Statt mit Alterskohorten könnten wir auch mit Generationen arbeiten. Mist! Wir haben leider keine Geburtsjahr-Variable in unserem Datensatz. Oder vielleicht doch? Überlege, wie du aus dem angegebenen Alter einer Person das Geburtsjahr berechnen würdest.

Ganz genau. Wir haben das Alter der befragten Personen zum Erhebungszeitpunkt. Wir wissen jetzt zum Glück, dass der Survey 2023 erhoben wurde. In anderen Surveys findet sich das Erhebungsjahr oftmals als Variable im Datensatz. Um das Geburtsjahr zu berechnen, ziehen wir vom Erhebungsjahr das Alter der Person zu diesem Zeitpunkt ab. Dafür können wir folgende Formel aufstellen: `Geburtsjahr(Fall) = Erhebungsjahr - Alter(Fall)`. Das Geburtsjahr eines Falles entspricht dem Erhebungsjahr minus dem Alter des Falles zum Erhebungszeitpunkt. Wir kennen sowohl das Erhebungsjahr, als auch das Alter des Falles. Also können wir auch eine Geburtsjahr-Variable berechnen. Wir fügen dazu einfach die Formel in den `COMPUTE`-Befehl ein.

{{< tabs groupId="subtraktion" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/subtraktion.gif)

{{% /tab %}}
{{% tab name="Syntax" %}}
```{spss}
COMPUTE birthyear = 2023 - age.
fre birthyear.
```
Wie ist dann die neue Variable `birthyear` codiert? SPSS zieht für jeden Fall das angegebene Alter vom Erhebungsjahr ab. 

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/subtraktion.png)

Hier ist ein Screenshot der neuen Geburtsjahres-Variable

{{% /tab %}}
{{< /tabs >}}

{{% expand \ "Welchen Wert würden die Fälle 10000, 10001 und 10002 auf der Variable birthyear erhalten?"\ %}}
Fall 10000: 1982

Fall 10001: 1958

Fall 10002: 1975
{{% /expand %}}


## Addition von Variablen

Super, jetzt hast du die Subtraktion verstanden. Machen wir weiter mit der Addition. Diese kommt zum Beispiel bei Indizes vor. Hierfür wollen wir einen Vertrauensindex erstellen. Welche Variablen in `PSS` messen das Vertrauen in eine Institution? Richtig: `trstprl`, `trstprt`, `trstplt` und `trstlgl`. Eigentlich müsste vorher noch mit einer Faktorenanalyse überprüft werden, ob es sich wirklich um eine Dimension handelt. Das lassen wir für die Übung außer Acht. Wenn wir einen additiven Index erstellen wollen, müssen wir die Variablen einfach addieren. 

{{< tabs groupId="addition" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/addition.gif)

{{% /tab %}}
{{% tab name="Syntax" %}}
```{spss}
COMPUTE trst = trstprl + trstprt + trstplt + trstlgl.
```
Für jeden Fall würde hier die Werte dieser vier Variablen addiert werden. Das Ergebnis ist der neue Wert in der neuen Variable `trst`.

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/addition.png)

Hier ist ein Screenshot der neuen Vertrauens-Variable. Wie du siehst, haben wir 75 fehlende Fälle. 

{{% /tab %}}
{{< /tabs >}}


{{% expand \ "Welchen Wert würden die Fälle 10000, 10001 und 10002 auf der Variable trst erhalten?"\ %}}
Fall 10000: 19

Fall 10001: 17

Fall 10002: 21
{{% /expand %}}

## Addition mit `SUM`

Wenn wir einen additiven Index erstellen wollen, definiert SPSS alle Fälle mit mindestens einem fehlenden Wert als fehlend für den gesamten Index. Schau dir im Datensatz dazu mal Fall 10026 an. 

Auf dem Index hat dieser Fall einen Punkt `.` verzeichnet. Er ist also ein systemdefinierter fehlender Wert. Warum? Das liegt daran, dass dieser Fall bei einer der Ursprungsvariablen, nämlich `trstprt`, bereits einen fehlenden Wert hat. Auf den anderen Variablen des Indexes, nämlich `trstprl`, `trstplt`, `trstlgl` hat dieser Fall jedoch gültige Werte. Wenn wir diese addieren erhalten wir einen Wert von 22. Wenn es theoretisch plausibel ist, möchten wir auch solche Fälle wie diesen in unseren additiven Index aufnehmen. Er würde dann auf dem neuen additiven Index den Wert `22` erhalten. Dafür gibt es einen alternativen Befehl, mit dem wir einen additiven Index erstellen können, der solche Fälle beinhaltet.

{{< tabs groupId="sum" >}}
{{% tab name="Klickweg" %}}

![Klickweg](../gif/sum.gif)

{{% /tab %}}
{{% tab name="Syntax" %}}
```{spss}
COMPUTE trst2 = SUM(trstprl, trstprt, trstplt, trstlgl).
```
Neu ist der Paramter `SUM`. In der Klammer musst du alle Variablen, aus denen der additive Index gebildet werden soll, nennen. 

{{% /tab %}}
{{% tab name="Ergebnis" %}}

![Ergebnis](../img/sum.png)

Hier ist ein Screenshot der neuen Vertrauens-Variable. Wie du siehst, haben wir hier keine fehlenden Werte. Du kannst gerne im Datensatz nachschauen, ob der Fall 10026 wirklich den Wert `22` erhalten hat.

{{% /tab %}}
{{< /tabs >}}

{{% expand \ "Was müsstest du machen, um wieder zur Ausgangsskala zu kommen?"\ %}}
Wenn die vier Ursprungsvariablen dieselbe Skala haben, können wir den additiven Index durch die Anzahl an Variablen teilen, aus denen der additive Index besteht. Dann erhalten wir einen Index von 0 bis 10, so wie die Ursprungsvariablen skaliert sind. Das könnte zum Beispiel so aussehen:

```{spss}
COMPUTE trst_mean = trst2/4.
```
Alternativ könnten wir das auch direkt in einem Schritt machen:

```{spss}
COMPUTE trst2 = SUM(trstprl, trstprt, trstplt, trstlgl)/4.
```
{{% /expand %}}

## Benennung von Variablen

Nun haben wir zwei neue Variablen erstellt `trst` und `birthyear`. Wie können wir diese Variablen jetzt benennen?

Richtig. Wie bei `RECODE` mit `VARIABLE LABELS` und `VALUE LABELS`. Du kannst dir vorher konzeptionell überlegen, wie du die Werte bei dem additiven Index benennen würdest, beziehungsweise was der potentiell höchste und niedrigste Wert ist. 

{{% expand \ "Welche Werte würde trst erhalten?"\ %}}
Der maximale Wert ist klar: `4 x 10 = 40`. Eine Person, die bei allen vier Variablen das höchste Maß an Vertrauen angekreuzt hat (also den Wert `10`), erhält im additiven Index den Wert `40`. Personen, die bei allen vier Variablen das geringste Maß an Vertrauen angekreuzt haben, erhalten den Wert `0`, `4 x 0 = 0`. Daher ist die potentielle Spannweite der Variable `trst` von `0` bis `40`.
{{% /expand %}}

{{% expand \ "Welche Werte würde birthyear erhalten?"\ %}}
Dafür musst du bei der Variable `agea` den jüngsten und ältesten Fall suchen. Wenn man dieses Alter von 2023 abzieht, erhälst du eine Spannweite von `1925` bis `2007`. Wow, mehr als 90 Jahre!
{{% /expand %}}