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
