# Mergetools 

## Welche Tools sind auf dem System vorhanden 

```
git mergetool --tool-help
```

## Meld (Windows) 

  *  https://meldmerge.org/

## Meld - Configuration in Git for Windows (git bash) 

```
# you have to be in a git project 
git config --global merge.tool meld
git config --global diff.tool meld
# Should be on Windows 10 
git config --global mergetool.meld.path “/c/Users/Admin/AppData/Local/Programs/Meld/Meld.exe”
# Windows 10 - different installation path 
git config --replace-all --global mergetool.meld.path  '/c/Program files/Meld/Meld.exe'


# do not create an .orig - file before merge 
git config --global mergetool.keepBackup false
```  

## TortoiseGitMerge - Configuration 

``` 
# If you have tortoisegit installed on your system, you can use tortoisegitmerge for git for windows as well
# Do not keep orig-file 
git config --global merge.tool tortoisegit 
git config --global mergetool.keepBackup false
```

## How to use it 

```
# when you have conflict you can open the mergetool (graphical tool with )
git mergetool
```
