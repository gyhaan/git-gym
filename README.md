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

### Exercise 2

```bash
PS C:\Users\Hp\Desktop\Practice\git-gym> git checkout main
M       README.md
Switched to branch 'main'
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS C:\Users\Hp\Desktop\Practice\git-gym> git pull
Updating 07475f9..498a51e
Fast-forward
 services.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
PS C:\Users\Hp\Desktop\Practice\git-gym> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\Hp\Desktop\Practice\git-gym> git add .
PS C:\Users\Hp\Desktop\Practice\git-gym> git commit -m 'new branch'
[ft/service-redesign 7b051d9] new branch
 2 files changed, 39 insertions(+)
PS C:\Users\Hp\Desktop\Practice\git-gym> git push origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1012 bytes | 506.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/gyhaan/git-gym/pull/new/ft/service-redesign
remote:
To https://github.com/gyhaan/git-gym.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
PS C:\Users\Hp\Desktop\Practice\git-gym> git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Hp\Desktop\Practice\git-gym> git add .
PS C:\Users\Hp\Desktop\Practice\git-gym> git commit -m 'origin brnach'
[main 84df4e8] origin brnach
 1 file changed, 1 insertion(+)
PS C:\Users\Hp\Desktop\Practice\git-gym> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 318 bytes | 318.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/gyhaan/git-gym.git
   498a51e..84df4e8  main -> main
PS C:\Users\Hp\Desktop\Practice\git-gym> git switch ft/service-redesign
Switched to branch 'ft/service-redesign'
PS C:\Users\Hp\Desktop\Practice\git-gym> git diff ft/service-redesign main
diff --git a/README.md b/README.md
index defcdf4..fe61fb9 100644
--- a/README.md
+++ b/README.md
@@ -105,41 +105,3 @@ HEAD is now at 1081cc2 about and  home
 PS C:\Users\Hp\Desktop\Practice\git-gym> git reset --hard
 HEAD is now at 1081cc2 about and  home
```

## Bundle 2

### Exercise 1

```bash
PS C:\Users\Hp\Desktop\Practice\git-gym> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\Hp\Desktop\Practice\git-gym> git add .
PS C:\Users\Hp\Desktop\Practice\git-gym> git commit -m 'bundle-2 init commit'
[ft/bundle-2 a26d31a] bundle-2 init commit
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
PS C:\Users\Hp\Desktop\Practice\git-gym> git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Hp\Desktop\Practice\git-gym> git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 437 bytes | 218.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/gyhaan/git-gym/pull/new/ft/bundle-2
remote:
To https://github.com/gyhaan/git-gym.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```

### Exercise 2

````bash
  -PS C:\Users\Hp\Desktop\Practice\git-gym> git checkout -b ft/bundle-2
  -Switched to a new branch 'ft/bundle-2'
  -PS C:\Users\Hp\Desktop\Practice\git-gym> git add .
  -PS C:\Users\Hp\Desktop\Practice\git-gym> git commit -m 'bundle-2 init commit' -[ft/bundle-2 a26d31a] bundle-2 init commit
- 1 file changed, 11 insertions(+)
- create mode 100644 services.html
  -PS C:\Users\Hp\Desktop\Practice\git-gym> git push
  -fatal: The current branch ft/bundle-2 has no upstream branch.
  -To push the current branch and set the remote as upstream, use
-
- git push --set-upstream origin ft/bundle-2
- -To have this happen automatically for branches without a tracking
  -upstream, see 'push.autoSetupRemote' in 'git help config'.
- -PS C:\Users\Hp\Desktop\Practice\git-gym> git push -u origin ft/bundle-2
  -Enumerating objects: 4, done.
  -Counting objects: 100% (4/4), done.
  -Delta compression using up to 8 threads
  -Compressing objects: 100% (3/3), done.
  -Writing objects: 100% (3/3), 437 bytes | 218.00 KiB/s, done.
  -Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
  -remote: Resolving deltas: 100% (1/1), completed with 1 local object.
  -remote:
  -remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
  -remote: https://github.com/gyhaan/git-gym/pull/new/ft/bundle-2
  -remote:
  -To https://github.com/gyhaan/git-gym.git
- - [new branch] ft/bundle-2 -> ft/bundle-2
  -branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
  -```
  diff --git a/services.html b/services.html
  index 2ef8a33..bf4ddf9 100644
  --- a/services.html
  +++ b/services.html
  @@ -7,6 +7,6 @@
     </head>
     <body>
       <p>Services</p>
- <p>New Branch</p>

* <p>Origin Branch</p>
     </body>
   </html>
  PS C:\Users\Hp\Desktop\Practice\git-gym> git merge main
  Auto-merging services.html
  CONFLICT (content): Merge conflict in services.html
  Automatic merge failed; fix conflicts and then commit the result.
  PS C:\Users\Hp\Desktop\Practice\git-gym> git merge main
  error: Merging is not possible because you have unmerged files.
  hint: Fix them up in the work tree, and then use 'git add/rm <file>'
  hint: as appropriate to mark resolution and make a commit.
  fatal: Exiting because of an unresolved conflict.
  PS C:\Users\Hp\Desktop\Practice\git-gym> git commit -m 'original branch services page'
  [ft/service-redesign 5893e0c] original branch services page
  PS C:\Users\Hp\Desktop\Practice\git-gym> git push
  fatal: The current branch ft/service-redesign has no upstream branch.
  To push the current branch and set the remote as upstream, use


    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Hp\Desktop\Practice\git-gym> git push origin ft/service-redesign
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 281 bytes | 281.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gyhaan/git-gym.git
7b051d9..5893e0c ft/service-redesign -> ft/service-redesign
PS C:\Users\Hp\Desktop\Practice\git-gym> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Hp\Desktop\Practice\git-gym> git push --set-upstream origin ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
Everything up-to-date
````
