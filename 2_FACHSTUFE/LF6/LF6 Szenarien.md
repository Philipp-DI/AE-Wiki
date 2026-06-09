# LF6 Szenarien

# 🎭 Lernfeld 6: Die Szenarien

Entscheidet euch im Team für **eines** der folgenden Unternehmen. Eure Wahl bestimmt den Kontext aller praktischen Aufgaben (Epics). Die fachlichen Anforderungen bleiben gleich, aber die _Lösungen_ und _Prioritäten_ unterscheiden sich drastisch.

## 🚀 Szenario A: RapidRoute Logistics GmbH

**"Move fast – we fix it later."**

### 🏢 Das Unternehmen

RapidRoute ist ein Quick-Commerce-Startup, das in deutschen Großstädten Lebensmittel in unter 10 Minuten liefert. Das Hauptquartier platzt aus allen Nähten; ständig werden neue "Hubs" (kleine Lagerhäuser) eröffnet. Die IT-Abteilung besteht aus drei überarbeiteten Admins, die bisher alles auf Zuruf gemacht haben.

### ⚠️ Das Problem (Ausgangslage)

Das Onboarding neuer Mitarbeiter ist pures Chaos. PCs werden "irgendwie" aus dem Keller geholt, Kabel fehlen, Lizenzen sind abgelaufen. Es gibt keine Liste, wer welchen Laptop hat (Asset-Chaos). Die Geschäftsführung fordert: "Wenn ein neuer Hub aufmacht, müssen am Tag 1 alle 5 Arbeitsplätze laufen – vollautomatisch. Wir haben keine Zeit für Bastelstunden."

### 🎯 Euer Auftrag

Baut eine **hochautomatisierte Deployment-Straße**. Sicherheit ist wichtig, aber Geschwindigkeit ist King. Ihr braucht Skripte, die PCs in Minuten statt Stunden aufsetzen. Der Service-Prozess muss schlank und schnell sein ("One-Click-Request").

## 📚 Szenario B: Städtische Bibliothek "BiblioTech"

**"Ordnung, Sicherheit und Nachhaltigkeit."**

### 🏢 Das Unternehmen

Die traditionsreiche städtische Bibliothek wandelt sich zum "Digitalen Lernort". Neben den Verwaltungs-Arbeitsplätzen für Bibliothekare gibt es öffentliche "Kiosk-PCs" für Bürger zur Recherche. Das Budget ist öffentlich und streng limitiert (Steuergelder).

### ⚠️ Das Problem (Ausgangslage)

Der Arbeitsschutz hat die alten Arbeitsplätze bemängelt (schlechte Bildschirme, Kabelsalat = Stolperfallen). Zudem gab es einen Vorfall, bei dem ein Besucher an einem öffentlichen Terminal Systemdaten gelöscht hat. Die Amtsleitung fordert: "Die neuen Arbeitsplätze müssen 100% der **BildscharbV** und den **VDE-Normen** entsprechen. Die öffentlichen PCs müssen 'unkaputtbar' sein und sich jede Nacht selbst zurücksetzen."

### 🎯 Euer Auftrag

Baut eine **robuste, normgerechte Umgebung**. Dokumentation ist alles – jeder PC braucht ein Prüfprotokoll. Ihr setzt auf Linux (Ubuntu) für die öffentlichen Terminals, um Lizenzkosten zu sparen und das System mittels lokaler Rechte (ACLs) extrem stark einzuschränken.

## 🧬 Szenario C: BioSafe Lab Solutions

**"Präzision rettet Leben."**

### 🏢 Das Unternehmen

BioSafe führt medizinische Laboranalysen (Blutbilder, DNA-Sequenzierung) durch. Die IT-Systeme steuern teure Analyse-Roboter. Ein Systemausfall bedeutet, dass Proben verderben könnten. Datenschutz (Patientendaten) hat oberste Priorität.

### ⚠️ Das Problem (Ausgangslage)

Ein Audit steht an. Derzeit weiß niemand genau, welcher Laborant Zugriff auf welche Ergebnis-Ordner hat. Es existieren lokale "Schatten-Accounts" auf den Auswertungs-PCs mit schwachen Passwörtern. Der Laborleiter fordert: "Ich brauche lückenlose Nachvollziehbarkeit. Wer hat wann welchen PC bekommen? Wer darf in den Ordner 'Befunde'? Wir brauchen garantierte Reaktionszeiten (SLAs), wenn ein PC ausfällt."

### 🎯 Euer Auftrag

Baut eine **Hochsicherheits-Umgebung**. Der Fokus liegt auf **Access Management** (lokale Gruppen/Rechte exakt setzen) und **Asset-Tracking**. Eure Service-Verträge (SLAs) müssen extrem strikt sein (z.B. "Ersatzgerät innerhalb von 2 Stunden").

## 🛠️ Entscheidungshilfe

| Kriterium | A: RapidRoute | B: BiblioTech | C: BioSafe |
| --- | --- | --- | --- |
| **Haupttreiber** | Speed & Skalierung | Normen & Budget | Sicherheit & Compliance |
| **Arbeitsweise** | "Agil & Automatisiert" | "Gründlich & Formal" | "Präzise & Dokumentiert" |
| **Tech-Fokus** | Unattended Install | VDE / Kiosk-Mode | ACLs / Asset-Mgmt |
| **Vibe** | Chaos bändigen | Vorschriften einhalten | Risiken minimieren |