# Shallow Clone 

## Walkthrough (nicht pushbar)

```
# ohne Einschränkung 1428 objekte aktuell (stand 09.09.2021) 
git clone https://github.com/jmetzger/mariadb-fuer-entwickler.git


## Clone only last 501 commits 
git clone --depth=501 https://github.com/jmetzger/mariadb-fuer-entwickler.git mfe 
cd mfe

## Es steht der Hinweis grafts im letzten Logeintrag.
## Der letzte Logeintrag (also das erste commit hat ein parent),
## dadurch kann es nicht in ein neues Repo gepushed werden.


```


## Walkthrough (pushbar) 

```
## Nur 201 commits abholen damit das handling einfacher ist.
git clone --depth=501 https://github.com/jmetzger/training-git.git gt 

## Jetzt Historie neu aufbauen
cd gt
## sha - id des ersten commits (letzter log eintrag finden) 
## z.b. cc43 
## tree rausfiltern und auf dieser Basis einen neuen Initial-Commit ohne eltern erstellen. 
echo "Start of truncated history"  | git commit-tree cc43^{tree}
## es erscheint die neue commit-id z.B. 56c3.....

## Diese nehmen wir um darauf die restliche Historie draufzuflanschen 
git rebase --onto 56c3 cc43 

## historie ist fertig

## Jetzt remote umbiegen 
git remote set-url origin https://url_zum/neuen_repo.git 

## bzw. master
git push origin main

```
