# LF6.2- Automatisierung, Softwareverteilung und Identitätsmanagement

**Fokus:** Effiziente Bereitstellung von Systemen, Software-Lebenszyklus und Zugriffskontrolle

## 👥 Epic User Story

> _Als IT-Service-Team_  
> _möchten wir Betriebssysteme und Software automatisiert bereitstellen, Aktualisierungen systematisch einspielen und Identitäten sowohl lokal als auch für Cloud-Dienste verwalten,_  
> _damit Arbeitsplätze schnell, sicher und wartungsarm einsatzbereit sind._

## 🎯 Celebration Criteria (Kernkompetenzen)

- Wir können ein automatisiertes Deployment für Linux-Systeme planen und eine Strategie für die Wartung (Updates) entwerfen. (K5)
- Wir bewerten verschiedene Software-Rollout-Szenarien (z. B. Staged Rollout) im Hinblick auf Stabilität und Nutzerakzeptanz. (K6)
- Wir implementieren Zugriffsberechtigungen unter Berücksichtigung von lokalen Diensten (LDAP) und Cloud-Anforderungen (SaaS). (K5)
- Wir vergleichen klassische Verzeichnisdienste (AD) mit modernen Identitätslösungen (Entra ID) hinsichtlich ihrer Anforderungen und Einsatzgebiete. (K4)

## 🧩 Ganzheitliche Aufgabe (Transfer)

**Schätzung:** 8 SP

**Titel:** "Der automatisierte Software-Lebenszyklus" **Szenario:** Wählt euer Szenario (RapidRoute, BiblioTech oder BioSafe).

**Die Mission:** Euer Unternehmen wächst, und die manuelle Installation von Software und Updates ist nicht mehr tragbar. Ihr sollt ein Konzept für eine automatisierte Arbeitsumgebung erstellen, die sowohl das Betriebssystem als auch die fachspezifische Software umfasst. Dabei müsst ihr sicherstellen, dass Updates die Arbeit nicht unterbrechen (Staged Rollout) und Zugriffsrechte für SaaS-Anwendungen zentral gesteuert werden.

**Die 5 Puzzleteile (Rollen):**

1. **Der Deployment-Ingenieur:** Konfiguriert die automatisierte Linux-Installation und definiert die Update-Strategie (Wartungsfenster).
2. **Der Software-Paketierer:** Erstellt den Plan für die Softwareverteilung in Abhängigkeit von Benutzergruppen (Staged Rollout).
3. **Der Identitäts-Manager:** Setzt die lokale Benutzerverwaltung um und bereitet die Anbindung an OpenLDAP vor.
4. **Der Cloud-Architekt:** Entwirft die Zugriffsberechtigungen für die genutzten SaaS-Lösungen und erstellt den theoretischen Ausblick für M365/Entra ID.
5. **Der Revisions-Prüfer:** Testet die Berechtigungen, prüft die Lizenz-Compliance und validiert den Update-Status der Systeme.

**Abschlusskriterien:** Ein funktionierendes Installations-Medium für Linux, ein dokumentierter Rollout-Plan für Software-Updates und eine Berechtigungsmatrix, die lokale Konten und SaaS-Zugänge abdeckt.