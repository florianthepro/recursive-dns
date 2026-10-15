# AGENTS.md

- Alles Verbindliche steht in `README.md`.
- `README.md` und `AGENTS.md` nicht ändern.
- Architektur, Zielbild und Grundprinzipien aus `README.md` einhalten.
- Das Gerät muss selbst die rekursive DNS-Auflösung durchführen.
- Es darf keine Abhängigkeit von externen rekursiven DNS-Resolvern entstehen.
- Vorhandene VPN-Lösungen müssen uneingeschränkt weiter funktionieren.
- DNS-Auflösung darf keinen VPN-Slot belegen.
- DNS-Verarbeitung darf nicht über ein VPN-Profil umgesetzt werden.
- Ausschließlich DNS-Verkehr behandeln.
- Nicht-DNS-Verkehr niemals verändern, umleiten oder verarbeiten.
- Vorhandene iOS-DNS-Caches nutzen.

## Minimalprinzip

- Die Anwendung soll ausschließlich die in `README.md` beschriebene Aufgabe erfüllen.
- Jede Funktion muss indirekt oder direkt zur rekursiven DNS-Auflösung beitragen.
- Funktionen ohne direkten Bezug zur DNS-Auflösung dürfen nicht implementiert werden.
- Die einfachste Lösung ist zu bevorzugen, sofern sie das Zielbild vollständig erfüllt.
- Vorhandene Betriebssystemfunktionen sind zu nutzen statt diese nachzubauen.
- Bestehende iOS-Funktionen sind zu integrieren statt durch eigene Implementierungen zu ersetzen.

## Nicht implementieren

- VPN
- Ad-Blocking
- Tracking-Schutz
- Firewall-Funktionen
- Traffic-Analyse
- Paketmitschnitt
- Netzwerk-Monitoring
- Benutzerkonten
- Cloud-Dienste
- Synchronisation
- Telemetrie
- Analytics
- Werbung
- Abonnements
- Bezahlfunktionen
- Social-Funktionen
- Diagnoseportale
- Web-Dashboards
- Eigene Caching-Systeme ohne technische Notwendigkeit

## Ziel

Die Anwendung soll möglichst klein, einfach und ressourcenschonend bleiben.

Sie soll genau eine Aufgabe erfüllen:

DNS-Anfragen lokal rekursiv auflösen.
