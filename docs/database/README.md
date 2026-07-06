# Database

## Zweck
Das Database-Modul verwaltet die gesamte lokale Datenhaltung der Anwendung.

## Grundprinzip
- Offline First
- SQLite ist die lokale Standarddatenbank und wird immer verwendet.

## Verantwortlichkeiten
- BootConfig
- UserConfig
- SyncConfig
- ChatDB
- IndexDB
- ProjectDB
- Datenbank-Migrationen
- Integritätsprüfung (Versionen und Hashwerte)

## Nicht Aufgabe
- Keine KI-Verarbeitung
- Keine Benutzeroberfläche
- Keine Synchronisation mit Cloud-Diensten (erfolgt über das Sync-Modul)
- Keine Verschlüsselungslogik (erfolgt über das Security-Modul)

Dieses Modul bildet die Grundlage für alle weiteren Module der Anwendung.