- 👋 Hi, I’m ```dch nguyen```
- 👀 I’m interested in OLAP, Scala, Python
- 🌱 I’m currently learning Scala, Python

# My Git Note

## PR - resolve conflict
### Merge with origin/master
You will not want to use it!
``` bash
$ git fetch origin/master
$ git merge origin/master

# Resolve conflict and create merge commit
$ git add path/to/files

$ git commit -m "blah blah"
```

### Rebase with origin/master
``` bash
$ git fetch origin/master
$ git rebase origin/master

# after resolve conflict
$ git add path/to/files

$ git rebase --continue

# if you want abort rebase process
$ git rebase --abort

# Push
$ git push -f
```

## Branch

``` bash
# Create new branch from
$ git checkout -b origin/SPARK-xxx

# Push to remote
$ git push remote_name SPARK-xxx:SPARK-xxx

```
``` bash
# Merge all change as single commit when you want create new branch
$ git checkout -b merge_branch master
$ git merge --squash feature_1_branch
```
## Commit
``` bash
# rebase multiple commits to single commit
$ git rebase -i HEAD~N  # N is number of commit
# change 'pick' key word to 'squash'
```
``` bash
# modify comment
$ git commit --amend
# modify author
$ git commit --amend --author="Author Name <email@address.com>" --no-edit
```
## Remote
``` bash
# Show all current remote
$ git remote -v
```
``` bash
# Add new remote
$ git remote add remote_name https://blahblah.git
```
``` bash
# Delete a remote
$ git remote rm remote_name
```

## Cherry pick
Get commit from a branch
Git cherry-pick is useful tool but not a best practice(cause duplicate commits)
``` bash
# Find hash_commit in git log, and then pick that commit to current branch for applying
$ git cherry-pick <hash_commit>
$ git cherry-pick <hash_commit1> <hash_commit2> ...
```
``` bash
# Pick the latest commit from branch 'AAA'
$ git cherry-pick <AAA~1>
```
