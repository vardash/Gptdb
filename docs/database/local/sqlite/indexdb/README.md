# IndexDB

## Zweck
Die IndexDB dient als schneller Suchindex über die Inhalte der ChatDB.

## Verantwortlichkeiten
- Schlüsselwörter verwalten
- Verweise auf ChatDB-Einträge speichern
- Suchvorgänge beschleunigen
- Nach Deep Search den Index erweitern

Die IndexDB wird bei jeder Suche zuerst verwendet. Nur wenn kein Treffer gefunden wird, kann eine vollständige Suche über die ChatDB erfolgen.