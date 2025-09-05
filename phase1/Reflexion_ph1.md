# Reflexion Kröpelin
## Phase 1 – Projektinitialisierung mit Git und DDEV
### Was ist Markdown?
* Ich wusste zwar, dass Markdown ein Text-Datei-Format ist, hatte das aber bisher noch nicht angewendet.
* Der Link zum Markdown-Cheatsheet konnte zwar die Syntax zeigen, aber nicht wie das dann aussieht. Ich habe mich also erstmal umgeschaut, wie ich das dann angezeigt bekomme. Dazu hatte ich kurz Obsidian installiert, bis ich feststellte, dass VS Code .md als Previews anzeigen kann – das reichte mir.
* Da ich für CheatSheets gerne Tabellen benutze, die aber mit Markdown eher umständlich zu generieren sind, habe ich mich entschieden diese per Html anzulegen und im Markdown unterzubringen. Meine eigentlich unübliche Methode dafür ist: Die Tabellen in LibreOffice zu schreiben und formatieren, dann aber als Html abzuspeichern. So kann ich das Html dann mit dem Browser öffnen und den Quelltext kopieren. Er wird dadurch zwar etwas umfangreicher (inline CSS), aber die Erarbeitung des Wissens ist komfortabler.

### Installation von DDEV:
* Es war einfach DDEV zu finden und die Installationsanleitung dazu. Allerdings hat der vorgegebene Weg erstmal nicht funktioniert, weil mein WSL wohl schon älter war und der Befehl `wsl –install` Ubuntu `–name DDEV` nicht funktioniert hat.
* Dafür hat aber der erste Befehl `wsl –install` gleich ein Ubuntu installiert, welches ich mit `wsl –unregister Ubuntu` wieder entfernt habe. Danach `wsl –update` und dann funktionierte auch das install mit Benamung.
* dann war erstmal etwas Grundlagen Linux nötig, um zu wissen wo jetzt der Projektordner am besten untergebracht wird (https://wiki.ubuntuusers.de/Verzeichnisstruktur/)
* `ddev config –auto` – hat man leider nur im Video so gesehen, funktioniert natürlich besser, weil ich erstmal bei `ddev config` nicht recht wusste, wie die aufploppende Abfrage zu verstehen ist

### Anlegen von Git
* erstes Problem war, dass ich nicht bedacht hatte, dass ich mit WSL und DDEV ja eine Virtuelle Maschine habe und Git also erstmal in DDEV installieren muss
* auch habe ich die Einrichtung von Git etwas durcheinander angefangen, weil ich wohl vergessen hatte den global User und E-Mail anzulegen
* Letztlich hat das aber alles funktioniert

### Verbinden von Git zu GitHub
* das war tatsächlich ein Zeitfresser – eigentlich dachte ich, ich kenne die Schritte, aber bei den Versuchen via Https zu verbinden, wurde immer der User und Password abgefragt – welche dann aber abgelehnt wurden, weil Git das so nicht unterstützt
* also Recherche – ich kam darauf, dass ich SSH benutzen müsste, das Anlegen von SSH-Keys in Linux hab ich hinbekommen
* aber dennoch wollte Git sich nicht verbinden …
* bis ich merkte, dass die GitHub-Anweisungen für die Verbindung auf Https gemeint waren
* man kann aber auch die SSH-Verbindung auswählen, mit leicht veränderten Anweisungen … und siehe da, dann hat es funktioniert
* allerdings habe ich nicht das GitHub-Repository in meinen lokalen Ordner Kursverwaltung geklont. Denn das hätte zur Folge gehabt, dass ich im lokalen Repository Kursverwaltung noch einen zweiten Ordner Kursverwaltung generiert hätte (den von GitHub geklonten). Das hielt ich für eine verwirrende Struktur und habe statt dessen, das lokale Repository Kursverwaltung mit dem GitHub-Repository verknüpft, so wie das GitHub auch vorschlägt. (siehe CheatSheet)

### Arbeiten in Branches mit VSCode und Verbindung zu GitHub
* es hat sich herausgestellt, dass man in VSCode zwar Branches anlegen kann und in ihnen arbeiten
* aber die Verbindung zu GitHub und damit das commiten und pushen funktioniert nicht, weil VSCode unter Windows läuft und auf andere SSH-Keys zugreift als die SSH-Keys von DDEV, die mit GitHub verbunden sind
* also muss ich das commiten und pushen über die Ubuntu-Console aus DDEV heraus machen
* kleine Verunsicherung beim pushen des neuen Branches main_ph1 – weil ich [hier bei git-scm.com](https://git-scm.com/docs/git-branch#Documentation/git-branch.txt---set-upstream "https://git-scm.com/docs/git-branch#Documentation/git-branch.txt---set-upstream") gelesen habe, dass `--set-upstream` nicht mehr aktuell ist – aber glücklicherweise ist `-u` auf `--set-upstream-to=` umgelabelt worden

### Unerwartete Verwirrung der Git-Accounts
* aber irgendwie hat VSCode dann doch commited - nur eben nicht gepushed
* was dazu führte, dass ich nach erfolgreichem Push des neuen Branches main_ph1 plötzlich einen commit von meinem zweiten git-Account (der auch auf meinem Rechner lebt und eine eigene Verbindung zu GitHub pflegt) in meiner Timeline hatte
* das war inakzeptabel!
* doch bevor ich jetzt wieder die Docu wälze und wieder Zeit an Git verliere, habe ich die komplette Gittisierung neu aufgesetzt (.git und alles andere gelöscht, das GitHub Repo gelöscht)
* Learning: git-Aktionen nur über die Ubuntu/DDEV Konsole, weil nur da die richtigen Accounts und Keys gelten

### pushen des neuen Branches
* das pushen des neuen Branche mit `git push -u origin main_ph1` hat offenbar nicht richtig funktioniert (obwohl man überall liest, dass man das so macht), weil es offenbar einen alternativen upstream Pfad anlegt oder so ähnlich (ich hatte danach Probleme aus local/main zu pullen)
* die bessere Variante ist `git push origin main_ph1`, wie es [hier im git Buch](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches "https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches") unter Pushing beschrieben ist

### Probleme mit dem .gitignore
* leider wird beim Branchen das .gitignore nicht mit übernommen, so dass alles was ich eigentlich von GitHub fernhalten wollte, plötzlich wieder als untracked erscheint
* also muss ich für jeden Branch das .gitignore neu schreiben (sicher gibt es Alternativen, aber momentan reicht mir das so)
* beim mergen des main_ph1 in das main auf GitHub hat sich gezeigt, dass da jetzt ein gitignore zuviel ist – sollte ich jetzt jedesmal, wenn ich merge dieses Problem bekommen??
* dieses Problem hat sich mit dem Neuaufsetzen des Git erledigt - wahrscheinlich hatte ich beim ersten Versuch den Branch angelegt ohne das .gitignore zu adden