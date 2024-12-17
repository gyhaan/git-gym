# Gym - Git Exercise

## Bundle 1

### Exercise 1

```bash
PS C:\Users\Hp\Desktop\Practice\git-gym> git init
PS C:\Users\Hp\Desktop\Practice\git-gym> git branch -m master main
PS C:\Users\Hp\Desktop\Practice\git-gym> git add .
PS C:\Users\Hp\Desktop\Practice\git-gym> git commit -m 'Init Commit'
PS C:\Users\Hp\Desktop\Practice\git-gym> git branch dev
PS C:\Users\Hp\Desktop\Practice\git-gym> git checkout dev
PS C:\Users\Hp\Desktop\Practice\git-gym> git branch test dev
PS C:\Users\Hp\Desktop\Practice\git-gym> git branch -D test
Deleted branch test (was 1a7819c).
PS C:\Users\Hp\Desktop\Practice\git-gym> git push -u origin dev
```

### Exercise 2

```bash
PS C:\Users\Hp\Desktop\Practice\git-gym> git add home.html
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash save 'home'
Saved working directory and index state On main: home
PS C:\Users\Hp\Desktop\Practice\git-gym> git add about.html
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash save 'about'
Saved working directory and index state On main: about
PS C:\Users\Hp\Desktop\Practice\git-gym> git add team.html
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash save 'team'
Saved working directory and index state On main: team
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash list
stash@{0}: On main: team
stash@{1}: On main: about
stash@{2}: On main: home
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\Hp\Desktop\Practice\git-gym> git stash pop "stash@{1}"
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (a22150d449c36cb59e4fb6fb9c8066fa9060c520)
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash list
stash@{0}: On main: team
stash@{1}: On main: home
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash pop "stash@{1}"
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (280b015742d9d2f363e0178ad6f3a127f18aacac)
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash pop stash@{0}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\Hp\Desktop\Practice\git-gym> git stash pop "stash@{0}"
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped stash@{0} (52a7c847c39fdcb5c32dd899cd9affebc402baac)
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash
Saved working directory and index state WIP on main: ab46c5c Bundle 1 - Exercise 1
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash list
stash@{0}: WIP on main: ab46c5c Bundle 1 - Exercise 1
PS C:\Users\Hp\Desktop\Practice\git-gym> git stash pop "stash@{0}"
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped stash@{0} (84ca6de48ceae7f3ac0634cbd51009777c1557ca)
PS C:\Users\Hp\Desktop\Practice\git-gym> git commit -m 'about and  home'
[main 1081cc2] about and  home
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\Hp\Desktop\Practice\git-gym> git reset --hard
HEAD is now at 1081cc2 about and  home
PS C:\Users\Hp\Desktop\Practice\git-gym> git reset --hard
HEAD is now at 1081cc2 about and  home
```
