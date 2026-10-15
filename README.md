> [!CAUTION]
> Disclaimer: This repository was created using AI.

# Recursive DNS

```text
Projektname: Recursive DNS
Repository:  recursive-dns
CLI-Befehl:  rdns
Kurzform:    RDNS
```

## Ziel

DNS-Auflösung lokal auf dem Gerät durchführen.

Kein Google DNS.
Kein Cloudflare DNS.
Kein ISP DNS.
Kein externer rekursiver DNS-Resolver.

Das Gerät wird selbst zum rekursiven DNS-Resolver.

## Architektur

Heute:

```text
Anwendung
    ↓
Gerät
    ↓
Externer Rekursiver Resolver
    ↓
Root
    ↓
TLD
    ↓
Authoritative DNS Server
```

RDNS:

```text
Anwendung
    ↓
iOS DNS Cache
    ↓
RDNS
    ↓
Root
    ↓
TLD
    ↓
Authoritative DNS Server
```

## VPN-Kompatibilität

VPN-Funktionalität bleibt unverändert.

```text
Anwendung
    ↓
VPN & Geräteverwaltung
    ↓
iOS DNS Cache
    ↓
RDNS
    ↓
VPN
    ↓
Root
    ↓
TLD
    ↓
Authoritative DNS Server
```

RDNS verarbeitet ausschließlich DNS-Anfragen.

Sämtlicher sonstiger Netzwerkverkehr wird unverändert durch vorhandene VPN-Lösungen verarbeitet.

DNS-Auflösung darf nicht über ein VPN-Profil umgesetzt werden.

## Eigenschaften

- Lokale rekursive DNS-Auflösung
- Nutzung des vorhandenen iOS DNS-Caches
- Keine externe Resolver-Abhängigkeit
- VPN-kompatibel
- Open Source
- Minimaler Ressourcenverbrauch
- Keine Telemetrie
- Keine Konten
- Keine Cloud-Dienste
- Keine Werbung

## Endzustand

Jede DNS-Anfrage wird lokal aufgelöst.

Kein externer rekursiver DNS-Resolver wird benötigt.

DNS-Auflösung funktioniert mit oder ohne VPN.

Das Gerät selbst übernimmt die vollständige rekursive DNS-Auflösung.
