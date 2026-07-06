# Sync

## Zweck
Das Sync-Modul synchronisiert verschlüsselte Daten zwischen dem lokalen Gerät und externen Speichern.

## Verantwortlichkeiten
- Synchronisation starten und überwachen
- Konflikte erkennen
- Provider abstrahieren
- Offline-First respektieren

## Geplante Provider
- WebDAV
- Nextcloud
- Dropbox
- OneDrive
- Google Drive
- SFTP
- SMB

## Nicht Aufgabe
- Keine Verschlüsselung (Security)
- Keine Datenbankverwaltung (Database)
- Keine KI-Verarbeitung (Agent)

Die Synchronisation erfolgt ausschließlich über definierte Provider-Schnittstellen.