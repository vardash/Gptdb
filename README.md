# GPTDB

Offline-First KI-Wissensmanagement.

## Technologie
- Flutter: Plattformübergreifendes UI
- Dart: Programmlogik und Module
- SQLite: Lokale Standard-Datenhaltung auf allen Plattformen.

## SQLite-Struktur
SQLite ist der lokale Standard und wird immer geladen.

Enthaltene Datenbanken/Konfigurationsbereiche:
- BootConfig (Runtime-/OS-Konfiguration des Bootstrappers)
- UserConfig (Benutzereinstellungen)
- SyncConfig (gewählter Provider und Synchronisationsoptionen, keine Zugangsdaten)
- ChatDB (alle Chats)
- IndexDB (Suchindex)
- ProjectDB (Projekt- und Referenzzuordnung)

## Architektur
- Bootstrapper erkennt Betriebssystem, Hardware und APIs.
- Bootstrapper erzeugt die BootConfig.
- Core lädt ausschließlich konfigurierte Module.
- SQLite ist Pflichtbestandteil (Offline First).
- Optionale Module: Security, Sync, KI-Agent und Provider.
- Der Core kennt nur Schnittstellen, keine Implementierungen.

## Grundprinzipien
- Offline First
- Modulare Architektur
- Klare Verantwortlichkeiten
- Konfiguration bestimmt geladene Module
- BootConfig und UserConfig sind strikt getrennt.

## Architektur (vereinfacht)
```text
App
 │
 ▼
Bootstrapper
 │
 ├─ OS
 ├─ Hardware
 ├─ APIs
 └─ BootConfig
      │
      ▼
     Core
      │
 ├─ SQLite
 │   ├─ BootConfig
 │   ├─ UserConfig
 │   ├─ SyncConfig
 │   ├─ ChatDB
 │   ├─ IndexDB
 │   └─ ProjectDB
 ├─ UI
 ├─ Security
 ├─ KI-Agent
 └─ Sync Provider
```

Weitere Architekturdetails folgen unter /docs.