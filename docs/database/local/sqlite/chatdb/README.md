# ChatDB

## Zweck
Die ChatDB speichert sämtliche Chats lokal.

## Verantwortlichkeiten
- Speicherung aller Chatverläufe
- Zeitstempel und Metadaten
- Referenz zur ProjectDB
- Grundlage für Deep Search

Die ChatDB wird nicht direkt durchsucht, solange ein Treffer über die IndexDB gefunden werden kann.