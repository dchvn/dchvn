- 👋 Hi, I’m @dchvn
- 👀 I’m interested in OLAP, Scala, Python
- 🌱 I’m currently learning Scala, Python

# PR - resolve conflict
## Merge with master
You will do not want to use it!
## Rebase with master
``` bash
git fetch origin/master
git rebase origin/master

# after resolve conflict
git add path/to/files
git add ..

git rebase --continue

# if you want abort rebase process
git rebase --abort

