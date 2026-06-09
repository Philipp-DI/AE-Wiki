# LF3.3.1- Der Client geht online - IP-Konfiguration

Als **IT-Servicetechniker im Field Service**

möchte ich die IP-Konfiguration eines Clients sowohl statisch als auch dynamisch per DHCP unter Windows und Linux durchführen können,

damit ich die Arbeitsplätze der "Innovate GmbH" korrekt in das geplante Adressschema einbinden kann.

# Celebration Criteria

- Wir können unter Windows 11 die Netzwerkeinstellungen finden und eine statische IPv4-Adresse, Subnetzmaske, Gateway und DNS-Server eintragen.
- Wir können unter Ubuntu Linux (grafisch und per Kommandozeile) eine statische IP-Konfiguration vornehmen.
- Wir können den Unterschied und die Vor- und Nachteile von statischer und dynamischer Adressvergabe (DHCP) erklären.
- Wir können überprüfen, ob ein Client seine IP-Konfiguration erfolgreich per DHCP bezogen hat.

# Wissens-Briefing

## Statische IP-Konfiguration

Die IP-Adresse, Subnetzmaske, Gateway und DNS-Server werden manuell und fest am Gerät eingetragen.

- **Vorteil:** Das Gerät ist immer unter derselben Adresse erreichbar.
- **Nachteil:** Hoher Verwaltungsaufwand, fehleranfällig (Gefahr von doppelter Adressvergabe).
- **Anwendung:** Für Server, Drucker, Router und andere zentrale Netzwerkkomponenten.

## Dynamische IP-Konfiguration (DHCP)

- **DHCP** (Dynamic **Host Configuration Protocol):** Ein Netzwerkdienst, der automatisch IP-Adressen und weitere Konfigurationsparameter (Subnetzmaske, Gateway, DNS-Server) an Clients in einem Netzwerk vergibt.
- **Funktionsweise (DORA-Prozess):**
    1.  **Discover:** Der Client sucht im Netz nach einem DHCP-Server.
    2.  **Offer:** Ein oder mehrere DHCP-Server bieten dem Client eine IP-Adresse an.
    3.  **Request:** Der Client fordert eine der angebotenen Adressen an.
    4.  **Acknowledge:** Der Server bestätigt die Vergabe der Adresse für eine bestimmte Zeit ("Lease Time").
- **Vorteil:** Geringer Verwaltungsaufwand, vermeidet Adresskonflikte, ideal für Clients (PCs, Laptops, Smartphones).

# Aufgaben

1.  **Praktische Übung (Paararbeit, Remote-fähig via VMs):** Arbeitet zu zweit. Einer konfiguriert seinen Windows-Client, der andere seinen Ubuntu-Client.
    - **Teil A (Statisch):** Weist euren Clients manuell eine IP-Adresse aus dem Netz `192.168.50.0/24` zu (z.B. `.10` und `.11`), Subnetzmaske `255.255.255.0`, Gateway `192.168.50.1`, DNS `8.8.8.8`. Dokumentiert die Schritte mit Screenshots.
    - **Teil B (Dynamisch):** Stellt die Konfiguration wieder auf "Automatisch (DHCP)" um. Überprüft mit `ipconfig /all` bzw. `ip addr`, welche Adresse ihr nun erhalten habt.
2.  **Diskussion (Szenario-Bezug):** Entscheidet in der Gruppe, welche Geräte im Netzwerk der "Innovate GmbH" eine statische IP-Adresse bekommen sollten und welche per DHCP konfiguriert werden können. Begründet eure Entscheidung.
3.  **Konzeptaufgabe:** Entwerft einen kleinen IP-Adressplan für die "Innovate GmbH". Legt fest, welcher Bereich für DHCP (`.100` bis `.150`), welcher für statische Clients (`.10` bis `.20`) und welcher für Netzwerkgeräte (`.1` für den Router, `.2` für den Switch) reserviert ist.

# Quellen & Vertiefung

- **IT-Handbuch**
    - **Kap. 5.8.1 "DHCP" (S. 293-294)**
    - **Kap.12.4.1 "Windows-Netzwerkkonfiguration" (S. 1032-1033)**
    - **Kap. 13.5.1 "Linux-Netzwerkkonfiguration" (S. 1162-1166).**
- Vertiefung (Wikipedia): [Dynamic Host Configuration Protocol (DHCP)](https://de.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)