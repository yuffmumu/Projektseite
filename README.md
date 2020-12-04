# Projektseite

1 [Einleitung/Vision](#1)    

2 [Das Programm](#2)
     
2.1      [Beschreibung des Programms](#2.1)
     
2.2      [Wie Funktionieren die Einzelteile?](#2.2)
     
3 [Besondere Herausforderungen](#3)  

4 [Schlusswort](#4)  


### <a name="1"></a>Einleitung/Vision:
"Brawl of Alphonzo and Gonzales" ist das Ergebniss unserer ersten Programmiererfahrung.
Was als ein Plattformer begann entwickelte sich nach kurzer Zeit zu einem Brawl-Game, in dem zwei Spieler als 2 Charactere (Alphonzo, Gonzales) auf einer von 2 Stages Gegeneinander Kämpfen.
Wir beide hatten uns schon vor dem Beginn des Informatikunterrichts sehr kurz mit dem Programmieren auseinandergesetzt. Die Anfängerfreundlichkeit aber dennoch verhältnissmäßig große Bandbreite an Möglichkeiten von Snap war uns schon im Vorhinein bekannt, sowie auch die Schwierigkeit einer richtigen Programmiersprache für einen Anfänger. 
Von daher war die Entscheidung für ein Snap-Projekt schnell gefallen.
Den Vorkentnissen entsprechend war die erste Idee ein Jump and Run Spiel.
Wir eigneten uns das Programmieren mit Snap von 0 an und entwickelten so, dank des anfängerfreundlichen Aufbaus der Block-Programmiersprache, die ersten Grundlagen für ein J&R Spiel.
Es dauerte nicht allzulang, bis wir bemerkten, dass uns ein J&R Spiel sehr limitieren würde, denn Level zu designen hatte 1. relativ wenig mit Programmieren sondern mehr mit Design zu tun und vor allem wäre das Spiel relativ kurz, denn ein Paar J&R Level durchzuspielen ist schnell passiert.
Beim betrachten der Grundlagen die bereits vorhanden waren fiel uns auf, dass alles, was wir bis zu diesem Zeitpunkt gemacht hatten, nicht nur auf einen Plattformer passen würde, sondern auch auf ein Brawlgame (wie z.B. Smash Brothers, Duck Game oder Brawlhallah).
Der größte Vorteil eines solchen Spiels gegenüber eines Plattformers ist selbstverständlich, dass er kompetitiv ist/sein kann. Spielen 2 Spieler gegeneinander in einem tatsächlich Skill-basierten Spiel ist die Spielzeit nicht so limitiert wie in einem J&R, da man immer weiter üben könnte, wenn man es darauf anlegt.
Außerdem wirkten die Möglichkeiten das Spiel zu Programmieren z.B. in Sachen Fähigkeiten wie dem Schuss deutlich reizvoller, als die Blöcke für das nächste Level eines Jump and Runs an den richtigen Ort zu bringen.
Dementsprechend entwickelten wir das Spiel in ein Brawl-Game um.
### <a name="2"></a>Das Programm:

### <a name="2.1"></a>Beschreibung des Prgramms: 
Startet man das Spiel erscheint der Startscreen.
Durch die Visuell angegebenen Zahlen, welche denen auf der Tastatur entsprechen, wird man durch die Startscreens geleitet, in welchen die Spieler ihren Character und ihre gewünschte Stage auswählen.
Hat man dies abgeschlossen, so Spawnt man und der Kampf beginnt.
Mithilfe der Waffe und der Individuellen Fähigkeit des gewählten Characters gilt es nun die Leben des Gegners von 100 auf 0 zu bringen.
Wer dies zu erst schafft Gewinnt das Spiel.

### <a name="2.2"></a>Wie Funktionieren die Einzelteile?:
[Startscreen](#2.2.1), 
[Bewegung und die Stage](#2.2.2) ,
[Kampfsystem](#2.2.3),

#### <a name="2.2.1"></a>Startscreen:

Als erstes werden beim Startscreen alle Variablen, die eine Rolle spielen definiert und das Cover wird sichtbar. 

![Fertiges Projekt Yannick Malte script pic](https://user-images.githubusercontent.com/69623479/101168960-8c04e200-363c-11eb-81e3-2ff5d6ecb15d.png)

![Unbenannt7](https://user-images.githubusercontent.com/69623479/101169530-5f9d9580-363d-11eb-9ffd-a2a3e99beefd.PNG)

Der nächste Schritt ist in die Characterauswahl zu wechseln

![Unbenannt](https://user-images.githubusercontent.com/69623479/101169789-c1f69600-363d-11eb-9fcf-1bb64aa61d97.PNG)

Ist dies geschafft können die Charactere ausgewählt werden und somit die Variable, die später im tatsächlichen Spiel als Flag genutzt wird, definiert werden. 
2 Spieler mit jeweils 2 Auwahlmöglichkeiten:

![Unbenannt2](https://user-images.githubusercontent.com/69623479/101169944-fb2f0600-363d-11eb-843a-59ae513cf092.PNG)

Danach musste der Übergang von Charakterauswahl zu Stageauswahl kommen:

![Unbenannt3](https://user-images.githubusercontent.com/69623479/101169984-0da93f80-363e-11eb-9789-a1202bdd0c7e.PNG)

Und demenstsprechend dann die Stageauswahl, welche wie auch bei den Characteren die Variable, die nach dem Startscreen als Flag genutzt wird defniniert:

![Unbenannt4](https://user-images.githubusercontent.com/69623479/101170281-85776a00-363e-11eb-8903-fe097d83bb3a.PNG)

Hierbei haben wir über das Definieren der Variable für die Stage hinaus um der Ästhetik willen eine kleine Animation eingebaut, auf die wir bei der Characterauswahl verzichtet haben, da eine Animation für alle möglichen Auswahlmöglichkeiten durch beide Spieler flüssig, schnell und bugfrei zu verwirklichen extrem unkompakt gewesen wäre.

Zuguterletzt musste ein Signal kommen mitdem dem Programm klar werden konnte das der Startscreen abgeschlossen ist. Hierfür haben wir einen Broadcast genutzt, welcher nur dann aktiviert werden kann, wenn alle Variablen definiert sind, also die Charactere, sowie Stages ausgewählt sind:

![Unbenannt5](https://user-images.githubusercontent.com/69623479/101170649-0cc4dd80-363f-11eb-93a5-2f460ab61c04.PNG)

#### <a name="2.2.2"></a>Bewegung und die Stage:

Die grundlegend sehr simplen Bewegungscommands zum nach rechts und links Bewegen wurden im Laufe der Entwicklung des Spiels, bzw. der Blöcke/Plattformen in der Stage, mit Flags versehen, um die gewünschte Funktionsweise der Blöcke zu gewährleisten. Die Commands, welche für jegliche Bewegung verantwortlich sind, haben also praktisch gesehen immer eine enge Verbindung, meist in der Form einer Flag, zu den Blöcken der Stage.
Hier ein Beispielcommand für die Bewegung nach links und rechts:

![Unbenannt8](https://user-images.githubusercontent.com/69623479/101173322-a8a41880-3642-11eb-8f5b-f9c5655e0b34.PNG)

Auch die Gravitation begann als eine simple "forever"-Schleife, welche nach und nach mit allen Möglichkeiten die Blöcke zu berühren aufgefüllt wurde. 
Der finale Command, welcher alle Möglichkeiten in der die Gravitation wirken soll beinhaltet sieht so aus:

![unbennant 9](https://user-images.githubusercontent.com/69623479/101173604-0cc6dc80-3643-11eb-84ea-dfbe41e6c2a2.png)

Der Sprung war (damals) eine etwas kompliziertere Angelegenheit, da wir eine Dynamische, relativ realistische Bewegung haben wollten, welche der realen Physik relativ nah kommt.
Dementsprechend erstellten wir eine Variable, welche bestimmt wie schnell der Character springt/fällt, welche während des Sprungs progressiv immer weniger wird, sodass er immer weniger hoch springt bis er schließlich eine negative Beschleunigung hat und somit, bis er den Boden berührt, immer schneller fällt.
Zuletzt fügten wir noch einen Command hinzu, der gewährleistete, dass der Spielcharakter keinsfalls in die Plattformen hinein "fallen konnte", da wenn z.B. der y wert um 10 geändert würde, der Character jedoch nurnoch y=1 vom Boden entfernt ist würde er eben um 9 im Boden stecken. Um dies zu verhindern Fügten wir ein, dass der Character um einen passenden Wert (10) nach oben gesetzt wird, falls er zu tief in den Block fällt:

![Unbenannt10](https://user-images.githubusercontent.com/69623479/101175353-5e706680-3645-11eb-94c5-0a8da922e681.PNG)

Die Letzte Bewegungsfähigkeit im Spiel ist die aktive Fähigkeit von dem Character Gonzales: der Teleport.
Ein simpler Code der einem unter der Bedingung, dass man im Startscreen Gonzales ausgewählt hat, die Fähigkeit gibt einen entsprechenden Wert auf der x-Achse (40) zu überspringen (sich zu teleportieren). Dieser Fähigkeit haben wir darüber hinaus einen Cooldown von 3 Sekunden gegeben.

![Unbenannt11](https://user-images.githubusercontent.com/69623479/101176014-2fa6c000-3646-11eb-9d45-802d8b094e4a.PNG)

Die Blöcke/Plattformen im Spiel bestehen aus 4 Teilen.
Der Block Masse, dem Marker rechts bzw. links und dem Teil oben.
In verschiedenen Situationen erfüllen diese Teile verschiedene Zwecke wie bereits oben erwähnt z.B. beim Sprung. 
Der Hauptzweck ist jedoch, dass man nicht links und rechts in den block reinspringen können sollte. 
Dies wurde mit folgenden Flags, welche das nach rechts/links laufen (wie oben gezeigt) bedingen gemacht:

![unbenannt 17](https://user-images.githubusercontent.com/69623479/101182175-10139580-364e-11eb-96aa-a6e77348384d.png)


#### <a name="2.2.3"></a>Kampfsystem:

Das Kampfsystem dreht sich bis auf die aktive Fähigkeit von dem anderen Character, Alphonzo, ums Schießen.

Die beiden Charactere haben ein unterschiedliches Schussystem.
Alphonzo schießt immer konstant. Die Besonderheit an seinem Schuss ist, dass je weniger Leben er hat, desto mehr Schaden macht er (wie in unserem Konzept "Wut"-> siehe Konzept im Blog).  
Gonzales hat eine "3-Schuss-Waffe". Er feuert also eine Salve bestehend aus 3 Schüssen ab und macht Schaden, sobald mindestens eine dieser 3 Projektile trifft.

Hier ein Beispielcode für ein Projektil (der Laserschuss von Alphonzo; der Code für die Projektile von Gonzales ist der gleiche):

![unbenannt 12](https://user-images.githubusercontent.com/69623479/101178060-d0967a80-3648-11eb-9378-50e37fe7b532.png)

Und der Code für den genommen Schaden:

![unbannt 13](https://user-images.githubusercontent.com/69623479/101178326-28cd7c80-3649-11eb-8047-09e4ab4ad6d0.png)

Der andere Teil des Kampfsystems ist die aktive Fähigkeit von Alphonzo, der Slam.
Die Fähigkeit besteht einmal aus dem Code für die Bewegung und die Defnition der Variable um die Flag zu aktivieren, welche klar macht, dass der Slam benutzt wurde:

![unbennant 14](https://user-images.githubusercontent.com/69623479/101178924-db9dda80-3649-11eb-85be-ffc144e39e02.png)

Und dementsprechend auch Codes für den Einfluss des Slams, nämlich sowohl Schaden, als auch Rückstoß für den getroffenen Gegner:

![unbenannt 16](https://user-images.githubusercontent.com/69623479/101179314-5a931300-364a-11eb-81d0-0c2d20056a04.png)

Zur entsprechenden Funktionsweise des obigen Commands musste die Variable "X position P1 oder P2" noch so definiert werden:

![unbenannt 15](https://user-images.githubusercontent.com/69623479/101179299-57982280-364a-11eb-9ced-e8771027e80f.png)

### <a name="3"></a> Besondere Herausforderungen:

Dem Umfang unseres Projekts entsprechend hatten wir zahlreiche, teils unerklärliche Fehlschläge.
Dies reichte von fehlendem Wissen z.B. beim Sprung, da dies unser erster Kontakt mit Variablen war und wir uns in dieses System entsprechend erst einfinden mussten, bishin zu nach wie vor unerklärlichen Fehlschlägen, wie z.B. beim Abschließen des Startscreens, wo der Letzte teil des Codes aus dem gesamten Block ausgetrennt werden musste um zu funktionieren. Wir mussten bei diesem Fall absoulut nichts am Code ändern, sondern ihn lediglich in eine eigene "forever"-schleife packen und schon funktionierte alles.

Unser größtes Probelem jedoch, welches über Monate ungelößt blieb, aber zuletzt gelößt werden konnte war der Block.
Das ursprüngliche Ziel war zu verhindern, dass man in den Block links oder rechts reinspringen kann und dass man nicht von unten durchspringen kann.
Unser erstes Workaround war den Block mit Farben zu definieren.
Würde der Character eine bestimmte Farbe berühren würde die Gravitation ausgestellt werden.
Dies erfüllte aber nur, dass man auf dem "Block" stehen konnte und war somit keine langfristige Lösung und nicht vollständig unseren Vorstellungen entsprechend.
Schon von Anfang an stellten wir es uns vor, dass es langfristig besser sei, den Block aus Sprites zu machen. 
Dies zu erreichen erforderte jedoch einiges an Können und Verständniss von Snap besonders in Sachen Flags, doch da der Block als ein Grundlegendes Element sowhl eines Jump and Runs, als auch eines Brawl-Games ist hat uns dies schon sehr früh, bevor wir uns die schwereren Teile von Snap ordentlich aneignen konnten beschäftigt und uns somit über einen Langen Zeitraum beschäftigt.
Im Endeffekt haben wir den Block größtenteils so programmierern können, dass er funktionell ist und den Spielfluss in keiner Weise behindert.

### <a name="4"></a>Schlusswort: 

Die Freiheit, die uns beim Arbeiten auf allen Ebenen gegeben wurde war extrem motivierend.
Sich etwas wie das Programmieren mit Snap anzueignen um etwas verwirklichen zu können, dass man sich slebst vorgestellt hatte, wie eben unser Spiel, hat das Arbeiten sehr erleichtert und angenehm gemacht. 
Auch wenn gelegentliche Einschränken durch die Block-Programmiersprache und/oder Bugs beim Arbeiten frustrierend waren, war es früher oder später umso schöner eine Lösung zu finden.
Snap hat sich als eine hervoragende Wahl für uns als Programmieranfänger herausgestellt, da die visuelle Darstellung der Codeschnipsel ein schnelles und sehr logisches zusammenfügen und somit Programmieren ermöglichen.
So konnten wir praktisch komplett ohne Vorwissen einen großen Schritt in die Welt des Programmierens machen.

