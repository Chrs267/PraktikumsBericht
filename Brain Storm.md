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
[Pampas](Pampas.md)
Aktuelles Monitoring
Glassfisch 4 Server
Nagios uralt mit modifikationen
	Bietet manche vordefinierte Checks
	Bietet custom checks über DBs
Daten kommen aus Datenbanken und direkt vom Linux Packet über einen technischen User
#### Probleme von Pampas
End of Life  
	Outdated UI
Schlecht zu erweitern  
	Komplette Überarbeitung der alten Versionen und selbst angepassten Bausteine nötig
	GlassFish4 auf Payara umziehen
	Automatisierung über Rundeck nicht möglich
	Ansible nicht zum automatischen einrichten möglich
		Große Vorteile: Wiederverwendbar, Reproduzierbar, Einheitlich
  Z. T. manuelle Aufgaben vor der Produktion nötig
	  Uhrzeit, menschlicher Fehler
Unsicher ob ITSM-Next angebunden werden kann

Reihenfolge: EoL -> Prometheus -> Ansible Automatisierung -> Rundeck als GUI -> Rundeck um alles mögliche zu automatisieren
### Anforderungen
Funktionale & Nichtfunktionale Anforderungen an das komplette System

Beschreibung des zu überwachenden Systems
Über 50 Schnittstellen, z. T. veraltete Technologien
Legacy Software
Monitoring speziell für das zentrale Qualitätssystem, welches aus Legacy Software mit z. T. veralteten Technologien besteht
### Implementierung

Abriss des Systems
Exporter werden auf Linux Server installiert und Sammeln Daten
Zentrales Prometheus scraped diese Daten ab
Loki erhält über Promtail Daten von Prometheus
Grafana erhält Daten von Loki und Prometheus
Loki und Prometheus schicken, im Fall eines Alarms, Daten an Alertmanager
Alertmanager Schickt Daten per Webhook an Teams, Rundeck, ITSM etc
Rundeck Jobs führen Skripte oder Ansible Playbooks aus
#### (Exporter)
Liefern Metrik auf verschiedene Weisen

Blocking Session
Session Utilization
#### Prometheus
Verarbeitet Metriken weiter zu Regeln  
Sendet bei Schwellwertüberschreitung Alarm an Alertmanager

Regeln angepasst (Ober und Untergrenze)
Regeln für oben erwähnte Metriken ergänzt
Blocking Session Regel Bild einfügen

#### Loki
Log Files empfangen  
Metriken aus Log Files generieren  
Alerts auf diese Metriken schreiben
#### Alertmanager
Sammelt Alerts und leitet nach Config weiter  (Aufgrund von Labels)
Zeigt feuernde Alerts an
#### Ansible
Genutzt zur Automatisierung verschiedener Tasks  
Fehlerbehebung  
Installation/Setup Prozesse
Selbst an Beispielen aus dem Unternehmen gelernt
#### Rundeck
Wird durch Alertmanager aufgerufen  
Jobs werden aufgerufen -> Automatisierung
#### Confluence, Jira, Git
Zur Koordination
Zur Source Control
Wissensmanagement (Dokumentieren)
### Test & Abnahme?
Prometheus Unit Tests für Prometheus Regeln  
Curl für Alertmanager
Workshop Vorstellungen
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