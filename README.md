# Tips

## Restore a file from a specific commit
```sh
 $ git checkout <commit-hash>~1 -- <filename>
```

## Reset a file with HEAD
```sh
$ git reset HEAD <path-to-file-or-folder>
```

### Reset a file with HEAD
```sh
$ git reset HEAD <path-to-file-or-folder>
```

### Create a branch
```sh
$ git checkout -b branch-name
$ git checkout -b <branch-name> origin/<branch-copy-from>
```

### Pull remote branch with rebase
```sh
$ git pull --rebase origin <remote-branch>
```

### Delete a branch
#### Local
```sh
$ git branch -d <branch-name>
```
#### Remote
```sh
$ git push origin --delete <branch-name>
```

### Force to a branch
```sh
$ git reset --hard origin/<branch-name>
```

### Push to remote branch
```sh
$ git push -u origin <branch-name>
```

### Un-track the file:
```sh
$ git update-index --assume-unchanged <path-to-file>
```

### Keep track again:
```sh
$ git update-index --no-assume-unchanged <path-to-file>
```

### Stop keeping track a folder:
```sh
$ git ls-files | tr '\n' ' ' | xargs git update-index --assume-unchanged
```

### Get conflicted files:
```sh
$ git diff --name-only --diff-filter=U
```

### View log on remote branch:
```sh
$ git log origin/<branch-name>
```

### Reset/revert a file to HEAD
```sh
$ git reset HEAD <path-to-file>
```

### Stop tracking a file
```sh
$ git rm --cached <path-to-file>
```

### Edit conflict use their/ours files:
```sh
$ git checkout --theirs <path-to-file>
$ git checkout --ours <path-to-file>
```

### Rename branch:
```sh
$ git branch -m <oldname> <newname>
$ git branch -m <newname> (Rename the current one)
```

### Remove folder/file as added to stage folder: (as cannot use "git reset" because we dont have it on origin)
```sh
$ git rm --cached -r <path-to-file-or-dir>
```

### Remove file in commit but keep it locally
```sh
$ git rm --cached PATH_TO_FILE
```

### Remove untracked files/folders:
```sh
$ git clean -df
```

### Fixing file "file is unmerged" or cannot checkout these files after solving conflict, we use:
```sh
$ git reset
```

- Install compass in case of write permissions/permitted
$ sudo gem install -n /usr/local/bin compass 

- Show info of specific stash:
$ git stash show -p stash{1}

### Back to previous branch:1
```sh
$ git checkout @{-1}
```

### How to tag:
```sh
$ git tag (list)
$ git fetch —tags
$ git tag -a v0.1 <hash_id> -m "Message here" 
$ git push -—tags origin master
$ git tag -—delete <name> (Delete local)
$ git tag —-delete origin <name> (Repo)
```

### Revert file with specific commit
```sh
$ git checkout c5f567 -- file1/to/restore file2/to/restore
```

### Check history log:
```sh
$ git reflog
```

### Apply files from specific stash:
```sh
$ git checkout stash@{0} -- <filename>
```

### Diff last commits to current HEAD
```sh
$ git diff HEAD~2..HEAD / git diff --name-status HEAD~2..HEAD
```

### View file in a specific branch:
```sh
$ git show <branch-name>:<path-to-file>
```

### Rename dir properly:
```sh
$ git mv casesensitive tmp
$ git mv tmp CaseSensitive
```

### Stash specific files:
```sh
$ git stash push -m <yourMessage> "app/**/submission*"
```

### Update.gitignore except few files:
```sh
!path/to/file
```
