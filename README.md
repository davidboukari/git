# git

## git checkout a file
```
git checkout HEAD -- my-file.txt
```

## git config
```
 git config --global core.editor "nano"
```

## change current branch name
```
git branch -m new-branch-name
```

# Reset to a commit version
```
git reset --hard 0d1d7fc32
```


## gitignore
* https://github.com/github/gitignore

## git diff branch.. (check all files also new files)
```
git diff origin/branch..
git diff origin/branch..testbranch
```

## git diff branch... (check only the same file)
```
git diff origin/branch...
git diff origin/branch...testbranch
```

## get fetch
```
# Get all update from remote branches remote/origin/.... after that just have to do the git diff remote/origin/branch..  
git fetch 

```


## Restore deleted file
* Restore a delete Jenkinsfile
```
git checkout HEAD -- Jenkinsfile
```

## clone specific branch
```
git clone --branch <branchname> <remote-repo-url>

or

git clone -b <branchname> <remote-repo-url>
```

## git log all commit
```
git log --oneline
9f4fd81 (HEAD) Add new path echo
d5332e3 (origin/swagger/v0.1.0) dependency:tree
2814210 (origin/master, master) Update doc
9aa7418 Initial commit

but to see all commit

git log --oneline --all
415581d (swagger/v0.1.0) Just to back up does not work
9f4fd81 (HEAD) Add new path echo
d5332e3 (origin/swagger/v0.1.0) dependency:tree
2814210 (origin/master, master) Update doc
9aa7418 Initial commit
```

## clone a repo
```bash
git clone <url>/project
cd  project
git remote add upstream <urlupstream>
git pull --rebase upstream master

git pull origin master
```

## rebase
```
git pull --rebase origin main

# if the update in the tmp branch do continue
git rebase --continue

git commit -am "xxxxx"
git push origin main
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

## diff get files from other branch
```
git diff ...mysourcebranch --name-only
file1
file2

git diff ...mysourcebranch -- file1 

git diff ...mysourcebranch -- file1  | git apply --
```

## diff

```bash
git diff origin/branch1 origin/branch2...
git diff tag1 tag2 
git diff origin/master origin/branch1 --name-only
git diff origin/master rev1 origin/dev rev2 --name-only
git diff tag1 tag2 | git apply --
git diff origin/master origin/dev | git apply --

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

# Tag a specific commit
git tag -a "v1.1.1" eb45467af765
```

## Delete
```
git branch -D mybranch
git push origin --delete mybranch
```

