# GPTDB

Offline-First KI-Wissensmanagement.

## Technologie
- Flutter: Plattformübergreifendes UI
- Dart: Programmlogik und Module
- SQLite: Lokale Standard-Datenbank (Pflichtbestandteil)

## Architektur
- Bootstrapper: Erkennt Plattform, Hardware und Runtime und erstellt die Runtime-Konfiguration.
- Core: Lädt ausschließlich konfigurierte Module und verbindet sie über definierte Schnittstellen.
- SQLite ist immer aktiv (Offline First).
- Optionale Module: Security, Sync, KI-Agent, Provider.

## Grundprinzipien
- Offline First
- Modulare Architektur
- Klare Verantwortlichkeiten
- Konfiguration bestimmt geladene Module
- Der Core kennt nur Schnittstellen, keine Implementierungen.

## Architektur (vereinfacht)
```text
App
 │
 ▼
Bootstrapper
 │
 ├─ OS erkennen
 ├─ Hardware erkennen
 ├─ Runtime-Config
 └─ UI auswählen
      │
      ▼
     Core
      │
 ├─ SQLite (immer)
 ├─ UI
 ├─ Security
 │    ├─ Crypto
 │    └─ Credential Store
 ├─ KI-Agent
 │    ├─ IndexDB
 │    └─ ChatDB
 └─ Sync
      ├─ Dropbox
      ├─ WebDAV
      ├─ PostgreSQL
      └─ weitere Provider
```

Weitere Architekturdetails folgen in den Dokumenten unter /docs.
