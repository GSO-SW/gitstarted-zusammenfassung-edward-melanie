











































































































































































































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
