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
