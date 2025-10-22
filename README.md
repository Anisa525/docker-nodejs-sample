# ToDo-Applikation mit Docker

Diese Anleitung beschreibt Schritt für Schritt, wie du die ToDo-Applikation auf deinem Rechner einrichtest, in Docker ausführst und eine persistente Datenbank konfigurierst.

---

## 1. Fork erstellen
1. Das originale GitHub-Repository öffnen: [docker-nodejs-sample](https://github.com/ICT-BLJ/docker-nodejs-sample)  
2. Oben rechts auf **Fork** klicken.  
3. Optional kannst du den Namen deines Forks anpassen.  
4. Auf **Fork erstellen** klicken, um das Repository in deinem eigenen GitHub-Account zu speichern.  
5. Der Fork ist nun bereit, lokal geklont zu werden.

---

## 2. Repository lokal klonen
1. Stelle sicher, dass Git Bash auf deinem Rechner installiert ist.  
2. Wähle einen Ordner aus, in dem du den Repository-Clone speichern möchtest.  
3. Öffne Git Bash und navigiere in diesen Ordner in welchem du das ganze haben möchtest (bsp.):  
   ```bash
   cd C:\Abschluss_doks

## 3. Dockeer einrichten 
1.	Docker Desktop öffnen
2.	Terminal öffnen und ins Projektverzeichnis wechseln
3.	Docker initialisieren:
-	docker init
4.	Fragen beantworten:
-	Plattform: Node
-	Node-Version: 18.0.0
-	Package-Manager: npm
-	Startkommando: node src/index.js
-	Port: 3000
5.	Container bauen und starten:

        docker compose up --build
   

## 4. Fehlerbehebung
1.	Tritt ein Fehler beim Bauen auf, Dockerfile anpassen:
-  NODE_VERSION=18.0.0
-	FROM node:${NODE_VERSION}-alpine
2.  Ersetzt denn oberen Code durch: 
-  ARG NODE_VERSION=18
-  FROM node:${NODE_VERSION}
-	Änderungen speichern und Container erneut starten:
-	docker compose up --build
-	Browser öffnen: http://localhost:3000
    
## 5. Datenbank einrichten
1.	compose.yaml anpassen (Datenbankservice, Volumes, Secrets)
2.	Neuen Ordner db erstellen
3.	Datei password.txt im Ordner db anlegen
-	Passwort ohne Sonderzeichen eintragen
-	Keine Leerzeilen oder Umbrüche
4.	Alle Änderungen speichern
5.	Container erneut starten:
6.	docker compose up --build
7.	Anwendung testen:
-	ToDo-Einträge hinzufügen
-	Container stoppen: Ctrl + C
-	Container entfernen:
-	docker compose rm
-	Container erneut starten:
-	docker compose up --build
-	Prüfen, ob Daten erhalten bleiben

## 6. Zusammenfassung
-	Fork erstellt und lokal geklont
-	Docker eingerichtet und Container gebaut
-	Fehler im Dockerfile behoben, falls notwendig
-	Datenbank konfiguriert
-	ToDo-Applikation erfolgreich getestet

## Notwndige Pakete 
- Doker Desktop 
