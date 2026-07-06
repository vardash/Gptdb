# Architektur

## Modulare Architektur

### Grundprinzip
Jedes Modul besitzt genau einen Verantwortungsbereich. Module kommunizieren ausschließlich über definierte Schnittstellen und kennen die internen Implementierungen anderer Module nicht.

### Module statt Plugins
Ein Modul kapselt seine komplette Funktionalität. Solange die öffentliche Schnittstelle unverändert bleibt, kann ein Modul unabhängig erweitert, ersetzt oder neu implementiert werden.

### Datencontainer
Die lokale SQLite-Struktur wird als ein gemeinsamer Datencontainer behandelt. Export und Synchronisation erfolgen immer auf Container-Ebene und niemals auf Ebene einzelner Datenbanken.

Ablauf:
- SQLite-Container erstellen
- Container komprimieren
- Container verschlüsseln
- An das Sync-Modul übergeben
- Über den gewählten Provider übertragen
