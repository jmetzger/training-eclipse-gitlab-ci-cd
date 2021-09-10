# git commands in Eclipse (EGit)

  * https://wiki.eclipse.org/EGit/Mapping_Git_Commands

| git | eclipse/EGit |
| --- | --- |
|add: | "Add to Index" -> toolbar/menubar item to add all changes in selected files. <br> "Team -> Add to Index" to add all changes in selected files. <br> Drag-and-drop in "Git Staging" view <br>Drag-and-drop in "Synchronization" view. <br> "Compare With.." to stage or unstage line-by-line | 
| annotate: | "Team -> Show in Annotations" |
| branch:  | "Checkout"/"Switch To" <br>toolbar/menubar item to list, create, rename and delete local branches and remote-references. <br> toolbar of Commit views to create a branch from that commit right-click menu of commits listed in history |
| checkout: | "Checkout"/"Switch To" toolbar/menubar item to checkout a local branch. <br> "Replace With..." to checkout a single file. <br> right-click menu of commits listed in history or reflog <br> right-click menu of branches in "Git Repositories" view toolbar of Commit views |
| cherry-pick: | right-click menu of commits listed in history. toolbar of Commit views | 
| clone: | toolbar of Git Repositories" view | 
| commit: | "Commit" toolbar/menubar item "Team -> Commit" <br> "Commit" toolbar in "Git Staging" view |
| config: | "Properties" view Preferences: "Team -> Git" "Team -> Remote -> Configure..." |
| diff: | "Team -> Advanced -> Synchronize" to compare branches <br> "Team -> Synchronize Workspace" to compare working tree to HEAD <br> "Compare With" for specific files double-click items in either "Git Staging" changes windows |
| fetch: | "Fetch changes from upstream" toolbar/menubar "Team -> Fetch changes from upstream" |
| init: | toolbar of Git Repositories" |
| log: | "Team -> Show in history" | 
| merge: | "Team -> Merge" |
| mv: | Implicit when file is renamed | 
| pull: | "Pull" toolbar/menubar item "Team -> Pull" | 
| push: | "Push to Upstream" toolbar/menubar item default push <br> "Team -> Push to Upstream" \\ ditto "Team -> Push..." for explicit push | 
| rebase: | "Rebase" toolbar/menubar item "Team -> Rebase" | 
| reflog: | "Git Reflog" view |
| remote: | "Team -> Remote" "Branches -> Remote Tracking" in "Git Repositories" view | 
| reset:  | "Reset" toolbar/menubar item to reset a branch "Team -> Reset" ditto | 
| revert: | right-click menu of commits listed in history. | 
| rm: | implicit when file is deleted |
| status: | implicit in decorations, "Git Staging View" | 
| tag: | "Team -> Advanced -> Tag...", annotated tags only toolbar of Commit views, ditto |
