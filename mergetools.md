# Mergetools 

## Welche Tools sind auf dem System vorhanden 

```
git mergetool --tool-help
```

## Meld (Windows) 

  *  https://meldmerge.org/

## Configuration in Git for Windwos (git bash) 

```
# you have to be in a git project 
git config --global merge.tool meld
git config --global diff.tool meld
# Should be on Windows 10 
git config --global mergetool.meld.path “/c/Users/Admin/AppData/Local/Programs/Meld/Meld.exe”
# do not create an .orig - file before merge 
git config --global mergetool.keepBackup false
```  

## How to use it 

```
# when you have conflict you can open the mergetool (graphical tool with )
git mergetool
```
