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