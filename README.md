# IoT-Stack für Industrieumgebungen

Dieses Projekt stellt einen vollständigen IoT-Stack für den Einsatz bei Industriekunden bereit. Ziel ist die Erfassung, Speicherung, Analyse und Visualisierung von Sensordaten in einer industriellen Umgebung.

## Komponenten (Docker Compose)
- **Mosquitto** (MQTT-Broker): Vermittelt Sensordaten zwischen Geräten und Backend.
- **Telegraf** (Datenkollektor): Liest MQTT-Daten und schreibt sie in InfluxDB.
- **InfluxDB** (Zeitreihendatenbank): Speichert Sensordaten effizient.
- **Grafana** (Visualisierung): Stellt Dashboards für die Analyse und Überwachung bereit.

## Einsatzzweck
- Zentrale Erfassung und Überwachung von Maschinendaten
- Visualisierung von Produktions- und Umweltdaten
- Grundlage für Predictive Maintenance und Prozessoptimierung

## Installation (Docker Compose)
1. Docker und Docker Compose installieren ([Download-Link](https://docs.docker.com/get-docker/))
2. Repository klonen:
   ```powershell
   git clone https://github.com/biebl/biebl_test_notes.git
   cd biebl_test_notes
   ```
3. Stack starten:
   ```powershell
   docker compose up -d
   ```
4. Zugriff:
   - Mosquitto: mqtt://localhost:1883
   - InfluxDB: http://localhost:8086 (Benutzer: admin, Passwort: admin1234)
   - Grafana: http://localhost:3000 (Benutzer: admin, Passwort: admin1234)

Weitere Konfigurationen können in den jeweiligen Service-Dateien vorgenommen werden.
