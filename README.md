
# Git Anleitung – Komplett
test

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

## Dateien verwalten

### Status prüfen  
```bash
git status
```
Zeigt dir, welche Dateien geändert, neu oder bereit zum Speichern (gestaged) sind.

### Dateien zur Staging Area hinzufügen  
```bash
git add <datei>
```
Bereitet eine einzelne Datei vor, um beim nächsten Commit gespeichert zu werden.
```bash
git add .
```
Bereitet alle geänderten Dateien vor.

### Dateien aus Staging entfernen  
```bash
git reset <datei>
```
Entfernt eine Datei aus der Vorbereitung für den nächsten Commit, lässt sie aber unverändert.

### Datei löschen  
```bash
git rm <datei>
```
Löscht eine Datei aus deinem Ordner und bereitet das Löschen für den nächsten Commit vor.

### `.gitignore`  
Datei, in der du festlegst, welche Dateien oder Ordner Git nicht verfolgen soll (z. B. Log-Dateien oder temporäre Dateien).

---

## Commits

### Commit erstellen  
```bash
git commit -m "Nachricht"
```
Speichert alle vorbereiteten Änderungen dauerhaft im Repository mit einer kurzen Beschreibung.

### Letzten Commit ändern  
```bash
git commit --amend
```
Ändert die letzte Commit-Nachricht oder fügt neue Änderungen hinzu, bevor du einen neuen Commit machst.

### Letzten Commit rückgängig machen (soft)  
```bash
git reset --soft HEAD~1
```
Entfernt den letzten Commit, aber behält die Änderungen zum Bearbeiten.

### Alles zurücksetzen (hard)  
```bash
git reset --hard
```
Verwirft alle Änderungen seit dem letzten Commit – sei vorsichtig, alles geht verloren!

---

## Branches verwalten

### Branches anzeigen  
```bash
git branch
```
Listet alle vorhandenen Branches (Zweige) in deinem Projekt auf.

### Neuen Branch erstellen  
```bash
git branch <name>
```
Erstellt einen neuen Zweig, um parallel zu arbeiten.

### Branch wechseln  
```bash
git checkout <name>
```
Wechselt zu einem anderen Branch, um daran zu arbeiten.

### Branch erstellen und wechseln  
```bash
git checkout -b <name>
```
Erstellt einen neuen Branch und wechselt direkt darauf.

### Branch löschen  
```bash
git branch -d <name>
```
Löscht einen Branch, den du nicht mehr brauchst.

---

=======










































































































































































































## Branches zusammenführen

### Branch mergen  
```bash
git merge <branch>
```
Fügt die Änderungen eines anderen Branches in den aktuellen Branch ein.

### Rebase  
```bash
git rebase <branch>
```
Überträgt deine Änderungen auf einen anderen Branch, um eine sauberere Historie zu schaffen.

### Cherry-pick  
```bash
git cherry-pick <commit-hash>
```
Nimmt einen einzelnen Commit von einem anderen Branch und fügt ihn in deinen aktuellen Branch ein.

---

## Änderungen ansehen

### Commit-Historie anzeigen  
```bash
git log
```
Zeigt alle bisherigen Commits mit Details an.

### Kompakte Historie  
```bash
git log --oneline
```
Zeigt die Commit-Historie in Kurzform.

### Historie mit Graph  
```bash
git log --graph --all --oneline
```
Zeigt eine Übersicht der Branch-Verzweigungen und Commits.

### Änderungen anzeigen  
```bash
git diff
```
Zeigt den Unterschied zwischen aktuellen Dateien und dem letzten Commit.

### Gestagte Änderungen anzeigen  
```bash
git diff --staged
```
Zeigt Änderungen, die zum nächsten Commit vorbereitet sind.

---

## Remote verwalten

### Remote hinzufügen  
```bash
git remote add origin <url>
```
Verknüpft dein lokales Repository mit einem Online-Repository.

### Remote anzeigen  
```bash
git remote -v
```
Zeigt alle verbundenen Remote-Repositories an.

### Änderungen pushen  
```bash
git push
```
Schickt deine lokalen Commits auf das Remote-Repository, damit andere sie sehen.

### Ersten Push mit Upstream-Verknüpfung  
```bash
git push --set-upstream origin <branch>
```
Erstellt eine Verbindung zwischen lokalem Branch und Remote-Branch für zukünftige Pushes.

### Änderungen holen (fetch)  
```bash
git fetch
```
Lädt neue Änderungen vom Remote-Repository, ohne sie zu übernehmen.

### Änderungen holen und mergen (pull)  
```bash
git pull
```
Lädt neue Änderungen und fügt sie direkt in deinen aktuellen Branch ein.

---
## Temporäre Änderungen speichern

### Änderungen stashen  
```bash
git stash
```
Speichert deine aktuellen Änderungen temporär weg, ohne sie zu committen.

### Liste aller Stashes  
```bash
git stash list
```
Zeigt alle gespeicherten temporären Änderungen.

### Stash anwenden  
```bash
git stash apply
```
Bringt die zuletzt gespeicherten Änderungen zurück in dein Arbeitsverzeichnis.

### Stash anwenden und löschen  
```bash
git stash pop
```
Bringt Änderungen zurück und entfernt sie aus der Liste der gespeicherten Stashes.

---

## Hilfe und Version

### Git Version anzeigen  
```bash
git --version
```
Zeigt die installierte Git-Version.

### Hilfe zu einem Befehl anzeigen  
```bash
git help <befehl>
```
Zeigt die Anleitung zu einem Git-Befehl.

---
>>>>>>> Edward_2
