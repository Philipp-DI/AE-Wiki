# M5 Szenarien

## Szenario A: NeuroVision AI (Data Science & ML)

### 1\. Titel & Beschreibung

**NeuroVision AI – Transparenz in der Black Box**

NeuroVision AI ist ein innovatives KI-Startup, das sich auf spezialisierte Bilderkennungssoftware und hochpräzise Empfehlungssysteme fokussiert. Das Team lebt eine hochtechnologische 'Data-First'-Mentalität, bei der datengetriebene Beweise mehr zählen als bloßes Bauchgefühl.

### 2\. Ausgangslage / Herausforderungen

NeuroVision AI hat ein massives Problem mit der Akzeptanz seiner Modelle. Ein wichtiger Enterprise-Kunde (ein riesiger Online-Shop) vertraut dem System nicht mehr, weil niemand im Sales-Team erklären kann, _warum_ Produkt A dem Kunden B empfohlen wird. Das Entwicklungsteam muss nun die zugrundeliegende Mathematik (User-Item-Matrizen und Vektor-Distanzen) transparent machen und kleine, fehlerfreie Prototypen in Python bauen, die diese fundamentalen Berechnungen "im Kleinen" simulieren, bevor sie auf Big Data losgelassen werden.

### 3\. Epic-Kontext

- **Epic 1:** Profil-Vektoren vergleichen, um Ähnlichkeiten zwischen Produkten mathematisch zu beweisen (Kosinus-Ähnlichkeit).
- **Epic 2:** Bild-Filter und Gewichtungen der Empfehlungs-Engine als Matrizen modellieren.
- **Epic 3:** Sensor-Kalibrierungen und Feature-Gewichte über Lineare Gleichungssysteme systematisch ausbalancieren.

## Szenario B: PolyRender Studios (Game Development & 3D)

### 1\. Titel & Beschreibung

**PolyRender Studios – Kampf mit der Physik**

PolyRender Studios ist ein kreatives Spieleentwicklungs-Studio, das eine eigene, leichtgewichtige 3D-Engine für Webbrowser programmiert. Die Unternehmenskultur ist stark visuell geprägt, agil und legt extremen Wert auf absolute Performance bei der Echtzeit-Berechnung.

### 2\. Ausgangslage / Herausforderungen

Die Entwicklung der neuen "Web-Core" Engine stockt gravierend. Objekte in der Spielwelt bewegen sich nicht physikalisch korrekt, Kollisionen werden von der Software völlig falsch oder zu spät berechnet, und die Kamera-Transformationen führen zu stark verzerrten Grafiken, wenn sich der Spieler dreht. Das Team muss dringend zurück zu den mathematischen Wurzeln und die Arithmetik für Bewegung, Raum-Transformationen und Schnittpunkte sauber und performant neu implementieren.

### 3\. Epic-Kontext

- **Epic 1:** Spieler- und Projektilbewegungen als Vektoren im 3D-Raum berechnen.
- **Epic 2:** Rotation, Skalierung und Translation von Polygonen durch Matrix-Multiplikation umsetzen.
- **Epic 3:** Schnittpunkte von "Sicht-Strahlen" (Raycasting) mit Objekten über Lineare Gleichungssysteme berechnen.

## Szenario C: GreenFlow Logistics (Optimierung & Planung)

### 1\. Titel & Beschreibung

**GreenFlow Logistics – Chaos in der Lieferkette**

GreenFlow Logistics ist ein etablierter Dienstleister, der hochkomplexe Lieferketten für die anspruchsvolle Pharmaindustrie optimiert. Das Unternehmen arbeitet extrem strukturiert, kostenbewusst und effizient, da Planungsfehler sofort immense finanzielle Schäden verursachen.

### 2\. Ausgangslage / Herausforderungen

Die gesamte Kapazitäts- und Rohstoffplanung wird derzeit in riesigen, chaotischen Excel-Listen abgewickelt. Diese Listen sind enorm fehleranfällig und stürzen regelmäßig ab. Wenn sich auch nur ein einziges Mischverhältnis in einem Medikament ändert, bricht die gesamte Berechnungskette zusammen. Die Aufgabe ist es nun, die Produktionsprozesse mathematisch absolut exakt zu modellieren, um Materialbedarfe auf Knopfdruck fehlerfrei vorausberechnen zu können.

### 3\. Epic-Kontext

- **Epic 1:** Anforderungs- und Lieferantenprofile als Feature-Vektoren anlegen und "matchen".
- **Epic 2:** Mehrstufige Produktion (Rohstoff -> Baugruppe -> Endprodukt) als verkettete Bedarfsmatrizen (Materialverflechtung) aufstellen.
- **Epic 3:** Exakte Produktionsmengen zur Deckung des Marktbedarfs über Lineare Gleichungssysteme (Gozintograph) ermitteln.