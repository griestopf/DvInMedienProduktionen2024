+++
title = 'Artikel Infos'
date = 2024-09-28T15:40:23+02:00
draft = false
weight = 500

+++

## Gliederung des Artikels

Legende: (***Ü***) - Gruppenübergreifender Abschnitt. (***G***) - von jeder Gruppe zu erstellender Abschnitt.

1. Einleitung (***Ü***)
   - Ziel der Analyse
     - Überblick über Engines, Gemeinsamkeiten und Unterschiede ggf. Empfehlungen
   - Methodik
     - Zweigeteiltes Verfahren: Objektive Tests nach Kategorien PLUS Erfahrungsbericht beim Erstellen eines Beispiel-Game 
	 - Beschreibung der Vorgehensweise

2. Unity (Erfahrungsbericht zur Erstellung eines Endless Runner mit der Engine) (***G***)
   - Facts über Engine
     - Lizenzmodell
     - Verbreitung
   - Benutzerfreundlichkeit, Usability
   - Programmierumgebung, Tools
   - "Grafikqualität"
   - Character Animation
   - Lernkurve
   - Probleme & Lösungen, Eigenheiten
   - Gesamteindruck

3. Unreal (***G***)
   - Struktur wie Unity

4. Godot (***G***) 
   - Struktur wie Unity

5. Vergleich (nach Kategorien)
   - Testkategorien:
	 - Unterstützte Plattformen
	 - Rentabilität/Kosten 
	 - Performance
	   - Rendering (nach u. s. Benchmark)
	   - Physik(nach u. s. Benchmark)
    - TODO
      - Tests durchführen und Messwerte/Ergebnisse generieren (***G***)
 	   - Messwerte zusammenfassen und tabellarisch darstellen (***Ü***)

6. Fazit
   - Stärken/Schwächen der Engine ((***G***) - Stichwortartig erfassen; (***Ü***) Zusammentragen und als Kapitel niederschreiben)
   - Empfehlungen ((***G***) - Stichwortartig erfassen; (***Ü***) Zusammentragen und als Kapitel niederschreiben)

5. Anhang (***G***)

## Zuordnung der gruppenübergreifenden (***Ü***) Abschnitte

| Abschnitt                                | Gruppe   |
|------------------------------------------|----------|
| 1 Einleitung/Ziel der Analyse              | Gruppe 1 |
| 6 Fazit/Stärken & Schwächen                | Gruppe 1 |
| 1 Einleitung/Methodik                      | Gruppe 2 |
| 6 Fazit/Empfehlungen                       | Gruppe 2 |
| 5 Vergleich (Zusammenfassung, Tabelle, Kapitel schreiben) | Gruppe 3 |



## Specs Physik-Benchmark

- Becken mit Kugeln Füllen (eine Kugel pro Millisekunde)
- Abbruch, wenn Frame-Time (Delta) > 100 ms (Framerate <= 10 FPS)
- Messergebnis: Wieviele Kugeln sind bis dahin instanziiert?
- World-Aufbau:
	- Dimension Becken: 20x20 m (Units)
	- Kugelradius 0.25 m; (Durchmesser 0,5 m)
	- Kamera-Position über Becken, senkrecht nach unten blickend
	- Kamera-Öffnungswinkel 60°
	- Kamera-Abstand so, dass oberer und unterer Beckenrand jewwils am oberen und unteren Bildschirmrand liegen
   - Renderfenster Full-HD: 1920 x 1080
   - Test als exportierte Windows-Applikation. Ausgabe des Ergebnis möglichst 
     ohne Ausgabe im Renderfenster während des Testlaufs.



## Specs Rendering-Benchmark

### Anfangszustand
Kamera Distanz Ursprung: 15
Initiale Kamera Höhe: 1
Rotationsdauer: 2 Sekunden
Start Grid Größe: `11*11`
Lücke zwischen Blöcken: $1$
Block Größe: `1*1`
#### **1. Wachsendes Gitter (Layer-basiert)**

Das Gitter wächst in Schichten, wobei jede Schicht ein Quadrat von Blöcken enthält. Mit jeder neuen Schicht wird die Größe des Gitters um eine zusätzliche Reihe und Spalte vergrößert.

**Code-Snippet für das Erstellen von Blöcken in einer Schicht**:

In Unity könnte dies so aussehen:

```csharp
private void GenerateLayer()
{
    float halfGridSize = startingSquareGridSize / 2.0f;
    float startX = -halfGridSize * blockSpacing + blockSpacing / 2.0f;
    float startZ = -halfGridSize * blockSpacing + blockSpacing / 2.0f;

    for (int i = 0; i < startingSquareGridSize; i++)
    {
        for (int j = 0; j < startingSquareGridSize; j++)
        {
            Vector3 spawnPos = new Vector3(startX + j * blockSpacing, 1.0f + _currentLayer * blockSpacing, startZ + i * blockSpacing);
            Instantiate(spawnObject, spawnPos, Quaternion.identity);
        }
    }

    _nBlocks += startingSquareGridSize * startingSquareGridSize;
    startingSquareGridSize++;  // Grid wächst mit jeder Schicht
    _currentLayer++;           // Schicht wird erhöht
}
```

#### **Erläuterung**:

- **`startingSquareGridSize`** ist die Größe des Gitters in der aktuellen Schicht.
- **`blockSpacing`** gibt den Abstand zwischen den Blöcken in der Schicht an.
- Mit `Instantiate()` werden die Blöcke in den gewünschten Positionen erstellt.
- Am Ende jeder Schicht wird die Größe des Gitters um eins erhöht (`startingSquareGridSize++`).

#### **2. Kamera-Management**

Die Kamera rotiert um das Zentrum des Gitters. Sie bleibt immer auf das Zentrum des Gitters ausgerichtet und bewegt sich in einem festen Abstand um die Struktur. Die Höhe der Kamera wird ebenfalls angepasst, um das wachsende Gitter zu berücksichtigen.

**Code-Snippet für Kamerabewegung und Rotation**:

```csharp
private void UpdateCamera()
{
    _angle += (360.0f / rotationTime) * Time.deltaTime;

    float dynamicCameraDistance = cameraDistance + _currentLayer * blockSpacing * _camPositionMultiplier;
    float x = dynamicCameraDistance * Mathf.Cos(_angle * Mathf.Deg2Rad);
    float z = dynamicCameraDistance * Mathf.Sin(_angle * Mathf.Deg2Rad);
    float y = cameraHeight + (_currentLayer * blockSpacing);

    _mainCamera.transform.position = new Vector3(x, y, z);
    _mainCamera.transform.LookAt(new Vector3(0.0f, y, 0.0f));  // Kamera schaut immer auf das Zentrum des Gitters
}
```
#### **Erläuterung**:

- Der **`_angle`** steuert die Rotation der Kamera um das Zentrum des Gitters.
- **`cameraDistance`** und **`cameraHeight`** definieren den Abstand und die Höhe der Kamera.
- Die Kamera bewegt sich in einem Kreis um das Zentrum des Gitters (`x`, `y`, `z`), wobei der Abstand dynamisch an die Schichtgröße angepasst wird.

#### **3. Leistungsmonitoring**

Die Leistung wird gemessen, indem die Anzahl der Blöcke (`_nBlocks`) und die durchschnittliche Frame-Zeit (`frameTime`) pro Schicht angezeigt werden. Dies gibt einen Überblick darüber, wie sich die Performance mit jeder hinzugefügten Schicht verändert.

**Code-Snippet für Leistungsmonitoring und Ausgabe**:

```csharp
void Update()
{
    _nFrames++;
    _timeDeltas += Time.deltaTime * 1000;  // Delta-Zeit in Millisekunden

    if (_angle >= 360.0f)
    {
        GenerateLayer();  // Neue Schicht generieren
        _angle = 0.0f;
        
        // Berechnung der durchschnittlichen Frame-Zeit
        float frameTime = _timeDeltas / _nFrames;
        print("Layer " + (_currentLayer + 1) + " (" + _nBlocks + " blocks visible) / Avg frame time: " + frameTime);

        // Reset der Zähler für die nächste Schicht
        _timeDeltas = 0.0f;
        _nFrames = 0;
    }

    UpdateCamera();  // Kamera regelmäßig aktualisieren
}
```

#### **Erläuterung**:

- **`_nFrames`** zählt die Anzahl der Frames pro Schicht.
- **`_timeDeltas`** speichert die Zeitdeltas (Frame-Zeiten) für die Berechnung der durchschnittlichen Frame-Zeit.
- Am Ende einer vollen Rotation (wenn `_angle >= 360.0f`), wird die **durchschnittliche Frame-Zeit** ausgegeben, und die Blockanzahl wird angezeigt.

#### **4. Dynamische Anpassung der Kamera**

Da das Gitter wächst, muss die Kamera ihre Position dynamisch anpassen, um das gesamte Gitter weiterhin sichtbar zu halten. Dazu wird der **Kameradistanz**-Wert basierend auf der Anzahl der Schichten und dem Abstand zwischen den Blöcken angepasst.

**Code-Snippet für die dynamische Anpassung der Kamera**:

```csharp
private void UpdateCamera()
{
    _angle += (360.0f / rotationTime) * Time.deltaTime;

    // Dynamische Anpassung der Kamera-Entfernung
    float dynamicCameraDistance = cameraDistance + _currentLayer * blockSpacing * _camPositionMultiplier;
    
    float x = dynamicCameraDistance * Mathf.Cos(_angle * Mathf.Deg2Rad);
    float z = dynamicCameraDistance * Mathf.Sin(_angle * Mathf.Deg2Rad);
    float y = cameraHeight + (_currentLayer * blockSpacing);

    _mainCamera.transform.position = new Vector3(x, y, z);
    _mainCamera.transform.LookAt(new Vector3(0.0f, y, 0.0f));  // Immer auf das Zentrum des Gitters ausrichten
}
```
#### **Erläuterung**:

- Der **`dynamicCameraDistance`** wird mit jeder neuen Schicht erhöht, um sicherzustellen, dass die Kamera genug Abstand hat, um das wachsende Gitter vollständig anzuzeigen.
- Die Kamera bleibt dabei immer auf das Zentrum des Gitters ausgerichtet.

---

#### **5. Generierung der ersten Schicht**

Die erste Schicht wird mit einer festgelegten Anzahl an Blöcken erstellt, die durch **`startingSquareGridSize`** definiert wird. Diese Blöcke werden in einem Gitter angeordnet, wobei der Abstand zwischen den Blöcken durch **`blockSpacing`** bestimmt wird.

**Code-Snippet für die Generierung der ersten Schicht**:

```csharp
private void GenerateLayer()
{
    float halfGridSize = startingSquareGridSize / 2.0f;
    float startX = -halfGridSize * blockSpacing + blockSpacing / 2.0f;
    float startZ = -halfGridSize * blockSpacing + blockSpacing / 2.0f;

    for (int i = 0; i < startingSquareGridSize; i++)
    {
        for (int j = 0; j < startingSquareGridSize; j++)
        {
            Vector3 spawnPos = new Vector3(startX + j * blockSpacing, 1.0f + _currentLayer * blockSpacing, startZ + i * blockSpacing);
            Instantiate(spawnObject, spawnPos, Quaternion.identity);
        }
    }

    _nBlocks += startingSquareGridSize * startingSquareGridSize;  // Anzahl der Blöcke wird erhöht
    startingSquareGridSize++;  // Gittergröße wächst
    _currentLayer++;           // Schicht wird erhöht
}
```
#### **Erläuterung**:

- **`startingSquareGridSize`** gibt die Anzahl der Blöcke pro Seite des Gitters in der aktuellen Schicht an.
- Mit **`Instantiate()`** wird jeder Block in einer Position innerhalb des Gitters erzeugt.
- **`_nBlocks`** wird nach jeder Schicht aktualisiert, um die Gesamtzahl der generierten Blöcke zu verfolgen.``