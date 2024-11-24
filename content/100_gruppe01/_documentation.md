# Dokumentation GoDot4

## Erstellung Szene + Objekte
- Projekt erstellt und Github-repo aufgesetzt - lief ohne Probleme ab
- Base-Assets "Sci-Fi Pack" ließ sich einfach importieren
- Das originale Barrel-Asset funktionierte nicht
  - Blender-Export schwierig - Doku existiert zwar, haben aber n anderes Asset verwendet
- Barrel-Asset - Problem = es gab kein Material
  - Lösung = neues Material erstellt und die Texturen in die jeweiligen Kategorien reingezogen

- Explosion Particle
  - umgesetzt
  - Szene, die mit mehreren 3d-GPU-Particle nodes
  - bestehen aus Material, Fläche(drawpass), ParticleProcessMaterial
  - Problem: bei Tutorial muss man auf die Aktualität achten

- Drohne
  - glb. dateien sind geeigneter  zum importieren, als die anderen, da Materials schon mit importiert und richtig gesetzt werden.
 
- piston
  - der Boden und das Licht muss wech 
- Fehler bei Strukturen der Pre-Fabs, da Verzeichnisse verschoben wurde

- Level
	- Der Player bleibt auf der stelle stehen und das level bewegt sich auf ihn zu.
	- Weitere Strassen spawnen noch nicht. (Work in progress)
  - Spawner der Level Module funktioniert
  - Basic Steuerung implementiert (Springen & WASD)
    - Musste z Achse locken, damit der Spieler von bewegenden Modulen nicht nach hinten geschoben wird.

- Player
	- Character import und Animations haben kein problem gehabt.
	- Für den import des des Chars und Animations wurde der [Character Animation Combiner](https://nilooy.github.io/character-animation-combiner/) verwendet
  - Animation Tree mit Blend Space angepasst, da vorherige Implementierung zu Problemen beim PlayerController geführt hat

- UI
  - Relativ einfach umgesetzt mit verschiedenen Control Nodes
  - Score Display
  - Leben Display
  - Game Over Display

- Drone
  - Animations in Godot selbst animiert (war einfach) mit AnimationPlayer

- Volumentric Fog
  - Eigenen Shader gecoded (UVW Koordinaten wegen 3D)


