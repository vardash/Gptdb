# Core

## Zweck
Der Core verbindet die Module der Anwendung und stellt deren Kommunikation sicher.

## Aufgaben
- BootConfig vom Bootstrapper übernehmen
- Konfigurierte Module laden
- Modul-Lebenszyklus verwalten
- Einheitliche Schnittstellen zwischen Modulen bereitstellen
- Kommunikation zwischen Modulen koordinieren

## Nicht Aufgabe
- Keine Plattformerkennung
- Keine Hardwareerkennung
- Keine Implementierung von Modulen
- Keine Geschäftslogik
- Keine direkte Chat- oder KI-Verarbeitung
- Keine direkte Datenbanksuche

Der Core kennt ausschließlich die konfigurierten Module und deren Schnittstellen. Er kennt keine konkreten Implementierungen.