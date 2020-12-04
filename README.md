# Projektseite

1 [Einleitung/Vision](#1)    

2 [Das Programm](#2)
     
2.1      [Beschreibung des Programms](#2.1)
     
2.2      [Wie Funktionieren die Einzelteile?](#2.2)
     
3 [Besondere Herausforderungen](#3)  

4 [Schlusswort](#4)  


### <a name="1"></a>Einleitung/Vision:
"Brawl of Alphonzo and Gonzales" ist das Ergebniss unserer ersten Programmiererfahrung.
Was als ein Plattformer begann entwickelte sich nach kurzer Zeit zu einem Brawl-Game in dem zwei Spieler als 2 Charactere (Alphonzo, Gonzales) auf einer von 2 Stages Gegeneinander Kämpfen.
Wir beide hatten uns schon vor dem Beginn des Informatikunterrichts sehr kurz mit dem Programieren auseinandergesetzt. Die Anfängerfreundlichkeit aber dennoch große Bandbreite an Möglichkeiten von Snap war uns schon im Vorhinein bekannt, sowie auch die Schwierigkeit einer richtigen Programmiersprache für einen Anfänger. 
Von daher war die Entscheidung für ein Snap-Projekt schnell gefallen.
Den Vorkentnissen entsprechend war die erste Idee ein Jump and Run Spiel.
Wir eigneten uns das Programmieren mit Snap von 0 an und entwickelten so, dank des anfängerfreundlichen Aufbaus der Block-Programmiersprache, die ersten Grundlagen für ein Spiel.
Es dauerte nicht allzulang, bis wir bemerkten das uns ein J&R spiel sehr limitieren würde, denn Level zu designen hatte 1. relativ wenig mit Programmieren sondern mehr mit design zu tun und vor allem wäre das Spiel relativ kurz, denn ein Paar J&R Level durchzuspielen ist schnell passiert.
Beim betrachten der Grundlagen die bereits vorhanden waren fiel uns auf, dass alles was wir bis zu diesem Zeitpunkt gemacht hatten nicht nur auf einen Plattformer passen würde sondern auch auf ein Brawlgame (wie z.B. Smash Brothers, Duck Game oder Brawlhallah).
Der größte Vorteil eines solchen Spiels gegenüber eines Plattformers ist selbstverständlich das er kompetitiv ist/sein kann. Spielen 2 Spieler gegeneinander in einem tatsächlich Skill-basierten Spiel wäre die Spielzeit nicht so limitiert wie in einem J&R, da man immer weiter üben könnte.
Außerdem wirkten die Möglichkeiten das Spiel zu Programmieren z.B. in Sachen fähigkeiten wie dem Schuss deutlich reizvoller als die Blöcke für das nächste Level eines Jump and Runs an den richtigen Ort zu bringen.
Dementsprechend begannen wir das Spiel in ein Brawlgame umzuentwickeln.

### <a name="2"></a>Das Programm:

### <a name="2.1"></a>Beschreibung des Prgramms: 
Startet man das Spiel erscheint der Startscreen.
Durch die Visuell angegebenen Zahlen, welche denen auf der Tastatur entsprechen wird man durch die Startscreens geleitet, in welchen die Spieler ihren Character und ihre gewünschte Stage auswählen.
Hat man dies abgeschlossen, so Spawnt man und der Kampf beginnt.
Mithilfe ihrer Waffe und ihrer Individuellen Fähigkeit gilt es nun die Leben des Gegners von 100 auf 0 zu bringen.
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

Ist dies geschafft können die Charactere ausgewählt werden und somit die Variable die später, im tatsächlichen Spiel als Flag genutzt wird, definiert werden. 
2 Spieler mit jeweils 2 Auwahlmöglichkeiten:

![Unbenannt2](https://user-images.githubusercontent.com/69623479/101169944-fb2f0600-363d-11eb-843a-59ae513cf092.PNG)

Danach musste der Übergang von Charakterauswahl zu Stageauswahl kommen:

![Unbenannt3](https://user-images.githubusercontent.com/69623479/101169984-0da93f80-363e-11eb-9789-a1202bdd0c7e.PNG)

und demenstsprechend dann die Stageauswahl, welche wie auch bei den Characteren die Variable die nach dem Startscreen als Flag dient defniniert:

![Unbenannt4](https://user-images.githubusercontent.com/69623479/101170281-85776a00-363e-11eb-8903-fe097d83bb3a.PNG)

hierbei haben wir über das Definieren der Variable für die Stage hinaus um der Ästhetik willen eine kleine Animation eingebaut auf die wir bei der Characterauswahl verzichtet haben, da eine Animation für alle möglichen Auswahlmöglichkeiten durch beide Spieler flüssig, schnell und bugfrei zu verwirklichen extrem unkompakt gewesen wäre.

Zuguterletzt musste ein Signal kommen mit dem Programm klar werden konnte das der Startscreen abgeschlossen ist. Hierfür haben wir einen Broadcast genutzt, welcher nur dann aktiviert werden kann wenn alle Variablen definiert sind, also die Charactere, sowie Stages ausgewählt sind:

![Unbenannt5](https://user-images.githubusercontent.com/69623479/101170649-0cc4dd80-363f-11eb-93a5-2f460ab61c04.PNG)

#### <a name="2.2.2"></a>Bewegung und die Stage:



#### <a name="2.2.3"></a>Kampfsystem:

### <a name="3"></a> Besondere Herausforderungen:

### <a name="4"></a>Schlusswort: 
