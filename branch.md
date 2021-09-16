# git branch

## Show branches

```
# locale branches + active branch (mit *)
git branch 
# remote branches
git branch -r 
# alle branches
git branch -a 
```

## Create branch based on commit (also past commit) 

```
git branch lookaround 5f10ca
```

## Delete unmerged branch 

```
git branch -d branchname # does not work in this case 
git branch -D branchname # <- is the solution 
```
