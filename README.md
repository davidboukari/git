# git

under contruction ...


## clone a repo
```bash
git clone <url>/project
cd  project
git remote add upstream <urlupstream>
git pull --rebase upstream master
```

## git add or reset to unadd
```
git add myfile

# unadd = reset
git reset myfile
```

## Update the last commit
```
git commit --amend -m "New commit message."
git push -f branchname
```

## squash (merge commits & messages)

```bash
git rebase -i HEAD~3
s to keep the commit but merge it
git push -f upstream master
```

## diff

```bash
git diff origin/branch1 origin/branch2...
git diff tag1 tag2 --
git diff tag1 tag2 -- | git apply
```

## patch
```bash
git diff tag1 tag2 -- > mypatch.patch
patch -i < mypatch
```

## git revert for Rollback
```bash
# See the log for a file
git log -- ./myfile

# See the changes to go from a version to a version for a file between 2 versions
git diff <version1> <version2> -- ./myfile

# See the changes to go from a version to a version for a file between 2 versions and apply it
git diff <version1> <version2> -- ./myfile | git apply
```

## Reset to a revision
```
reset --hard HEAD
```


## fetch
* Get the missing commit but not merge to the local branch, need to go git merge after to merge them
```
# Get the into local origin/master the commit
git fetch origin master
git  branch -a
git log --oneline master...origin/master
git diff master...origin/master
git merge origin/master master
```

## pull
* Get the missing commit and merge automaticaly to the local branch
```
git pull origin main
git pull --rebase upstream master
```

## git tag
```
git tag v0.0.1
git tag --list
```

## Delete
```
git branch -D mybranch
git push origin --delete mybranch
```

## git diff 
```
git diff origin/master origin/branch1 --name-only

```

