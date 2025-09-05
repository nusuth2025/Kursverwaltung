## Phasenfragen für Phase 1
1. Welche grundlegenden DDEV-Befehle gibt es und wofür werden sie genutzt?
    * Antwort: siehe CheatSheet
2. Wie läuft der typische Workflow ab, um Änderungen mit Git zu versionieren?
    * Ich nehme an damit ist der tägliche Ablauf gemeint:
    git status, git add, git commit, git push, ggf. vorher noch ein git pull um Änderungen von Remote zu holen
3. Was ist der Unterschied zwischen git checkout -b und git switch?
    * git checkout -b branch erstellt einen neuen Branch und wechselt direkt dahin, git switch branch wechselt einfach nur in einen bereits bestehenden Branch
4. Welche Rolle spielen git remote und git remote -v?
    * beide zeigen die remote-Branches an, aber mit -v wird noch die Adresse der Verknüpfung angezeigt
5. Warum ist es wichtig, für jede Phase einen eigenen Branch anzulegen?
    * so lassen sich die Änderungen jeder Phase leichter nachvollziehen, ggf. sogar als unabhängige Branches replizieren