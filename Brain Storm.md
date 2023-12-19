## Vorwort
[Vorwort](Vorwort.md)  
Studiengang  
Daten des Praktikums  
Dauer
## BMW
### Kurzvorstellung BMW
[Kurzvorstellung BMW](Kurzvorstellung%20BMW.md)  
Gründung  
Werke, Länder  
Mitarbeiter  
Produzierte Autos
### Werk Regensburg
[Werk Regensburg](Werk%20Regensburg.md)  
Bau  
Art des Werks  
Mitarbeiter  
Produktionsmenge und Typen  
Fläche  
Luftbild
### Gruppe FG-750
[Gruppe FG-750](Gruppe%20FG-750.md)  
Position im Unternehmen  
Zuständigkeitsbereiche  
Mitarbeiter  
Subprodukte
## Hauptteil/Tätigkeitsbeschreibung
### Regeltermine
[Regeltermine](Regeltermine.md)  
Q-Next Daily & Sprintwechseln  
Zweiwöchentliches Gruppen Meeting  
Zweiwöchentliches IT-Regensburg Meeting  
Wöchentliches TU-1 Werksinfo Meeting  
Wöchentliches Domänen-/Abteilungs-Meeting  
Monatlicher Arbeitstermin, in dem neue Technologien/Pläne/etc vorgestellt werden
### Problem Beschreibung
#### Erklärung was Pampas ist
#### Probleme von Pampas
End of Life  
Schlecht zu erweitern  
Outdated UI
### Anforderungen
Funktionale & Nichtfunktionale Anforderungen an das komplette System
### Implementierung
#### (Exporter)
Liefern Metrik auf verschiedene Weisen
#### Prometheus
Verarbeitet Metriken weiter zu Regeln  
Sendet bei Schwellwertüberschreitung Alarm an Alertmanager
#### Loki
Log Files empfangen  
Metriken aus Log Files generieren  
Alerts auf diese Metriken schreiben
#### Alertmanager
Sammelt Alerts und leitet nach Config weiter  
Zeigt feuernde Alerts an
#### Ansible
Genutzt zur Automatisierung verschiedener Tasks  
Fehlerbehebung  
Installation/Setup Prozesse
#### Rundeck
Wird durch Alertmanager aufgerufen  
Jobs werden aufgerufen -> Automatisierung
### Test & Abnahme?
Prometheus Unit Tests für Prometheus Regeln  
Curl für Alertmanager
## Reflexion
### Was habe ich fachlich dazugelernt
Arbeiten im Low-/No-Code Bereich  
Arbeiten in einem agilen Team  
Fähigkeiten auf der Kommandozeile verbessert  
SQL gefestigt  
Arbeit zu präsentieren und für Personen, die weniger tief im Thema drin sind, verständlich   auszudrücken und sie abzuholen
### Was konnte ich aus dem Studium anwenden
Prozesse des Software Engineering aus SE  
Arbeiten auf der Kommandozeile aus OS  
SQL und Wissen über Datenbanken aus DB  
Auch nicht direkt angewandtes Wissen aus dem Studium als Grundlage, um Zusammenhänge zu verstehen  
Die Fähigkeit mir neues Wissen anzueignen
### Was bringt mir das persönlich (Studium/Beruf)