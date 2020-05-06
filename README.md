# git

under contruction ...

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
