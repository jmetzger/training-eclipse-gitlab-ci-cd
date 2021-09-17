# 5 Goldene Regeln 

```
1. Kein git commit --amend auf bereits veröffentlicht (gepushed) commit.

2. Kein git reset vor bereits veröffentlichte (gepushed) commits 
(1234 (HEAD -letzter Commit) < 5412 (vö - HEAD~1 - vorletzte Commit ) -> kein reset auf 1234) 

(3. Nie Struktur in 2 Branches (z.B. Master / Feature-Branch) vor Merge gleichzeitig ändern)

4. Mach niemals ein git push --force (JM sagt) 

5. Kein Rebase auf bereits veröffentlichte commits (nach vö von Feature branchen) 
- ausser Feature-Branch kann online gelöscht und nochmal erstellt werden 

```
