# Beispielhefte

## Lastenheft

### 1\. Projektübersicht

**Projektname:** WIMS - Web-Based Inventory Management System

**Kunde:** Socksnation AG (Einzelhandelsunternehmen mit Online-Shop)

**Vorhaben:** Optimierung der Lagerverwaltung, Echtzeit‑Tracking, und Automatisierung von Bestellprozessen.

### 2\. Projektziele

| Ziele | Messkriterien |
| --- | --- |
| Reduzierung manueller Fehler | mind. 20% weniger fehlerhafte Bestellungen |
| Schnellere Lagerprozesse | ca. 40% schneller Durchlaufzeit |
| Kosteneinsparung | mind. 10% reduzierte Lagerkosten pro Jahr |

### 3\. Funktionsanforderungen

| Funktion | Beschreibung | Akzeptanzkriterien |
| --- | --- | --- |
| Echtzeit-Lagerbestand | Anzeige aktueller Bestände in Echtzeit | ~99 % Genauigkeit |
| Bestellautomatisierung | Automatisches Nachbestellen bei Schwellenwerten | Keine manuellen Eingriffe bei Schwellenwerten nötig |
| Benutzer‑ und Rollenmanagement | Admin, Lagerist, Manager | Rollenbasierte Zugriffskontrolle |
| Mobile App | Android & iOS | Synchronisation mit Web‑Interface |

### 4\. Nicht-Funktionsanforderungen

| Aspekt | Anforderung | Akzeptanzkriterien |
| --- | --- | --- |
| Leistung | schnelle Response-Time | i.d.R. alle Anfragen in <3s bearbeitet |
| Sicherheit | konform mit DSGVO | Keine Datenverluste, Verschlüsselung |
| Skalierbarkeit | aktuell ca. 10000 User \| ca. 1 Mio. Artikel | keine Downtimes unter 70% Last |

### 5\. Sonstige Rahmenbedingungen

- **Budget:** 200.000 €, inkl. Linzenzen und Support
- **Zeitplan:** 12 Monate, evtl. Meilensteine

## Pflichtenheft

### 1\. Datenzuweisung / Modell

| Art | Attribute | Typ |
| --- | --- | --- |
| Artikel | SKU, Name, Beschreibung, Preis, Bestand | String, Number |
| Bestellung | ID, Artikel-ID, Menge | Integer |
| User | ID, E-Mail | Integer, String |

_Für weitere Details fehlt mir an dieser Stelle das passende (technische) Know-How._