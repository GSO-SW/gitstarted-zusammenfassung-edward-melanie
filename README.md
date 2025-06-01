# Git Anleitung – Komplett

## Zu Git

Ein Versionskontrollsystem (VCS) wie Git hilft dir, Änderungen an Dateien und Projekten zu speichern und nachzuvollziehen.  
Git erlaubt schnelles Arbeiten mit verschiedenen Entwicklungszweigen (Branches) und deren Zusammenführung (Merging).

---

## Allgemeine Begriffe

### Repository  
Ein Speicherort für den Quellcode und die gesamte Historie. Kann lokal (auf deinem Rechner) oder remote (auf einem Server) sein.

### Lokal vs. Remote  
- **Lokal:** Auf deinem eigenen Computer, mit vollständiger Historie.  
- **Remote:** Auf einem Server, damit mehrere Leute zusammenarbeiten können.

### Branch  
Ein Zweig, auf dem du unabhängig vom Hauptzweig arbeiten kannst. Nützlich für neue Features oder Experimente.

### Working Directory  
Der aktuelle Zustand deiner Dateien auf deinem Rechner.

### Staging Area  
Zwischenspeicher, in den du Dateien legst, bevor du sie in einem Commit speicherst.

### Commit  
Ein gespeicherter Moment in der Historie mit einer Nachricht, was geändert wurde.

### Historie  
Die komplette Aufzeichnung aller Änderungen an Dateien und Branches.

---

## Git einrichten

### Git installieren  
Lade Git von [git-scm.com](https://git-scm.com) herunter und installiere es.

### Benutzername und E-Mail konfigurieren  
```bash
git config --global user.name "Dein Name"
```
Legt deinen Namen fest, der bei jedem Commit angezeigt wird.
```bash
git config --global user.email "deine@email.de"
```
Legt deine E-Mail fest, die bei jedem Commit angezeigt wird.

### Editor für Git setzen (optional)  
```bash
git config --global core.editor "code --wait"
```
Legt den Texteditor fest, den Git für Eingaben benutzt (z. B. für Commit-Nachrichten).

### Konfiguration anzeigen  
```bash
git config --list
```
Zeigt alle Git-Einstellungen, die aktuell gelten.

---

## Repository starten oder klonen

### Neues Repository erstellen  
```bash
git init
```
Erstellt einen neuen Git-Ordner im aktuellen Projekt, damit du mit Versionskontrolle arbeiten kannst.

### Repository klonen  
```bash
git clone <repo-url>
```
Lädt ein bestehendes Online-Repository herunter, damit du lokal damit arbeiten kannst.

---

