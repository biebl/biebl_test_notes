# IoT-Stack für Industrieumgebungen (Kubernetes)

Dieses Projekt stellt einen vollständigen IoT-Stack für den Einsatz bei Industriekunden bereit. Ziel ist die Erfassung, Speicherung, Analyse und Visualisierung von Sensordaten in einer industriellen Umgebung.

## Komponenten (Kubernetes)
- **Mosquitto** (MQTT-Broker): Vermittelt Sensordaten zwischen Geräten und Backend.
- **Telegraf** (Datenkollektor): Liest MQTT-Daten und schreibt sie in InfluxDB.
- **InfluxDB** (Zeitreihendatenbank): Speichert Sensordaten effizient.
- **Grafana** (Visualisierung): Stellt Dashboards für die Analyse und Überwachung bereit.

## Einsatzzweck
- Zentrale Erfassung und Überwachung von Maschinendaten
- Visualisierung von Produktions- und Umweltdaten
- Grundlage für Predictive Maintenance und Prozessoptimierung

## Installation (Kubernetes)
1. Kubernetes-Cluster bereitstellen (z.B. Minikube, k3s, AKS, EKS, GKE)
2. Repository klonen:
   ```powershell
   git clone https://github.com/biebl/biebl_test_notes.git
   cd biebl_test_notes\k8s
   ```
3. Deployments anwenden:
   ```powershell
   kubectl apply -f .
   ```
4. Zugriff:
   - Mosquitto: NodePort 31883 (MQTT), 39001 (WebSocket)
   - InfluxDB: NodePort 32086 (Benutzer: admin, Passwort: admin1234)
   - Grafana: NodePort 33000 (Benutzer: admin, Passwort: admin1234)

Weitere Konfigurationen können in den jeweiligen YAML-Dateien vorgenommen werden.
