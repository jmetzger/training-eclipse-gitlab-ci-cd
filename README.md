# Eclipse with (E)git Training

## Agenda 

 1. Technical Background 
     * [Projects with git](/projects-with-git.md)
     * [How does it work?](/git-how-does-it-work.md)
     * [The flow of git](/git-the-flow.md)
     * [Git and its objects](/git-objects.md) 
     * [5-goldene-Regeln - Zerstörung](/5-goldene-regeln.md)

 1. Eclipse (Basics)
     * [Prepare Perspective for good user experience](/tipps-tricks/prepare-perspective.md)
     * [Create/Initialize Repository/Project](/eclipse/create-repo.md)
     * [Eclipse Icons](/eclipse/icons.md)
     * [Git-Commands in eGit](/eclipse/git-commands-in-egit.md) 
     * [Setup Identity](/eclipse/setup-identity.md)
     * [Staging Area](/eclipse/staging-area.md)
     * [Log](/eclipse/log.md)
     * [Commit](/eclipse/commit.md)
     * [Add](/eclipse/add.md)
     
  1. Commands - Commandline (with tipps & tricks) 
     * [git add + Tipps & Tricks](add.md)
     * [git commit](commit.md)
     * [git log](log.md)
     * [Beautify Logs](beautify-log.md)
     * [git config](config.md) 
     * [git show](show.md)
     * [Needed commands for starters](started-commands.md)
     * [git branch](branch.md)
     * [git checkout](checkout.md)
     * [git merge](merge.md)
     * [git tag](tag.md)
     * [git remote -v](remote.md)
   
 1. Advanced Commands 
     * [git reflog](reflog.md) 
     * [git reset - Back in Time](reset.md) 
 
 1. GIT Mergetools 
     * [git mergetools](/mergetools.md) 
  
 1. gitlab + CI/CD 
    * [gitlab ci/cd Überblick](/gitlab/01-ci-cd-overview.md)
    * [gitlab stages](/gitlab/03-example-running-stages.md)
 
 1. Documentation (git)
    * [GIT pdf](https://schulung.t3isp.de/documents/pdfs/git/git-training.pdf)
    * http://wiki.eclipse.org/EGit/User_Guide
    * [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
    * [Conventional Commits](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)
 1. Documentation (gitlab)
    * https://about.gitlab.com/blog/2020/12/10/basics-of-gitlab-ci-updated/
 

## Backlog 
   
  1. Eclipse/STS(Spring Tool Suite) 
     * [Increasing Icon Size](/tipps-tricks/icon-size.md)
     * [Installation of Eclipse](/installation/eclipse.md) 
     * [Installation of STS (Spring Tool Suite)](/installation/sts.md)
     * [Prepare Perspective for good user experience](/tipps-tricks/prepare-perspective.md)
     * [Create/Initialize Repository/Project](/eclipse/create-repo.md)
     * [Eclipse Icons](/eclipse/icons.md)
     * [Git-Commands in eGit](/eclipse/git-commands-in-egit.md) 
     * [Setup Identity](/eclipse/setup-identity.md)
     * [Staging Area](/eclipse/staging-area.md)
     * [Log](/eclipse/log.md)
     * [Commit](/eclipse/commit.md)
     * [Add](/eclipse/add.md)
     * [Edit markdown in eclipse with plugin](https://marketplace.eclipse.org/content/markdown-text-editor)
 
  1. Features 
     * [Partial Clone](partial-clone.md) 
     * [Hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)

  1. GIT-Server 
     * [GIT Server](git-server.md) 

  1. Golden 
     * [5-goldene-Regeln](5-goldene-regeln.md)

  1. Tipps & Tricks (git / git bash)

     * [Konfigurationseinstellung löschen](/tipps-tricks/config-loeschen.md)
     * [Anderen Editor verwenden](/tipps-tricks/anderen-editor.md)
     * [Platz sparen mit dem shallow clone + neu pushen](/tipps-tricks/shallow-clone.md)
     * [Branch aus bestehendem Branch neu erstellen (alles auf Anfang!)](/tipps-tricks/branch-orphan.md)
     * [Arbeiten mit git replace](https://git-scm.com/book/en/v2/Git-Tools-Replace)
     * [ssl Verifizierung ausschalten (quick & dirty)](/tipps-tricks/ssl-verify.md)
     * [generic no-ff](/tipps-tricks/generic-no-ff.md)
  
  1. GIT-Guis
     * https://git-scm.com/download/gui/windows 
     * https://github.com/DmitryZhelnin/git-extensions-intellij
     * https://github.com/gitextensions/gitextensions/
     * https://git-fork.com/  

  1. Exercises 
     * [Create simple conflict on commandline](/exercises/conflict-commandline.md) 
     * [Conflict merge-request](/exercises/conflict-merge-request.md)

  1. Documentation 
     * [GIT pdf](https://schulung.t3isp.de/documents/pdfs/git/git-training.pdf)
     * http://wiki.eclipse.org/EGit/User_Guide
     * https://schulung.t3isp.de/documents/pdfs/git/git-training.pdf
     * https://git-scm.com/book/de/v2
     * https://git-lfs.github.com/
     * https://de.wikipedia.org/wiki/Liste_von_Git-GUIs
     * https://git-scm.com/download/gui/windows

  1. Off-Topic 
     * [Alternatives jira/confluence](jira-confluence-alternatives.md)





 

## SHA1 - checksums & backgrounds 

  * git extensively works with checksums in the background
  * a checksum is a 40-char long hex-string ( a unique checksum of the data ) 
  * every object gets a checksum
    * blogs
    * trees
    * commits
    * tags

## Lab 4: Find created object

```
# Works only within git bash or Linux 
# Just for reference here !! 
cd .git 
cd objects 
ls -la 
# you will find a directory name with the 
# first 2 chars of the object, e.g. 
# drwxr-xr-x   3 jmetzger  staff  102 26 Okt 16:28 4f
```

```
# change into that directory
# Hint: Replace name with your directory name 
cd 4f 
# your object 
ls -la 
# 51d02eb27b6bdf1741ad48ccf6f7dc3326bbd2
```

```
# now let us see the content 
# (taking the 4 letters of the object is sufficient) 
git cat-file -p 4f51
my first line 
```

```
# and the type of object 
git cat-file -t 4f51
blob
```












##  Merge changes -> merge 

  * You can merge, if you want to get changes from another branch
  * A typical scenario would be:
    * You are in master
    * Checkout a feature branch 
    * Work on a feature
    * Checkout master
    * merge changes from feature-branch 
  * You merge feature from another branch into your current branch
    * with -->
    * git merge your-feature-branch   





## Lab 10: Exploring HEAD (commandline) 

``` 
cd .git 
cat HEAD 
# ref: refs/heads/master
cat refs/heads/master 
# f80891db4afa604b243bd06a5779fee88c3cad53
# compare this with the last commit - id
# What do you notice ? 
git lg -1 
```

## Replay changes in other branch + changes on current branch -> rebase (commandline) 

  * Change into branch (z.B.feature-4711) 
  * git rebase master 
  * -- how does it work ? ->
    - go back to the point where the branch was created 
    - apply change from master
    - at the end apply changes from feature-4711
  * -- ATTENTION ->
    - only do rebasing in your own "local" branch (NO ! collaborative branches)
    - never rebase, after push is done and branch is shared with others ! 


## Cancellation -> revert (commandline) 

  * Take back the last change \\ But: you will have an additional log entry

``` 
# commandline 
git revert
```

```
# Eclipse/EGit 
1) Go to Log -> Right Click -> Show In -> History 
2) Right Click on Commit (you want to revert) -> Revert 
```

## From -> local repository -> to -> remote repository -> why ? 

### Why ? 
 
  * data is saved outside of my system 
  * others can access it too (collaboration, e.g. on a feature)



## Publish the local changes remote 

  * (commandline) git push origin master 
  * (Eclipse/Egit): Right click -> Team -> Push to Upstream 

## Tagging of a current version (locally)

  * eclipse/EGit -> Team -> Advanced -> Tag 

```
git tag -a v0.0.1 -m "Commit Message"
git push --tags 
```
## Getting an old revision of a file 

```
1) Rechte Maustaste 
2) Replace With (on top of entry Team) Previous Revision/Commit 
```

## Clone an online session into a new (none existant) directory ==== 

  * git bash (on the desktop - right click) 
  * git clone https://url schulung2

## where is configuration saved ? 

  * on your local system the general configuration is saved in a file.
  * Linux/Mac: ~/.gitconfig
  * --
  * example Mac: /Users/jmetzger/.gitconfig 
  * example Linux: /home/jmetzger/.gitconfig
  * example Windows: C:\Users\<user_name>\.gitconfig 

## Commit - messages: what for and why should they be speaking ? 

  * other participants should be able to see changes based on commits
  * good commit - message: reduces the time for search (for other participants) - more efficient
  * search more easily and thoroughly (e.g. for later debugging)  
  * eventually included in the changelog and other tools

## Commit - message : structure 

  * line 1: short! summary only(!) chars and letters 
  * line 1: max. 50 chars
  * line 1: best practice -> issue number/logical unit, then ":", then summary  \\ e.g. \\ modulexy: Fixed problems with memory management
  * line 2: EMPTY
  * line 3: thorough description of commit
  * line 3: max. 72 chars 
  * line 3: to structure: *, -, # possible 
  * line 3: time: presence 
  * line 3: do not write, what do you did, but why.

## The cleanup: removal and untracking : git rm (commandline) 

``` 
git rm 
# removes the files locally (working directory) 
# as well as for next staging. 
# In the next commit the file will not be contained anymore.

git rm --cached 
# if i only want to "untrack" a file (so it should be in the repo anymore), 
# but want to keep it locally)
```
 
## Troubleshooting ssh -> repo (tortoise/openssh) 

```
It is either possible to use openssh or plink.exe. 
Here are the most important settings for ssh.
```
 
  * git bash: echo $GIT_SSH \\ it should be: C:\Program Files\Git\usr\bin\ssh.exe here 
  * if not: export GIT_SSH="C:\Program Files\Git\usr\bin\ssh.exe" 
  * in addition in tortoisegit under settings -> network the should be the following: \\ C:\Program Files\Git\usr\bin\ssh.exe 




  

  
