# LF4.3.2- Zero Trust- Vertraue niemandem

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
2. **Szenario anwenden:** Wie würde sich der Zugriff eines Designers der "KreativKopf GmbH" aus dem Homeoffice auf den Cloud-Speicher in einem Zero-Trust-Modell vom traditionellen VPN-Zugriff unterscheiden? Welche Faktoren würden bei der Zugriffsentscheidung geprüft?
3. **Diskussion:** Warum ist Multi-Faktor-Authentifizierung (MFA) eine absolut unverzichtbare Grundlage für jede Zero-Trust-Strategie?

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Zero Trust - Ein Überblick](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/CS/Konzeptstudien/Zero-Trust_Ueberblick.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Microsoft - Was ist Zero Trust?](https://docs.microsoft.com/de-de/security/zero-trust/zero-trust-overview)