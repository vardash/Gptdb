# Agent

## Zweck
Der Agent bildet die intelligente Verarbeitungsschicht der Anwendung.

## Verantwortlichkeiten
- IndexDB durchsuchen
- ChatDB bei Bedarf per Deep Search durchsuchen
- Ergebnisse zusammenführen
- Zusammenfassungen erstellen
- Neue Erkenntnisse in den Index übernehmen

## Arbeitsweise
1. Immer zuerst IndexDB durchsuchen.
2. Wird nichts gefunden, kann eine Deep Search über die ChatDB vorgeschlagen werden.
3. Neue Treffer werden zur Optimierung in den Index übernommen.

## Nicht Aufgabe
- Keine UI
- Keine Datenbankverwaltung
- Keine Synchronisation
- Keine Sicherheitsfunktionen

Der Agent arbeitet ausschließlich über die vom Core bereitgestellten Schnittstellen.