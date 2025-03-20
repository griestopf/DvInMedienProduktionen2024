+++
title = 'Game Engine Vergleich'
date = 2024-09-28T15:40:23+02:00
draft = false
weight = 600

+++


Hier soll der gesamte Artikel zusammengeführt werden. 


Ein Beispiel-Bild:
![Example Image](images/example_image.png)

## Einleitung
Die Wahl der richtigen Game-Engine spielt eine entscheidende Rolle bei der Entwicklung von Computerspielen und beeinflusst sowohl die Effizienz des Arbeitsprozesses als auch die Qualität des Endprodukts. In diesem Bericht untersuchen wir drei der bekanntesten und am weitesten verbreiteten Game-Engines: Godot, Unreal Engine und Unity. Durch eine detaillierte Analyse möchten wir ihre Eigenschaften sowie die dazugehörigen Stärken und Schwächen aufzeigen, um Entwicklern und Interessenten eine fundierte Entscheidungsgrundlage zu bieten.
   
### Ziel der Analyse
Die Analyse konzentriert sich auf zentrale Aspekte wie Benutzerfreundlichkeit, technische Leistungsfähigkeit, Tool-Unterstützung und die Entwicklungsumgebung. Darüber hinaus spielt die Eignung der Engines für bestimmte Projekte – wie zum Beispiel das Entwickeln von Spielen, Simulationen, Software etc. – eine wesentliche Rolle. Neben der theoretischen Bewertung stellen wir daher auch praktische Erfahrungen vor, um einen praxisnahen Einblick in die Stärken und Schwächen der Engines zu geben. Unsere Ergebnisse sollen sowohl für professionelle Entwicklerteams als auch für Einzelpersonen nützlich sein, die sich in der Planung oder Umsetzung ihrer Projekte befinden. Durch die Ergebnisse unserer Arbeiten, möchten wir nicht nur technische Unterschiede aufzeigen, sondern auch Empfehlungen geben, welche Engine sich für spezifische Anwendungen und Anforderungen besonders eignet. Ziel ist es, einen umfassenden und zugleich verständlichen Überblick zu bieten, der eine informierte Entscheidung ermöglicht.

### Methodik
Um die Leistungsfähigkeit und Benutzerfreundlichkeit verschiedener Game Engines zu analysieren, haben wir zwei verschiedene Verfahren angewendet. Dieses umfasst sowohl objektive, messbare Tests als auch subjektive Erfahrungsberichte, die während der Entwicklung eines Beispielprojekts gewonnen wurden. Ziel ist es, die Stärken und Schwächen der Engines zu evaluieren und eine fundierte Grundlage für Empfehlungen bereitzustellen. Dabei haben wir zum Einen verschiedene objektive Tests nach bestimmten Kategorien durchgeführt und zum Anderen ein Beispielprojekt in Form eines Endless Runner entiwckelt. Die Kategorien waren: 

**Physik-Benchmark:**
	Ein rechteckiges Becken (20 × 20 Meter) wird kontinuierlich mit Kugeln gefüllt, die pro Sekunde nacheinander instanziiert werden. Die Simulation wird beendet, sobald die Frame-Time (Delta) 100 ms überschreitet, was einer Framerate von ≤ 10 FPS entspricht. Das Messergebnis gibt an, wie viele Kugeln instanziiert werden konnten, bevor die Leistungsgrenze erreicht wurde.

Der Szenenaufbau beinhaltet:
- Beckenabmessungen: 20 × 20 Meter.
- Kugelradius: 0,05 Meter (Durchmesser: 0,1 Meter).
- Kameraposition: Senkrecht über dem Becken zentriert.
- Kamera-Öffnungswinkel: 60°.
- Kameraabstand: So gewählt, dass das Becken den oberen und unteren Bildschirmrand vollständig ausfüllt.

![Physik Benchmark](images/image_PhysikBenchmark.png)

**Grafik-Benchmark:**
	Zur Überprüfung der Grafikleistung wird ein Turm aus Blöcken schrittweise aufgebaut. Dabei wird in jeder Iteration das Grid um eine Spalte und eine Reihe vergrößert, wodurch die Gesamtanzahl der Blöcke exponentiell ansteigt. Eine Kamera, die um den Mittelpunkt des Turms rotiert, stellt sicher, dass möglichst viele Flächen gerendert werden. Der Test endet, wenn die Frame-Time 100 ms überschreitet. Das Messergebnis gibt an, wie groß der Turm (in Blockanzahl) wird, bevor die Leistungsgrenze erreicht wird.

Der Szenenaufbau beinhaltet:
- Die Kamera bleibt zentriert auf den Turm ausgerichtet und rotiert um diesen herum.
- Turm wird pro Iteration um eine Spalte und Reihe vergrößert

![Grafik Benchmark](images/image_GrafikBenchmark.png)

Die Benchmarks wurden mit der folgenden Hardware getestet:

#### CPU
- **Modell:** 12th Gen Intel® Core™ i9-12900H  
- **Taktfrequenz:** 2,9 GHz  
- **Kerne:** 14  
- **Logische Prozessoren:** 20  
- **Arbeitsspeicher:** 32 GB RAM  

#### GPU
- **Modell:** NVIDIA GeForce RTX 3080 Ti (Laptop)  
- **Videospeicher:** 16 GB GPU-RAM  

#### Bildschirmauflösung
- **Auflösung:** 2560 × 1600  


Neben den Benchmarks wurde ein Endless-Runner-Spiel entwickelt, um die Engines unter praxisnahen Bedingungen zu testen. Das Projekt umfasst wesentliche Spielelemente wie prozedural generierte Levelabschnitte und verschiedene Gameplay Mechaniken wie Laufen und Springen.

Die Entwicklung des Projekts diente dazu, qualitative Eindrücke über die Benutzerfreundlichkeit, die Arbeitsabläufe und die Lernkurve der jeweiligen Engines zu sammeln. Aspekte wie die Zugänglichkeit der Dokumentation, die Effizienz der Entwicklungsumgebung und die Eignung der Engines für ein prozedurales Spiel wurden hierbei bewertet.
Die gewonnenen Ergebnisse aus den Benchmarks und der Entwicklung des Endless Runners wurden miteinander kombiniert, um eine ganzheitliche Bewertung zu ermöglichen. Damit konnten sowohl die technische Leitungs, als auch die praktischen Vor- und Nachteile geschickt erfasst werden.

Mit diesem Verfahren wird sicher gesellt, dass die Analyse sowohl fundierte, datenbasierte Einblicke bietet, als auch die Erfahrungen der Teams und der tatsächlichen Entwicklung berücksichtigt.


## Unity

### Die Engine

Unity bietet verschiedene Lizenzmodelle an, darunter kostenlose und kostenpflichtige Versionen. Eine Runtime-Gebühr wurde angekündigt, jedoch nach massiven Beschwerden der Community wieder verworfen.
         
Zum einen gibt es die "Personal"-Version, also die kostenfreie Version. Diese ist ideal für Einsteiger, da selbst kein Geld investiert werden muss und trotz allem die grundlegenden Funktionen wie Echtzeit-Entwicklung, Startbildschirm-Anpassung und der Unity Asset Manager verfügbar sind.

Die Pro-Version ist ab 1.877€ im Jahr erhältlich und eignet sich für profesionelle Entwickler. Es werden zusätzliche Features wie ein erweiterter Langzeit-Support und ein größerer Asset Manager angeboten.

"Enterprise" ist auf große Teams und Firmen ausgerichtet. Diese Version umfasst Pro-Features und zusätzliche Optionen wie Build-Server-Lizenzen und einen vollen Zugriff auf den Quellcode. 

Bei der Industry-Lizenz ist der Fokus auf Unternehmen in spezifischen Branchen gelegt und es werden branchenspezifische Toolkits angeboten.

Unity ist vor allem für 2D- und VR-Anwendungen weit verbreitet. Dank einer starken Community bietet die Engine zahlreiche Ressourcen, die den Einstieg und die Weiterentwicklung erleichtern. 
Die offizielle [Unity-Dokumentation](https://docs.unity3d.com/Manual/index.html) bietet eine umfassende Übersicht über die Funktionen und Möglichkeiten der Engine. Für Einsteiger und Fortgeschrittene gibt es zudem [Unity Learn](https://learn.unity.com/). Zusätzlich kann über Youtube, Reddit und anderen Plattformen viele Anleitungen und Tipps gefunden werden. Wer allerdings gezielte Unterstützung sucht, kann im [Unity-Forum](https://discussions.unity.com/) und Plattformen wie Reddit nach Hilfe fragen.


### Benutzerfreundlichkeit, Usability
Die Benutzeroberfläche von Unity ist übersichtlich gestaltet und bietet eine Vielzahl an Werkzeugen, die eine flexible Anpassung an unterschiedliche Projekte ermöglichen. Für Einsteiger kann die Fülle an Funktionen anfangs überwältigend wirken, doch dank umfangreicher Tutorials kann der Einstieg immens erleichtert werden.
Ein gutes Beispiel ist das Partikelsystem. Mit einer Anleitung konnte etwa ein explodierendes Fass problemlos erstellt werden, während es ohne Tutorial aufgrund der zahlreichen Parameter und Optionen deutlich schwieriger gewesen wäre. Die hohe Flexibilität und Anpassungsfähigkeit der Engine sind beeindruckend, gehen jedoch mit einer gewissen Lernkurve einher.

### Programmierumgebung, Tools
Unity verwendet C# als Programmiersprache und unterstützt gängige IDEs wie Visual Studio, Visual Studio Code und Rider. Auch Debugging und Profiling sind mit den integrierten Tools realisierbar. Diese ermöglichen detaillierte Analysen, wie z.B. die Nutzung des Profilers zur Überprüfung der Frame-Time.
    ![Profiler](images/image_Profiler.png)
Zusätzlich wird Visual Scripting unterstützt, wobei diese Methode weniger verbreitet ist als herkömmliches C#-Scripting. Dennoch bietet sie eine Möglichkeit für Entwickler ohne tiefgehende Programmierkenntnisse, ihre Spiele mechanisch zu erweitern.

### Grafikqualität
Die visuelle Darstellung in Unity hängt maßgeblich von der gewählten Renderpipeline ab. Die Built-in Render Pipeline ist die Standardlösung, die eine solide Basis bietet, jedoch in ihrer Leistungsfähigkeit für moderne Effekte begrenzt ist. Eine optimierte Alternative stellt die Universal Render Pipeline (URP) dar, die besonders für mobile Geräte und leistungsschwächere Plattformen entwickelt wurde, ohne dabei auf eine ansprechende Grafikqualität zu verzichten. Wer realistische visuelle Effekte erzielen möchte, kann auf die High Definition Render Pipeline (HDRP) setzen, benötigt dafür jedoch leistungsstarke Hardware.

In unserem Endless-Runner-Projekt mit prozedural generierten Levels überzeugte Unity mit flüssigen Übergängen und einer ansprechenden Darstellung. Die Engine ermöglicht zahlreiche Anpassungen für Shader und visuelle Effekte, sodass Entwickler die Grafikqualität gezielt anpassen und optimieren können.

### Character Animation
Unity bietet mit dem Animator ein leistungsstarkes Tool zur Steuerung von Animationen. Die State-Machine ermöglicht komplexe Übergänge zwischen Animationen, wobei Übergangszeiten und Bedingungen individuell angepasst werden können.

Bei der Nutzung von Mixamo für Charakteranimationen stellte sich heraus, dass Mixamo keinen direkten Export von Animationen erlaubt. Die Lösung bestand darin, die Animationen aus dem Import in Unity zu extrahieren und anschließend im Animator zu verwenden.
Das Ragdoll-System von Unity bietet zwar eine solide Grundlage für physikbasierte Animationen, weist jedoch einige Einschränkungen auf. Es gibt keine automatische Erkennung von Bones, was das manuelle Setup erfordert. Zudem ist ein nahtloser Übergang zwischen Animation und Ragdoll-Physik nicht direkt möglich. Dieses Problem konnte mit einem Ragdoll-Enabler-Skript aus einem [YouTube-Tutorial](https://www.youtube.com/watch?v=RB18IyKZiB0) behoben werden.

### Lernkurve
Dank der umfassenden Ressourcen wie Unity Learn und der großen Community gestaltet sich der Einstieg in Unity relativ einfach. Für fortgeschrittene Themen, etwa das Partikelsystem oder Animationen, sind jedoch oft zusätzliche Tutorials erforderlich. 
Insgesamt bietet Unity eine moderate Lernkurve, wobei die hohe Anzahl an Funktionen eine gewisse Einarbeitungszeit erfordert.

### Probleme & Lösungen, Eigenheiten
Beim Import von 3D-Modellen traten Probleme auf, insbesondere beim Importieren von .blend-Dateien ohne installiertes Blender. Zudem war das manuelle Extrahieren und Zuweisen von Texturen erforderlich. Eine effektive Lösung bestand darin, stattdessen .fbx-Dateien zu verwenden, um den Workflow reibungsloser zu gestalten.

Im Bereich der Ragdolls zeigte sich, dass die automatische Erkennung von Bones nicht zuverlässig funktioniert, was ein manuelles Setup notwendig machte. Außerdem ist der Übergang von Animationen zu Ragdoll-Physik nicht nativ möglich. Dieses Problem konnte jedoch durch den Einsatz eines Ragdoll-Enabler-Skripts behoben werden.

Bei der Arbeit mit Mixamo-Animationen stellte sich der Export mehrerer Animationen als problematisch heraus. Die Lösung bestand darin, die Animationen manuell zu extrahieren und sie anschließend in den Animation Controller einzubinden.

### Gesamteindruck
Unity ist eine äußerst vielseitige Engine mit einer breiten Palette an Funktionen, die sowohl für Anfänger als auch für erfahrene Entwickler geeignet ist. Besonders hervorzuheben sind die starke Community und die umfangreiche Dokumentation, die den Einstieg erleichtern und bei Problemen schnell Lösungen bieten.

Für unser Endless-Runner-Projekt erwies sich Unity als eine ausgezeichnete Wahl, da die Engine prozedurale Levelgenerierung, komplexe Animationen und leistungsfähige Grafikpipelines unterstützt. Trotz einiger Herausforderungen, insbesondere beim Import von 3D-Modellen und Animationen, konnten diese Probleme durch gezielte Lösungen bewältigt werden. Die anschließende Erstellung der Web-Anwendung war überraschend einfach. Dank der benutzerfreundlichen Tools und mithilfe dieses [Youtube-Tutorials](https://www.youtube.com/watch?v=X8Njwk4IRo0) konnte einfach und schnell eine Web-Anwendung erstellt werden.

![EndlessRunner Unity](images/image_EndlessRunner_Unity.png)

Mit diesem Link kann die Anwenung selbst getestet werden: [Endless Runner Unity](https://play.unity.com/en/games/8c5831da-319c-47af-a985-51e2100a43b4/webbuild).

Unity bietet eine starke Basis für verschiedenste Projekte und bleibt eine der führenden Engines für die Spielentwicklung. Entwickler, die bereit sind, sich in die Vielzahl der Funktionen einzuarbeiten, können mit Unity beeindruckende Ergebnisse erzielen.


## Unreal

### Die Engine
Die Unreal Engine 5 (UE5) von Epic Games ist eine der leistungsstärksten 3D-Entwicklungsplattformen. Sie glänzt besonders durch High-End-Grafik, ermöglicht durch Nanite (virtuelle Geometrie) und Lumen (Echtzeit-Global-Illumination). Die Engine ist bis zu einem Jahresumsatz von einer Million US-Dollar kostenfrei nutzbar; darüber hinaus fällt eine Umsatzbeteiligung von fünf Prozent an. Dies ist für kleine und mittlere Projekte attraktiv, kann jedoch für umsatzstarke Produktionen schnell teuer werden.

### Benutzerfreundlichkeit, Usability
Unreal Engine 5 bietet eine moderne Oberfläche und vielfältige Funktionen, setzt für effizientes Arbeiten jedoch eine leistungsfähige Hardware voraus. Einsteiger finden die Fülle an Einstellungen anfangs oft verwirrend. Viele Funktionen sind tief verschachtelt, weshalb man sich intensiver einarbeiten muss als etwa in Unity oder Godot. Unser Team stieß zum Beispiel auf Konfigurationshürden bei Material-Instanzen und den Projekteinstellungen. Mit offiziellen Tutorials und Dokumentationen ließen sich diese jedoch lösen.

Für das Endless-Runner-Projekt haben wir uns hauptsächlich auf Blueprints konzentriert, da diese eine schnelle Umsetzung ermöglichen, ohne direkt in den Code eingreifen zu müssen. Trotz der Vorteile können Blueprints in komplexen Projekten schnell unübersichtlich werden, weshalb eine saubere Strukturierung und Namenskonventionen besonders wichtig sind.

### Programmierumgebung, Tools
Unreal Engine bietet zwei Hauptwege zur Entwicklung von Gameplay:
- **Blueprints**: Ein visuelles Scripting-System, das schnelle Prototypen ohne tiefere Programmierkenntnisse erlaubt.
- **C++**: Für komplexe oder besonders performante Anwendungen wird C++ eingesetzt, das allerdings anspruchsvoller ist.

Der Editor unterstützt Hot Reload, sodass Codeänderungen in vielen Fällen ohne Neustart übernommen werden können. In unserem Projekt zeigten sich hierbei jedoch gelegentliche Fehler, die teils einen Editor-Neustart erforderten.

Für Tests und Benchmarks erwies sich die Einrichtung teils als aufwändig. Beispielsweise verlangte das ständige Instantiieren und Verwalten von Objekten in Echtzeit (z. B. für einen Physik-Benchmark) ein tieferes Verständnis von Actor-Klassen und Kollisionskanälen.

### Grafikqualität
Die Grafikfunktionen der Unreal Engine 5 gehören zu den modernsten im Markt:
- **Nanite**: Eignet sich für extrem detaillierte Meshes, die ohne manuelles LOD-Handling gerendert werden können.
- **Lumen**: Bietet dynamische globale Beleuchtung, wodurch Szenen realistisch wirken.

Für unseren Endless-Runner, der keine fotorealistischen Assets nutzte, waren diese Features teils überdimensioniert. Wer jedoch hohen Wert auf realitätsnahe 3D-Umgebungen legt, wird mit Unreal Engine 5 hervorragend bedient.

In unserem Endless Runner war die Grafik zwar eher schlicht gehalten, aber wir konnten einige interessante Shader-Effekte umsetzen. Besonders das "Curved World"-Feature, bei dem die Spielwelt optisch gekrümmt wird, war ein spannendes Experiment mit dem Material-Editor. Durch die Nutzung einer Material Parameter Collection (MPC) konnten wir verschiedene Parameter wie Krümmungsradius und Intensität anpassen, was zu einem einzigartigen Look führte.

![Material_1](images/Material_Function.png "Dieser Screenshot zeigt den Curved World Shader im Material-Editor. Durch mathematische Berechnungen und Parametersteuerung wird der Spielfluss optisch gekrümmt, sodass die Umgebung eine kontinuierliche Biegung erhält. Dies trägt zur visuellen Dynamik des Endless Runners bei.")
![Material_2](images/Material_Function_settings.png)


### Character Animation
Die Engine verfügt über komplexe Animationswerkzeuge, darunter Animation Blueprints, State Machines und Retargeting. Dadurch können Animationen von unterschiedlichen Skeletten übernommen werden. 
Für die Charakteranimation wurde ein Modell von Mixamo genutzt. Mixamo bietet eine große Auswahl an vorgefertigten Animationen, die sich leicht in Unreal importieren lassen. Allerdings gab es einige Schwierigkeiten beim Retargeting der Animationen, da die Skelettstrukturen von Mixamo nicht 1:1 mit dem Unreal-Standard-Mannequin übereinstimmen.
Um dieses Problem zu lösen, mussten wir eine Retargeting-Session innerhalb von Unreal durchführen, in der die Knochen korrekt zugeordnet wurden. Danach konnten wir die Lauf-, Sprung- und Rutschanimationen problemlos in unser Spiel integrieren. Besonders das Sliding-Feature war eine Herausforderung, da die Kapsel-Kollision des Charakters angepasst werden musste, um das Untergleiten von Hindernissen zu ermöglichen.

![Charac](images/Character_Animation_1.png "Diese Screenshots zeigen die Retargeting-Session in Unreal Engine. Da das Mixamo-Skelett nicht direkt mit dem Unreal-Mannequin kompatibel ist, wurde eine Knochenanpassung durchgeführt. Dadurch können die Mixamo-Animationen für Laufen, Springen und Rutschen korrekt auf den Charakter übertragen werden.fehlerhaft sein.")
![Charac](images/Character_Animation_2.png)


### Lernkurve
Unreal Engine 5 erfordert eine steile Einarbeitung. Blueprints sind ein schneller Einstieg für Prototypen, doch für umfassende Projekte ist fundiertes C++-Wissen ratsam. Wer aus anderen Engines kommt, muss sich zudem auf das komplexe Projekt-Setup und die Editor-Struktur einstellen. Dennoch gibt es eine große Menge an Lernmaterial: Offizielle Dokumentation, Community-Foren, YouTube-Kanäle und kostenpflichtige Kurse helfen beim Einstieg.

### Probleme & Lösungen, Eigenheiten

#### Fehlender Web-Export
In älteren Versionen gab es einen offiziellen Web-Export. Mit UE4 wurde er eingestellt, was Entwicklern nur noch die Option ließ, „Pixel Streaming“ oder externe Lösungen zu nutzen. In UE5 fehlt diese Option vollständig. Das Fehlen des Web-Exports ist für viele Projekte ein Nachteil, wenn Browser-Unterstützung benötigt wird.

#### Implementierung der Benchmarks
Unsere Benchmarks sollten Framezeiten, Objektinstanzierungen und andere Metriken erfassen. Ein Problem war die fehlende Möglichkeit, umfangreiche Daten direkt in eine Konsole oder Log-Datei auszugeben, sobald das Projekt exportiert ist. Stattdessen stellt Unreal On-Screen-Statistiken und hauseigene Logs bereit, die für automatisierte Testverfahren aber nur bedingt geeignet sind.

#### Kameramanagement
Die Kamera in Unreal Engine 5 ist an einen Player-Controller geknüpft. Eine statische oder frei rotierende Kamera ließ sich nur schwer ohne zusätzliche Keyframe-Animationen realisieren. Da wir Benchmarks in Echtzeit ausführen wollten, benötigten wir jedoch eine feste Kameraperspektive. Cine Cameras sind zwar mächtig, aber eher für vorgerenderte Sequenzen ausgelegt, was automatisierte Tests erschwerte.

#### Physik-Benchmarks
Für unseren Physik-Benchmark waren mehrere Projekteinstellungen nötig. Kollisionskanäle, Sub-Level-Strukturen und Physikprofile gestalteten sich komplexer als erwartet.

#### UAssets und Versionskontrolle
Weil Unreal Assets in binären Dateien (UAssets) gespeichert werden, können Merge-Konflikte in Git oder anderen Versionskontrollen schwer zu lösen sein. Um dies zu vermeiden, braucht es sorgfältige Arbeitsabläufe und die Aufteilung der Projektbereiche.

#### Herausforderungen: Endless Runner
Bei der Entwicklung des Spiels kam es zu Herausforderungen, sei es durch die Mechanik/Physik, der Grafischendarstellung oder auch die Kamera Einstellungen.

Ein Beispiel für eine Herausforderung war die Optimierung des Straßen-Spawn-Systems. Ursprünglich wurden zu viele Straßenabschnitte gleichzeitig geladen, was zu Performance-Problemen führte. Die Lösung war die Implementierung eines Kollisionstriggers: Sobald der Spieler eine neue Plattform betritt, wird eine neue Straße generiert und die alte gelöscht. Dies sorgte für eine effiziente Verwaltung der Level-Elemente.

![Probleme](images/Problem_Lernkurve_1.png)
![Probleme](images/Problem_Lernkurve_2.png "Dieser Screenshot zeigt die Blueprint-Logik für das Erstellen und Entfernen der Straßenabschnitte. Das System sorgt dafür, dass immer nur eine bestimmte Anzahl an Plattformen existiert, indem neue Straßen generiert und alte entfernt werden, sobald der Spieler voranschreitet. Dies optimiert die Performance und verhindert, dass sich unnötige Objekte im Speicher ansammeln.")

Ein weiteres Problem trat bei der Rutschmechanik auf. In der ersten Version konnte der Charakter zwar eine Slide-Animation ausführen, aber die Kollision verhinderte das tatsächliche Durchrutschen unter Hindernissen. Hier mussten wir die Kapsel-Kollision des Charakters dynamisch anpassen und nach der Animation wieder auf die Standardgröße zurücksetzen.

![Probleme](images/Problem_Lernkurve_3.png "Hier wird die Implementierung der Rutschmechanik in Blueprints dargestellt. Der Charakter wechselt in die Slide-Animation, wenn der Spieler die entsprechende Taste drückt. Gleichzeitig wird die Kapsel-Kollision des Charakters vorübergehend verkleinert, um ein realistisches Durchrutschen unter Hindernissen zu ermöglichen. Nach der Animation kehrt die Kollision zur ursprünglichen Größe zurück.")
![Probleme](images/Problem_Lernkurve_4.png)

Ein zusätzliches Problem war die Kameraeinstellung. Die Kamera sollte den Charakter flüssig verfolgen, ohne dass abrupte Bewegungen auftreten. Dafür wurde ein Kamera-Blueprint erstellt, der die Bewegung interpoliert und sich dynamisch an den Spurwechsel anpasst.

![Probleme](images/Problem_Lernkurve_5.png "Der Screenshot zeigt die Implementierung der dynamischen Kamerasteuerung. Die Kamera folgt dem Charakter mit einer sanften Verzögerung und passt sich automatisch an Spurwechsel und Sprünge an. Dies sorgt für ein flüssiges Spielerlebnis, ohne abrupte Bewegungen oder ruckartige Wechsel in der Kameraposition.")

Das Power-Up-System wurde so integriert, dass der Spieler temporäre Vorteile wie einen Magnet-Effekt oder höhere Sprünge erhalten kann. Die Power-Ups erscheinen zufällig in der Spielwelt und werden über ein Widget im HUD angezeigt.

![Probleme](images/Problem_Lernkurve_6.png)
![Probleme](images/Problem_Lernkurve_7.png)

Der gespeicherte Highscore wird in einer Datei im Slot „SaveGame“ abgelegt, sodass die besten Punktestände erhalten bleiben. Dies ermöglicht es, die Punktzahlen auch nach einem Spielende wieder abzurufen.

![Probleme](images/Problem_Lernkurve_8.png "Nach dem Spielende wird der Highscore auf dem Game-Over-Bildschirm angezeigt. Falls der Spieler einen neuen Rekord aufgestellt hat, wird dieser gespeichert und mit zukünftigen Runden verglichen. Das System nutzt eine SaveGame-Klasse, um den Punktestand dauerhaft zu sichern.")
![Probleme](images/Problem_Lernkurve_9.png "Funktion Veränderung des HUD")
![Probleme](images/Problem_Lernkurve_10.png "Funktion Veränderung des HUD")
![Probleme](images/Problem_Lernkurve_11.png "Funktion Veränderung des HUD")
![Probleme](images/Problem_Lernkurve_12.png "Funktion Veränderung des HUD")



### Gesamteindruck
Unreal Engine 5 zählt zu den leistungsfähigsten Engines für hochwertige 3D-Projekte und bietet dank Nanite und Lumen Top-Grafik. Sie ist ideal für ambitionierte Spieleentwicklungen oder interaktive Echtzeitvisualisierungen, wenn genügend Hardwareressourcen verfügbar sind. Allerdings ist die Einstiegshürde hoch, und das Fehlen einer aktuellen Web-Export-Lösung kann sich für bestimmte Projekte als kritisch erweisen.

Die Entwicklung eines Endless Runners mit Unreal Engine war eine spannende Erfahrung, die uns viele Einblicke in die Funktionsweise der Engine gegeben hat. Besonders positiv ist die Flexibilität der Engine: Dank Blueprints konnten wir viele Mechaniken schnell umsetzen, ohne tief in C++ einsteigen zu müssen. Die Grafikqualität und die verfügbaren Tools sind auf einem sehr hohen Niveau, was Unreal zu einer idealen Wahl für ambitionierte Projekte macht.

Für rein 2D-basierte Spiele oder extrem einfache Prototypen wirkt Unreal oft überdimensioniert. Dort sind andere Engines (z. B. Godot oder Unity) meist schneller eingerichtet. Wer jedoch an AAA-Qualität oder großen Projekten interessiert ist, findet in UE5 eine mächtige, wenn auch komplexe Entwicklungsumgebung.

Insgesamt sind wir sehr zufrieden mit dem Endergebnis. Der Endless Runner funktioniert stabil, und wir konnten viele interessante Features wie zufällige Hindernis-Generierung, Power-Ups und ein Highscore-System implementieren. Unreal Engine hat sich als leistungsfähige und vielseitige Entwicklungsplattform erwiesen.


## Godot
![Godot Endless Runner Main Menu Image](Godot_ER_mainmenu.png)
![Godot Endless Runner Image](Godot_ER.png)

### Die Engine
Die Godot Engine, welches 2014 veröffentlicht wurde, ist eine MIT - lizensierte Open-Source Engine. Die MIT-Lizenz erlaubt es die Software frei zu nutzen, zu modifizieren und zu verteilen, solange der ursprüngliche Lizenztext beibehalten wird. Sie bietet zudem keinen Haftungsausschluss für Schäden. Godot wird von einer aktiven Community sowie einem Kernteam kontinuierlich weiterentwickelt. Godot unterstützt sowohl 2D- als auch 3D-Spieleentwicklung, wobei der Fokus besonders auf der 2D- Performance liegt, allerdings gab es bereits schon wesentliche Fortschritte im 3D - Bereich. Die Engine bietet eine umfassende Plattformunterstützung und erlaubt die Veröffentlichung von Spielen auf Windows, macOS, Linux, Android, iOS und Konsolen. Ein Alleinstellungsmerkmal von Godot ist das integrierte Szenensystem, das Spielelemente hierarchisch organisiert und den Entwicklungsprozess stark vereinfacht.

### Benutzerfreundlichkeit, Usability
Godot zeichnet sich durch eine intuitive Benutzeroberfläche und ein klar strukturiertes Layout aus, das sowohl für Einsteiger als auch für erfahrene Entwickler leicht verständlich ist. Besonders die Drag- and-Drop-Funktionalität und der Node-basierte Aufbau tragen dazu bei, dass die Engine schnell erlernt werden kann. Tutorials und Dokumentationen sind gut verfügbar, wobei die Community eine Vielzahl zusätzlicher Ressourcen bereitstellt. Ein Nachteil könnte jedoch die kleinere Community im Vergleich zu Unity oder Unreal darstellen, was die Verfügbarkeit spezifischer Plugins oder Lösungen einschränken könnte. 

### Programmierumgebung, Tools
Die Programmierung in Godot erfolgt primär mit der hauseigenen Skriptsprache GDScript, die Python-ähnlich ist und sich durch ihre Einfachheit und Lesbarkeit auszeichnet. Alternativ unterstützt Godot auch C# und externe Skriptsprachen. Die integrierte Entwicklungsumgebung (IDE) bietet viele hilfreiche Funktionen wie einen eingebauten Code-Editor, Debugging-Tools und ein Live-Update-System, mit dem Änderungen sofort getestet werden können. Besonders hervorzuheben ist die Modularität der Engine: Entwickler können problemlos eigene Plugins und Erweiterungen integrieren, um den Entwicklungsprozess weiter zu optimieren. Dabei zu beachten, ist, dass nicht alle Plugins auf den neusten Stand gehalten werden, da viele von ihnen kostenlos angeboten werden und es auf eine freiwillige Tätigkeit basiert und der finanzielle Anreiz fehlt. Zusätzlich kann man die Engine modifizieren mithilfe von C++.

### Grafikqualität
Mit der Einführung des Vulkan-Renderers in Version 4.3 hat Godot erhebliche Fortschritte erzielt. Vulkan ermöglicht moderne Rendering-Technologien wie realistische Lichteffekte, dynamische Schatten, High Dynamic Range (HDR), Global Illumination und Screen-Space Reflections, die die visuelle Darstellung deutlich verbessern. Dennoch wurden in einigen Fällen Performance-Einbußen festgestellt, insbesondere bei der Verwendung von OmniLight3D-Schatten, was auf eine erhöhte Anzahl von Draw Calls zurückzuführen ist. 

### Character Animation
Godot bietet umfangreiche Tools für Animationen, darunter den AnimationPlayer und den AnimationTree, die komplexe Animationsabläufe ermöglichen. Skeletale Animationen lassen sich einfach importieren und bearbeiten. Mit Blend Spaces und State Machines können fließende Übergänge zwischen Animationen realisiert werden. Dennoch wurden in der Community Performance-Probleme bei Animationen diskutiert, insbesondere im Vergleich zu anderen Engines. Allerdings kam es in unserem Projekt nicht zu Performance Problemen bezüglich der Animationen.

### Lernkurve
Godot zeichnet sich durch eine intuitive Benutzeroberfläche und ein flexibles Node-basiertes System aus, was besonders für Einsteiger den Einstieg erleichtert. Die Skriptsprache GDScript, die Python-ähnlich ist, ermöglicht einen einfachen und schnellen Start in die Spieleentwicklung. Alternativ bietet Godot Unterstützung für C#. Die umfangreiche Dokumentation und eine aktive Community bieten zusätzliche Hilfestellung. Der Umstieg von anderen Engines kann jedoch aufgrund der einzigartigen Konzepte von Godot anfangs herausfordernd sein. Es ist wichtig zu beachten, dass Visual Scripting in Godot 4 entfernt wurde, da es wenig genutzt wurde und der Wartungsaufwand hoch war. Es gibt jedoch Community-Plugins wie "Orchestrator", die ähnliche Funktionalitäten bereitstellen. 

### Probleme & Lösungen, Eigenheiten
Ein bekanntes Problem der Godot Engine betrifft die Physics Engine, insbesondere im 3D-Bereich. Die Kollisionserkennung und die Physikberechnungen sind nicht immer präzise, was oft zusätzliche Optimierungen erfordert. Auch der Asset-Import, vor allem aus Blender, kann problematisch sein, insbesondere bei Materialien und Texturen. Bei der Shader - Programmierung gab es Performance - Probleme. Diese wurden durch Anpassungen an den Einstellungen in der Godot Engine selbst und der Nodes behoben.

### Gesamteindruck
Die Godot Engine 4.3 ist eine Open-Source-Spielentwicklungsumgebung, die sowohl 2D- als auch 3D-Spielentwicklung unterstützt. Sie wird unter der MIT-Lizenz vertrieben, was Entwicklern maximale Freiheit bietet, den Code anzupassen und zu verteilen. Godot hat eine wachsende Community und ist besonders bei Indie-Entwicklern beliebt, da es kostenlos und leicht zugänglich ist. 

Die Engine ist bekannt für ihre benutzerfreundliche Oberfläche und das Node-basierte System, das die Strukturierung von Projekten erleichtert. Godot bietet eine integrierte Entwicklungsumgebung (IDE) mit einem umfassenden Toolset, einschließlich eines visuellen Editors und einer relativ einfach zu verstehenden Script-Sprache namens GDScript, die besonders gut auf die Engine angepasst ist. Es unterstützt auch C# und C++. 

Die Grafikqualität in 3D scheint akzeptabel zu sein, jedoch konnten wir in diesem Projekt nicht tief darauf eingehen. Animationen lassen sich einfach importieren und bearbeiten. Die Engine verfügt über integrierte Tools wie den AnimationPlayer, um Animationen direkt in der Engine zu erstellen. Die Lernkurve ist moderat. Für Anfänger gibt es viele Tutorials und eine aktive Community, die Unterstützung bietet. 

Es gibt einige Herausforderungen, insbesondere mit der Physics Engine von Godot 4.3. In unserem Fall, bei der Entwicklung eines kleinen 3D-Spiels, stellte sich heraus, dass die Physics Engine nicht besonders akkurat und performant ist. Diese Schwierigkeiten erforderten zusätzliche Anpassungen und Optimierungen, um die gewünschte Funktionalität zu erreichen. Insgesamt bietet die Godot Engine 4.3 jedoch eine robuste und vielseitige Plattform für Spieleentwickler, die bereit sind, sich in die Engine einzuarbeiten und individuelle Lösungen für spezifische Herausforderungen zu finden. 

### Referenzen
- [Github Godot Benchmark](https://github.com/Schnike/GodotBenchmark)
- [Godot WEB-Export](https://schnike.itch.io/space-mouse)

## Vergleich von Unreal Engine, Unity und Godot

## Vergleich von Unreal Engine, Unity und Godot

Im Folgenden finden sich die wichtigsten Eckdaten zu den drei Engines in tabellarischer Form. Die Angaben zur **Performance** basieren auf Beispiel-Benchmarks (Rendering/Physik) in einer Testumgebung mit folgendem System:

- **CPU:** 12th Gen Intel(R) Core(TM) i9-12900H, 2,90 GHz (14 Kerne / 20 Threads)  
- **RAM:** 32 GB  
- **GPU:** NVIDIA GeForce RTX 3080 Ti Laptop GPU (16 GB VRAM)  
- **Auflösung:** 2560 × 1600  

### Performance und Physik-Evaluation
Die Ergebnisse wurden anhand von Rendering-Benchmarks (Anzahl darstellbarer Objekte, bevor die Framerate unter 10 FPS fällt) und Physik-Benchmarks (instanziierte Kugeln oder Blöcke bis zum Erreichen einer kritischen Frame-Time von 100 ms) ermittelt.

| **Kategorie**               | **Unreal Engine**                                                              | **Unity**                                                                             | **Godot**                                                                                      |
|-----------------------------|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| **Lizenzmodell**            | Kostenfrei bis 1 Mio. USD Umsatz, dann 5 % Umsatzbeteiligung                  | Personal (kostenlos), Pro ab 1.877 €/Jahr; Enterprise für große Teams                  | Open Source (MIT), kostenfrei                                                                  |
| **Unterstützte Plattformen**| PC, Konsolen, VR/AR (kein offizieller Web-Export seit UE4/UE5)                | PC, Konsolen, Mobile, VR/AR, Web (HTML5)                                              | PC, Mobile, Konsolen, Web (HTML5 per Export)                                                   |
| **Rendering-Benchmark**     | Keine Daten vorhanden          | Layer 139: ca. 1.113.390 Blöcke, Frame Time ~102 ms                                    | Objektanzahl 203.275; im Frame ~101.024 Objekte                                               |
| **Physik-Benchmark**        | Keine Daten vorhanden          | 11.584 Kugeln, danach Frame Time ≥100 ms                                               | 8.757 Instanzen, davon 1.502 aktive 3D-Physikobjekte                                           |
| **Community & Ressourcen**  | Große AAA-Community, sehr aktive Foren, Blueprint + C++-Support               | Sehr verbreitet, riesiger Asset Store, unzählige Tutorials (YouTube, Foren etc.)       | Wachsende Community, gute Dokumentation, jedoch weniger Plugins/Assets als Unity/Unreal        |
| **Grafik-Funktionen**       | High-End-Features (Nanite, Lumen), hohe Hardware-Anforderungen                | Versch. Render-Pipelines (URP, HDRP, Built-In), skalierbar, eher moderater Bedarf      | Vulkan ab Godot 4.x, weitere Optimierungen in Arbeit, 3D-Funktionalität wird ständig verbessert |
| **Einsatzbereich**          | AAA / High-End-3D-Projekte, aufwendige visuelle Umsetzungen, steile Lernkurve | Sehr flexibel (2D, 3D, VR), eignet sich für Indie bis AA/AAA, relativ zugänglicher Einstieg | Besonders stark in 2D und Prototyping, Open Source, für 3D weiterentwickelt, aber teils weniger performant |


**Hinweise zu den Messwerten**  
- Die **Rendering-Benchmarks** prüfen, wie viele Objekte (Blöcke, Meshes o. Ä.) gerendert werden können, bevor die Bildrate unter einen praxisrelevanten Grenzwert sinkt.  
- Die **Physik-Benchmarks** messen, wie viele Instanzen (z. B. Kugeln) erzeugt werden können, bevor die Frame-Time 100 ms (unter 10 FPS) überschreitet.  


## Fazit
   
### Stärken/Schwächen
Unity bietet eine große und aktive Community mit zahlreichen Hilfestellungen über YouTube, Reddit und andere Foren. Zudem gibt es viele Open-Source-Ressourcen sowie einen umfangreichen Asset Store mit zahlreichen Inhalten. Die Engine ist äußerst flexibel und unterstützt eine Vielzahl von Plattformen und Betriebssystemen. Ihre umfangreichen Tools erleichtern die Entwicklung erheblich. Allerdings gestaltet sich die Implementierung von Ragdoll-Physik als komplex, und das UI-System gilt als umständlich.

Godot punktet durch seine Open-Source-Natur und die Tatsache, dass keine Lizenzgebühren anfallen. Die intuitive Oberfläche und das Node-basierte System ermöglichen eine benutzerfreundliche Projektstrukturierung. Die eigens für die Engine entwickelte Skriptsprache GDScript ist leicht verständlich und besonders für Entwickler mit Programmiererfahrung schnell erlernbar. Zudem bietet Godot eine breite Plattformunterstützung, eine integrierte Entwicklungsumgebung und sehr gute Dokumentation. Trotz dieser Vorteile weist die Engine einige Schwächen auf: Die Physics Engine kann in 3D-Projekten ungenau und leistungsschwach sein, was Optimierungen erfordert. Auch der Asset-Import, insbesondere von Blender-Modellen, kann problematisch sein. Zudem ist die Rendering-Leistung in aufwendigen 3D-Projekten nicht herausragend, und schlecht integrierte Plugins können zu Problemen führen.

Unreal Engine überzeugt mit herausragender Grafikqualität, dank moderner Technologien wie Nanite, Lumen und Echtzeit-Raytracing. Das Blueprint-System ermöglicht visuelle Programmierung, sodass auch Entwickler ohne tiefgehende C++-Kenntnisse komplexe Mechaniken erstellen können. Zudem ist die Engine Open Source, was individuelle Anpassungen erlaubt. Die Lizenzpolitik ist für kleinere Studios vorteilhaft, da erst ab einem Umsatz von einer Million Dollar Lizenzgebühren anfallen. Unreal unterstützt zahlreiche Plattformen, bietet eine starke Community und leistungsstarke Physik- sowie KI-Systeme. Allerdings erfordert die Engine leistungsfähige Hardware und hat eine steile Lernkurve, insbesondere für Anfänger. Die hohe Dateigröße und langen Ladezeiten können problematisch sein, ebenso wie die geringe Optimierung für 2D-Spiele. Zudem kann die Engine für kleine Projekte überdimensioniert sein, und Updates können bestehende Projekte beeinträchtigen. Das Lizenzmodell mit einer Umsatzbeteiligung von 5 % ist für erfolgreiche kommerzielle Spiele ein möglicher Nachteil.

#### Unity
- Stärken:
    - Gute Community mit vielen Hilfestellungen via YouTube, Reddit und anderen Foren
    - Viele Open Source Ressourcen
    - Eigener Asset Store mit viele Inhalten
    - Weitreichende Platformunterstützung
    - Flexibilität bei Betriebssystemen 
    - Umfangreiche Tools, die die Entwicklung vereinfachen
- Schwächen: 
    - Komplexe Ragdoll-Implementierung
    - UI System ist umständlich
 
      
#### Unreal Engine
##### Stärken
- **High-End-Grafik**  
  Durch Technologien wie Nanite und Lumen ermöglicht die Engine fotorealistische Darstellung und dynamische Beleuchtung für qualitativ hochwertige 3D-Projekte.
- **Blueprints & C++**  
  Mit dem visuellen Scripting-System (Blueprints) ist ein schneller Einstieg möglich. Wer mehr Leistung und Flexibilität benötigt, kann auf C++ umsteigen.
- **Umfangreiche Tools & Integration**  
  Eine breite Palette an Entwicklertools (z. B. Animation Blueprints, Visual Effects, KI) und die enge Verzahnung mit professionellen Film- und TV-Produktionspipelines machen Unreal vielseitig einsetzbar.
- **Große Community & AAA-Referenzen**  
  Dank zahlreicher Foren, Tutorials und Marketplace-Inhalte findet man schnell Lösungen, Beispielcode und Assets. Viele AAA-Studios setzen auf Unreal, was den Bekanntheitsgrad steigert.

##### Schwächen
- **Steile Lernkurve**  
  Die Engine ist sehr mächtig und umfangreich. Einsteiger müssen mit erheblicher Einarbeitungszeit rechnen, besonders bei der C++-Programmierung.
- **Hohe Systemanforderungen**  
  Um die Vorteile von Nanite und Lumen auszuschöpfen, wird eine leistungsfähige Hardware vorausgesetzt. Auch der Editor selbst gilt als ressourcenintensiv.
- **Kein offizieller Web-Export**  
  Anders als bei Unity oder Godot bietet Epic seit UE4/UE5 keine offizielle Möglichkeit mehr, Projekte direkt für das Web zu exportieren. Externe Lösungen wie Pixel Streaming bieten nur einen begrenzten Ersatz.
- **Binäre Asset-Dateien (UAssets)**  
  Diese können in Versionskontrollsystemen zu Konflikten führen, da Merge-Tools häufig nicht mit Binärdateien umgehen können. Für Teamprojekte erfordert das eine durchdachte Arbeitsorganisation.


#### Godot
##### Stärken 
- **Open-Source und kostenlos:** Keine Lizenzgebühren oder Einschränkungen bei der Nutzung.
- **Benutzerfreundlichkeit:** Intuitive Oberfläche und ein Node-basiertes System, das die Projektstrukturierung erleichtert.
- **GDScript:** Eine einfach zu erlernende Script-Sprache, die gut auf die Engine angepasst ist und für Entwickler mit Programmiererfahrung leicht verständlich ist.
- **Plattformübergreifend:** Unterstützung für zahlreiche Plattformen, einschließlich Windows, macOS, Linux, Android, iOS, HTML5 und mehr.
- **Integrierte Entwicklungsumgebung (IDE):** Umfassendes Toolset, einschließlich visueller Editor und Debugging-Tools.
- **2D- und 3D-Unterstützung:** Flexible Entwicklungsmöglichkeiten sowohl für 2D- als auch für 3D-Projekte.
- **Community und Support:** Eine aktive Community und zahlreiche Tutorials und Ressourcen, die den Einstieg erleichtern.
- **Dokumentation:** Sehr gute und auch offline verfügbare Dokumentation.
- **Anpassbarkeit:** Einfacher Zugang zum Quellcode ermöglicht tiefgreifende Anpassungen und Erweiterungen der Engine.
- **Plugins:** Vielzahl verfügbarer Plugins, die die Funktionalität der Engine erweitern können.

##### Schwächen 
- **Physics Engine:** In 3D-Projekten kann die Physics Engine ungenau und leistungsschwach sein, was zusätzliche Optimierungen erfordert.
- **Asset-Import:** Probleme beim Import von Blender-Assets und anderen Modellen, insbesondere im Hinblick auf Materialien und Texturen.
- **Rendering-Leistung:** In 3D-Projekten kann die Rendering-Leistung akzeptabel, aber nicht herausragend sein, was bei umfangreicheren Projekten zu Einschränkungen führen könnte.
- **Plugins:** Obwohl Plugins eine positive Erweiterung darstellen, können sie Probleme verursachen, wenn sie nicht sorgfältig integriert werden.

### Empfehlungen

#### Unity
**Spieleentwicklung**

Unity ist besonders auf 2D-Entwicklungen ausgelegt und bietet leistungsstarke Werkzeuge dafür. Durch das integrierte Partikelsystem und den Sprite-Renderer lassen sich damit detaillierte 2D-Spiele erstellen. Zudem unterstützt Unity 3D-Entwicklungen mit verschiedenen Renderpipelines. Hierbei ist allerdings anzumerken, dass Unreal Engine die bessere Wahl für 3D-Spiele ist. Darüber hinaus ist Unity eine der führenden Engines für Virtual Reality (VR) und Augmented Reality (AR). 

**Anwendungen und Tools**

Unity unterstützt eine Vielzahl von Plattformen, darunter PC, Konsolen, Mobile und Web.

**Lern- und Bildungstools**

Unity bietet mit [Unity Learn](https://learn.unity.com/), YouTube-Tutorials und einer aktiven Community viele Einstiegsmöglichkeiten für Anfänger. Zudem wird Unity oftmals in Bildungseinrichtungen genutzt, um Programmierkonzepte praxisnah zu vermitteln.

#### Unreal Engine
**Spieleentwicklung**

Unreal Engine ist bekannt für seine beeindruckende Grafikqualität und eignet sich besonders für aufwendige 3D-Projekte. Die Engine nutzt hierzu fortgeschrittene Beleuchtungs- und Rendering- Technologien. Zudem arbeitet Unreal mit einem Blueprint-System, also einer visuellen Skriptsprache, mit der besonders Entwickler ohne tiefgehende Programmierkenntnisse leicht Spiele entwickeln können.

**Anwendungen und Tools**

Unreal bietet erstklassige Rendering-Technologien, die nicht nur für Spiele, sondern auch für Architekturvisualisierungen und Filmproduktionen genutzt werden. Zudem wird eine integrierte Lösung für realistische Charaktermodelle und KI-gestützte Animationen geboten.

**Lern und Bildungstools**

Die Community bietet zahlreiche Ressourcen, um die visuelle Programmierung mit Blueprints zu erlernen. Außerdem ist Unreal für Lernzwecke und kleinere Projekte kostenlos nutzbar.

#### Unity

- Unity kann besonders gut für 2D Spiele oder VR-Anwendungen empfohlen werden. Auch 3D-Entwicklungen sind möglich. Diese können aber bei grafisch anspruchsvollen Spielen nicht mit anderen Engines mithalten. Auch Erwähnenswert ist die starke Community, die mit verschiedensten Tools, Addons und Tutorials die Spieleentwicklung enorm erleichtern. Zudem ist Unity eine budgetfreundliche Option die zudem eine breite Plattformunterstützung bietet.

#### Unreal

##### Spieleentwicklung
- **High-End-3D-Spiele**: Die Unreal Engine ist besonders für groß angelegte 3D-Projekte mit fotorealistischer Grafik geeignet. Nanite (virtuelle Geometrie) und Lumen (dynamische globale Beleuchtung) sorgen für beeindruckende visuelle Ergebnisse und machen die Engine zum Favoriten bei AAA-Titeln.  
- **Prototyping größerer Projekte**: Dank Blueprints lassen sich Mechaniken rasch umsetzen, ohne tiefgreifende Programmierkenntnisse. Für komplexe, rechenintensive Funktionen bietet C++ zusätzliche Performance und Flexibilität.

##### Anwendungen und Tools
- **Architekturvisualisierung und Simulationen**: Unreal eignet sich hervorragend für interaktive Simulationen oder begehbare Architekturrundgänge. Die hohe Grafikqualität und vielseitigen Physik-Features ermöglichen detailgetreue, immersive Szenen.  
- **Film- und TV-Produktionen (Virtual Production)**: Die Engine hat sich im Bereich Virtual Production etabliert. Echtzeit-Rendering und Integration mit professionellem Filmequipment schaffen beeindruckende virtuelle Sets.

##### Lern- und Bildungstools
- **Blueprints als Einstieg**: Das visuelle Scripting-System erlaubt Einsteigern einen schnellen Zugang zu den Grundmechaniken, ohne sich zunächst in C++ einarbeiten zu müssen.  
- **Umfangreiche Ressourcen**: Offizielle Dokumentationen, Video-Tutorials und eine große Community bieten zahlreiche Lernmaterialien. Fortgeschrittene Themen wie Shader-Programmierung und Netzwerkfeatures werden ebenfalls detailliert behandelt.  
- **Community-Projekte**: Zahlreiche Indie-Projekte und GitHub-Repositories liefern praktische Beispiele, um verschiedene Genres und Anwendungsfälle zu erforschen.


#### Godot
**Spieleentwicklung** 

Godot ist besonders stark in der 2D-Spieleentwicklung. Die Engine bietet eine Fülle von Tools, um 2D-Spiele effizient und effektiv zu erstellen, einschließlich eines visuellen Editors, der die Arbeit mit Sprites, Tilesets und Animationen erleichtert. Während die Engine historisch eher auf 2D-Spiele fokussiert war, hat die 4.3-Version erhebliche Verbesserungen in der 3D-Entwicklung mit sich gebracht. Die Engine bietet nun bessere Rendering-Fähigkeiten, Shader-Unterstützung und eine Vielzahl von Tools, um 3D-Welten zu erschaffen.
Durch die benutzerfreundliche Oberfläche und Skripting-Tools eignet sich Godot hervorragend für das schnelle Prototyping von Spielideen.

**Anwendungen und Tools** 
Godot kann für die Entwicklung von interaktiven Anwendungen und Tools verwendet werden, die auf verschiedenen Plattformen laufen, einschließlich Desktop, Mobile und Web.

**Lern- und Bildungstools** 
Die Engine ist aufgrund ihrer Zugänglichkeit und der umfassenden Dokumentation eine großartige Wahl für Bildungseinrichtungen und Lernende, die in die Spielentwicklung einsteigen möchten. Die Engine bietet eine ideale Plattform, um grundlegende Konzepte der Programmierung und Spieleentwicklung zu erlernen.

## Anhang

### Referenzen


1. Unity Technologies, „Unity Lizenzmodelle,“ Unity, 2025. [Online]. Verfügbar: https://unity.com/de/products/compare-plans.
1. Unity Technologies, „Unity-Dokumentation,“ Unity, 2025. [Online]. Verfügbar: https://docs.unity3d.com/Manual/index.html.
1. Unity Technologies, „Unity-Forum,“ Unity Discussions, 2025. [Online]. Verfügbar: https://discussions.unity.com/.
1. Unity Technologies, „Unity Learn,“ Unity Learn, 2025. [Online]. Verfügbar: https://learn.unity.com/.
1. [DA LAB], „[Create and Publish WebGL Build in Unity],“ YouTube, 2025. [Online]. Verfügbar: https://www.youtube.com/watch?v=X8Njwk4IRo0
1. [LlamAcademy], „[Ragdolls - Creation, Transitioning to, and Optimization | Unity Tutorial],“ YouTube, 2025. [Online]. Verfügbar: https://www.youtube.com/watch?v=RB18IyKZiB0.
1. [Unreal Engine 5 – Offizielle Dokumentation](https://docs.unrealengine.com/5.0/en-US/)  
2. [Unreal Engine Lizenzmodell](https://www.unrealengine.com/en-US/release)  
3. [Blueprint Visual Scripting](https://docs.unrealengine.com/5.0/en-US/blueprints-visual-scripting-in-unreal-engine/)  
4. [Nanite in Unreal Engine 5](https://docs.unrealengine.com/5.0/en-US/nanite-in-unreal-engine/)  
5. [Lumen in Unreal Engine 5](https://docs.unrealengine.com/5.0/en-US/lumen-in-unreal-engine/)  
6. [Pixel Streaming Informationen (Community Plugin)](https://docs.unrealengine.com/5.0/en-US/pixel-streaming-in-unreal-engine/)
1. [Godot Dokumentation Referenz](https://docs.godotengine.org/de/4.x/index.html)
1. [Godot Endless Runner Referenz](https://gameidea.org/2024/10/01/making-3d-endless-runner-game-part-1/)
