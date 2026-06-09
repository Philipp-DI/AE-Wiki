# Olena

Als Junior Network Security Engineer

möchte ich die Prinzipien von Zero Trust verstehen,

damit ich moderne Sicherheitsarchitekturen entwerfen kann, die nicht mehr auf veralteten Perimetermodellen basieren.

# Celebration Criteria

- Wir können das traditionelle "Castle-and-Moat"-Sicherheitsmodell dem Zero-Trust-Ansatz gegenüberstellen.
- Wir können die drei Kernprinzipien von Zero Trust ("Verify explicitly", "Use least privilege access", "Assume breach") erklären.
- Wir können die zentrale Rolle von Identität und Multi-Faktor-Authentifizierung (MFA) in einer Zero-Trust-Architektur begründen.

# Wissens-Briefing

Das traditionelle Sicherheitsmodell **("Castle-and-Moat" / Burg und Graben)** geht davon aus, dass alles innerhalb des Unternehmensnetzwerks vertrauenswürdig ("innen") und alles außerhalb bösartig ("außen") ist. Eine starke Firewall schützt die Grenze. Dieses Modell versagt, sobald ein Angreifer einmal "drin" ist (z.B. durch eine Phishing-Mail) oder wenn es keine klare Grenze mehr gibt (Remote-Arbeit, Cloud-Dienste).

**Zero Trust** ist eine moderne Sicherheitsstrategie, die auf dem Grundsatz **"Never trust, always verify" (Vertraue niemals, überprüfe immer)** basiert. Es gibt kein "innen" oder "außen" mehr. Jeder Zugriff, egal von wo, wird als potenziell feindlich betrachtet und muss authentifiziert und autorisiert werden.

**Kernprinzipien:**

1. **Verify explicitly (Explizit überprüfen):** Jeder Zugriffsversuch wird basierend auf allen verfügbaren Datenpunkten (Identität, Standort, Geräte-Sicherheit, Dienst) authentifiziert und autorisiert.
2. **Use least privilege access (Zugriff mit geringsten Rechten):** Benutzer erhalten nur die minimalen Berechtigungen, die sie für ihre Arbeit benötigen (Just-in-Time und Just-Enough-Access).
3. **Assume breach (Von einer Kompromittierung ausgehen):** Man geht davon aus, dass der Angreifer bereits im Netzwerk ist. Daher wird der Netzwerkverkehr segmentiert, um die Ausbreitung zu minimieren, und alles wird protokolliert und analysiert.

# Aufgaben

1. **Modelle vergleichen:** Zeichnet ein einfaches Diagramm, das den "Castle-and-Moat"-Ansatz darstellt, und ein weiteres, das die Zero-Trust-Prinzipien visualisiert. Stellt sie gegenüber.  
  <br/>**Vergleich: Castle-and-Moat vs. Zero Trust**  
  **Castle-and-Moat (Burg-und-Graben-Prinzip)**  
  Fokus: Der äußere Perimeter (Firewalls, VPN-Gateways). Die gesamte Verteidigung konzentriert sich auf die Grenze zwischen dem Internet und dem internen Netzwerk.  
  Vertrauen: Das Prinzip lautet: „Vertraue allem im Inneren, misstraue allem von außen.“ Sobald ein Nutzer im Netzwerk ist, gilt er als sicher.  
  Risiko: Wenn ein Angreifer den Perimeter durchbricht, hat er freien Zugriff auf fast alle Ressourcen im Inneren. Es ist ein „Alles-oder-nichts-Modell“.  
  Einfachheit: Dieses Modell ist relativ einfach umzusetzen, besonders für kleinere Netzwerke mit zentraler Infrastruktur.  
  **Zero Trust (Null Vertrauen)**  
  Fokus: Jede einzelne Transaktion und jeder Zugriff auf eine Ressource. Sicherheit findet direkt am Datenpunkt oder der Anwendung statt.  
  Vertrauen: Das Motto lautet: „Niemals vertrauen, immer überprüfen“ (Never Trust, Always Verify). Es gibt keinen Unterschied zwischen „intern“ und „extern“.  
  Risiko: Selbst wenn ein Angreifer Zugriff auf einen Teil des Netzwerks erhält, bleibt sein Spielraum stark begrenzt. Die sogenannte laterale Bewegung (das Umherwandern im Netzwerk) wird durch Mikro-Segmentierung extrem erschwert.  
  Komplexität: Die Implementierung ist deutlich komplexer. Sie erfordert eine moderne Identitätsverwaltung (IAM), strikte Zugriffskontrollen und eine feingliedrige Aufteilung des Netzwerks.
  
  |     |     |     |
  | --- | --- | --- |
  | **Merkmal** | **Castle-and-Moat** | **Zero Trust** |
  | **Sicherheitsfokus** | Netzwerk-Perimeter | Identität und Daten |
  | **Vertrauensbasis** | Standortabhängig (intern/extern) | Standortunabhängig (immer Null) |
  | **Hauptgefahr** | Lateral Movement (nach Einbruch) | Hoher Administrationsaufwand |
  | **Philosophie** | Vertrauen nach dem Login | Verifizierung bei jedem Schritt |
  
    
  **Castle-and-Moat**  
  Alles Innerrhalb des Netzwerks → vertrauenwürdig  
  Alles außerhalb des Netzwerks → bösartig → Firewall (müssen authentifiziert und autorisiert werden).
  
  ```mermaid
  graph TD
      subgraph Internet ["Internet (Gefahrenzone)"]
          I[Unbekannter Traffic]
      end
  
      subgraph Perimeterschutz ["Burggraben (Schutzwall)"]
          FW[Firewall]
          VPN[VPN-Gateway]
      end
  
      subgraph Internes_Netz ["Burg (Vertrauenszone)"]
          APP1[Anwendung A]
          DB1[(Datenbank A)]
          APP2[Anwendung B]
          SRV1[Server]
      end
  
      I --> FW
      FW --> VPN
      VPN --> APP1
      APP1 --- DB1
      APP1 --- APP2
      APP2 --- SRV1
  
      style Perimeterschutz fill:#f9f,stroke:#333
      style Internes_Netz fill:#fff9c4,stroke:#fbc02d
  ```
  
  ![](files/019cee46-bb56-772b-a840-a052711288f9/image.png)
2. **Szenario anwenden:** Wie würde sich der Zugriff eines Designers der "KreativKopf GmbH" aus dem Homeoffice auf den Cloud-Speicher in einem Zero-Trust-Modell vom traditionellen VPN-Zugriff unterscheiden? Welche Faktoren würden bei der Zugriffsentscheidung geprüft?  
  <br/>**Traditionellen VPN-Zugriff**  
  Anmeldung am VPN  
  Nach erfolgreicher Verbindung gilt der Benutzer als INTERN  
  Zugriff auf den Cloud Speicher erfolgt wie aus dem Firmennetz  
  <br/>\- Vertrauen ensteht einmalig beim VPN-Login  
  \- Netzwerkstandort ist entscheidend  
  <br/>**Zero-Trust-Modell**  
  Im Zero-Trust-Modell wird der Zugriff von zu Hause jedes Mal überprüft. Der Benutzer gilt nicht automatisch als vertrauenswürdig, wie es beim VPN der Fall ist.  
  Beim Anmelden wird sein Benutzerkonto und seine Rolle geprüft und es wird eine Multi-Faktor-Authentifizierung genutzt.  
  Außerdem wird geschaut, von welchem Gerät der Zugriff erfolgt, ob das System aktuell ist und der Schutz aktiviert ist.  
  Auch der Standort, die Uhrzeit und das Verhalten des Benutzers werden berücksichtigt.  
  Der Zugriff wird nur auf die Daten gewährt, die für die Arbeit wirklich nötig sind.  
  
3. **Diskussion:** Warum ist Multi-Faktor-Authentifizierung (MFA) eine absolut unverzichtbare Grundlage für jede Zero-Trust-Strategie?  
  MFA ist in Zero Trust unverzichtbar, weil niemand automatisch vertraut wird. Sie prüft immer, dass sich wirklich der richtige Benutzer anmeldet. Ohne MFA könnten Angreifer mit gestohlenen Passwörtern leicht Zugriff bekommen.

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Zero Trust - Ein Überblick](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/CS/Konzeptstudien/Zero-Trust_Ueberblick.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Microsoft - Was ist Zero Trust?](https://docs.microsoft.com/de-de/security/zero-trust/zero-trust-overview)