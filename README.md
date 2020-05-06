# git

under contruction ...

## diff

```bash
git diff origin/branch1 origin/branch2...

git diff tag1 tag2 --
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
git diff 34a1af95fbe87de8b0cf3faa469cc5391b9598a2 2560646055f9bd7072206d209774c54e6a81bc8b -- ./myfile

# See the changes to go from a version to a version for a file between 2 versions and apply it
git diff 34a1af95fbe87de8b0cf3faa469cc5391b9598a2 2560646055f9bd7072206d209774c54e6a81bc8b -- ./myfile | git apply
```
