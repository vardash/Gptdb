# Architektur

## Modulare Architektur

### Grundprinzip
Jedes Modul besitzt genau einen Verantwortungsbereich. Module kommunizieren ausschließlich über definierte Schnittstellen und kennen die internen Implementierungen anderer Module nicht.

### Module statt Plugins
Ein Modul kapselt seine komplette Funktionalität. Solange die öffentliche Schnittstelle unverändert bleibt, kann ein Modul unabhängig erweitert, ersetzt oder neu implementiert werden.

### Bedarfsorientiertes Laden
Optionale Module werden nur geladen, wenn sie vom Benutzer aktiviert oder tatsächlich benötigt werden. Standardmäßig arbeitet die Anwendung vollständig lokal (Offline First).

### Datencontainer
Die lokale SQLite-Struktur wird als ein gemeinsamer Datencontainer behandelt. Export und Synchronisation erfolgen immer auf Container-Ebene und niemals auf Ebene einzelner Datenbanken.

Ablauf (optional):
- SQLite-Container erstellen
- Container komprimieren
- Container verschlüsseln
- Nur bei aktiviertem Export oder Sync an das Sync-Modul übergeben
- Über den vom Benutzer gewählten Provider übertragen