# LF3.3.2- Funktioniert es- Netzwerk-Diagnose mit Bordmitteln

Als **First-Level-Supporter am Helpdesk**

möchte ich die wichtigsten Kommandozeilen-Tools zur Netzwerkdiagnose beherrschen,

damit ich die Konnektivität der Clients bei der "Innovate GmbH" systematisch überprüfen und Fehlerquellen schnell eingrenzen kann.

# Celebration Criteria

- Wir können mit `ping` die Erreichbarkeit eines anderen Geräts im LAN und im Internet testen und die Ausgabe (Antwortzeit, TTL) interpretieren.
- Wir können mit `ipconfig /all` (Windows) und `ip addr` (Ubuntu) die vollständige IP-Konfiguration eines Clients anzeigen und auf Fehler (z.B. fehlendes Gateway) prüfen.
- Wir können mit `tracert` (Windows) bzw. `traceroute` (Linux) den Weg eines Datenpakets durch das Internet verfolgen.
- Wir können mit `nslookup` (Windows) bzw. `dig` (Linux) die Namensauflösung (DNS) überprüfen.

# Wissens-Briefing

- **DNS (Domain Name System):** Ein hierarchisches System, das menschenlesbare Domainnamen (z.B. `www.google.de`) in computerlesbare IP-Adressen (z.B. `142.250.185.3`) übersetzt. Es funktioniert wie ein Telefonbuch für das Internet.
- **Diagnose-Werkzeuge:**
    - `ping`**:** Sendet kleine Testpakete (ICMP Echo Request) an ein Ziel, um dessen Erreichbarkeit und die Antwortzeit zu prüfen. Das grundlegendste Tool zur Konnektivitätsprüfung.
    - `ipconfig` **(Windows) /** `ip addr` **(Linux):** Zeigen die aktuelle IP-Konfiguration der Netzwerkschnittstellen an (IP-Adresse, Subnetzmaske, Gateway etc.). Unerlässlich zur Überprüfung der lokalen Konfiguration.
    - `tracert` **(Windows) /** `traceroute` **(Linux):** Verfolgt die Route eines Datenpakets zum Ziel und listet alle Zwischenstationen (Router-Hops) auf. Hilft bei der Lokalisierung von Verbindungsabbrüchen.
    - `nslookup` **/** `dig`**:** Dienen zur Abfrage von DNS-Servern, um zu überprüfen, ob die Namensauflösung korrekt funktioniert.

# Aufgaben

1.  **Systematische Fehlersuche:** Die Mitarbeiterin meldet "kein Internet". Spielt das Szenario in eurer Gruppe durch. Nutzt die Kommandozeile und geht systematisch vor:
    1.  `ipconfig /all` / `ip addr`: Hat der Client eine gültige IP-Adresse und ein Gateway?
    2.  `ping <gateway-ip>`: Ist der eigene Router erreichbar?
    3.  `ping 8.8.8.8`: Ist ein Server im Internet per IP erreichbar? (Testet die Internetverbindung an sich)
    4.  `ping www.google.de`: Funktioniert die Namensauflösung?
    5.  `nslookup www.google.de`: Welches Ergebnis liefert der DNS-Test? Dokumentiert eure Schritte und die jeweilige Schlussfolgerung in einem Protokoll.
2.  **Analyse:** Führt jeder für sich einen `tracert www.heise.de` (Windows) oder `traceroute www.heise.de` (Linux) aus. Vergleicht die ersten drei Hops in eurer Gruppe. Warum sind diese wahrscheinlich bei allen gleich oder sehr ähnlich? Was repräsentieren sie?
3.  **Peer-Teaching:** Bildet Paare. Einer erklärt dem anderen die Ausgabe von `ping` (was bedeutet "Zeit<1ms", "TTL=58"?). Der andere erklärt die Ausgabe von `ipconfig /all` (was ist der Unterschied zwischen "Physische Adresse" und "IPv4-Adresse"?).

# Quellen & Vertiefung

- **IT-Handbuch**
    - **Kap. 5.8.2 "DNS" (S. 295-298)**
    - **Kap. 12.4.2 "Netzwerkanalyse unter Windows" (S. 1034-1040)**
    - **Kap. 13.5.2 "Netzwerkanalyse unter Linux" (S. 1166-1171).**
- Vertiefung (Wikipedia): [Ping (Datenübertragung)](https://de.wikipedia.org/wiki/Ping_%28Daten%C3%BCbertragung%29)
- Vertiefung (Wikipedia): [Domain Name System (DNS)](https://de.wikipedia.org/wiki/Domain_Name_System)