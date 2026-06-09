# M2- Mengenlehre & diskrete Mathematik

# Zusammenfassung

Willkommen zu unserem Lernmodul „Mengenlehre & Grundlagen der Diskreten Mathematik“! Auf den ersten Blick wirkt Mengenlehre sehr theoretisch, doch sie ist das unsichtbare Fundament unzähliger IT-Systeme – von Datenbanken über Netzwerke bis hin zu Benutzerrechten. In diesem Modul schlagen wir die Brücke von abstrakten mathematischen Konzepten zu ganz konkreten, praxisnahen Aufgaben eines Fachinformatikers. Wir starten spielerisch mit LEGO, um die Logik zu verinnerlichen, und wenden unser Wissen dann direkt auf eine realistische PostgreSQL-Datenbank an, um mit SQL mächtige Datenanalysen durchzuführen. Am Ende werdet ihr nicht nur wissen, was ein `INNER JOIN` ist, sondern auch, warum er auf den Prinzipien der Mengenlehre beruht.

# Welche Kernkompetenzen erwerben wir?

Nach Abschluss dieses Moduls sind wir in der Lage:

- **Abstraktes Denken zu operationalisieren**: Wir können die Konzepte der Mengenlehre (z.B. Menge, Teilmenge, Relation) nutzen, um reale IT-Systeme wie Benutzergruppen oder Datenbankstrukturen präzise zu beschreiben und zu modellieren.
- **Theorie in Code zu übersetzen**: Wir können die Äquivalenz zwischen Mengenoperationen (Schnittmenge, Vereinigung, Differenz) und den entsprechenden SQL-Befehlen (`INTERSECT`/ `JOIN`, `UNION`, `EXCEPT`) herstellen und zur Lösung praktischer Datenprobleme anwenden.
- **Datenbanken tiefgreifend zu verstehen**: Wir können das Schema einer relationalen Datenbank als System mathematischer Abbildungen interpretieren und dieses Wissen nutzen, um komplexe, tabellenübergreifende Abfragen (Joins) logisch korrekt zu formulieren.
- **Datengetriebene Entscheidungen zu ermöglichen**: Wir können die Ergebnisse unserer mengenbasierten SQL-Analysen verständlich aufbereiten, visualisieren und einem Fachpublikum präsentieren, um fundierte Geschäftsentscheidungen zu unterstützen.

# Unsere Lernreise - Das Epic im Überblick

Unsere Reise führt uns schrittweise von der greifbaren Logik zur digitalen Anwendung. Jede Etappe baut auf der vorherigen auf und bereitet uns auf die Abschlusspräsentation vor.  
<br/>Phase 1: Das Fundament legen (analog)  
<br/>M2.1.1 & M2.1.2: Wir entdecken die Grundbegriffe und Operationen der Mengenlehre mit LEGO-Steinen. Wir bauen, sortieren und kombinieren, um ein intuitives Gefühl für die Logik zu bekommen, ganz ohne Code.  
<br/>Phase 2: Die Brücke zur IT bauen (digital)  
<br/>M2.1.3: Der entscheidende Schritt! Wir öffnen die Datenbank und übersetzen unsere LEGO-Operationen direkt in die SQL-Befehle UNION, INTERSECT und EXCEPT.  
<br/>M2.1.4: Wir analysieren die Beziehungen zwischen den Datentabellen und lernen mit JOINs das mächtigste Werkzeug für relationale Datenbanken kennen.  
<br/>Phase 3: Die Expertise vertiefen (Analyse)  
<br/>M2.1.5 & M2.1.6: Wir nutzen fortgeschrittene Konzepte, um gezielt fehlende Daten aufzuspüren (Komplement) und komplexe Unterschiede zwischen Datensätzen zu analysieren (Symmetrische Differenz).  
<br/>Abschluss: Die Meisterprüfung  
<br/>Gesamtaufgabe: Wir wenden alle erlernten Fähigkeiten an, um eine strategische Analyse für die Stadtbibliothek Braunschweig durchzuführen und unsere Ergebnisse professionell zu präsentieren.

```
\begin{tikzpicture}[scale=0.7, every node/.style={scale=0.8}]
    % Draw circles
    \draw (-1.2,0) circle (1.5cm) node[xshift=-2.2cm] {$A$};
    \draw (1.2,0) circle (1.5cm) node[xshift=2.2cm] {$B$};
    % Fill the union
    \begin{scope}
        \fill[gray, opacity=0.3] (-1.2,0) circle (1.5cm);
        \fill[gray, opacity=0.3] (1.2,0) circle (1.5cm);
    \end{scope}
\end{tikzpicture}
```