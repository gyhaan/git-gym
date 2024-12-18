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
error: unknown switch `e
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
error: unknown switch `e
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

## Bundle 3

### Exercise 1

```bash
Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/team-page)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git switch ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/team-page)
$ git log
commit 46d53bc53176298d2c469074187ec75fb4af41e7 (HEAD -> ft/team-page, origin/ft/team-page)
Author: gyhaan <g.yhaan@alustudent.com>
Date:   Wed Dec 18 10:51:09 2024 +0200

    team page

commit a96a8ee357dec520f849f8ce34187079e47415e1 (origin/main, main, ft/contact-page)
Author: gyhaan <g.yhaan@alustudent.com>
Date:   Wed Dec 18 10:36:24 2024 +0200

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/team-page)
$ git switch ft/contact-page
Switched to branch 'ft/contact-page'

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git cherry-pick 46d53bc53176298d2c469074187ec75fb4af41e7
[ft/contact-page a9e312a] team page
 Date: Wed Dec 18 10:51:09 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git add .

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git commit -m 'contact page'
[ft/contact-page 033dac1] contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 667 bytes | 166.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/gyhaan/git-gym/pull/new/ft/contact-page
remote:
To https://github.com/gyhaan/git-gym.git
 * [new branch]      ft/contact-page -> ft/contact-page

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git branch ft/contact-page ft/faq-page
fatal: a branch named 'ft/contact-page' already exists

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git branch ft/faq-page ft/contact-page

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/contact-page)
$ git switch ft/faq-page
Switched to branch 'ft/faq-page'

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/faq-page)
$ git add .

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/faq-page)
$ git commit -m 'faq page'
[ft/faq-page 77a8c39] faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 421 bytes | 140.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/gyhaan/git-gym/pull/new/ft/faq-page
remote:
To https://github.com/gyhaan/git-gym.git
 * [new branch]      ft/faq-page -> ft/faq-page

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/faq-page)
$ git switch ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/team-page)
$ git revert 46d53bc53176298d2c469074187ec75fb4af41e7
[ft/team-page 413078d] Revert "team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/team-page)
$ git add .

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/team-page)
$ git commit -m 'team page revert'
On branch ft/team-page
Your branch is ahead of 'origin/ft/team-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/team-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 244 bytes | 244.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gyhaan/git-gym.git
   46d53bc..413078d  ft/team-page -> ft/team-page
```

### Exercise 2

```bash

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git branch ft/home-page-redesign ft/faq-page

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git switch ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git add .

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git commit -m 'after rebase'
[ft/home-page-redesign d2b5065] after rebase
 1 file changed, 1 insertion(+)

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 1.25 KiB | 213.00 KiB/s, done.
Total 12 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/gyhaan/git-gym/pull/new/ft/home-page-redesign
remote:
To https://github.com/gyhaan/git-gym.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
```

## Bundle 4

### Exercise 1

```bash
Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git branch ft/home-page-redesign ft/faq-page

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git switch ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git add .

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git commit -m 'after rebase'
[ft/home-page-redesign d2b5065] after rebase
 1 file changed, 1 insertion(+)

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 1.25 KiB | 213.00 KiB/s, done.
Total 12 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/gyhaan/git-gym/pull/new/ft/home-page-redesign
remote:
To https://github.com/gyhaan/git-gym.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (ft/home-page-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git remote add git-copy https://github.com/gyhaan/git-gym-2.git

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git remote -v
git-copy        https://github.com/gyhaan/git-gym-2.git (fetch)
git-copy        https://github.com/gyhaan/git-gym-2.git (push)
origin  https://github.com/gyhaan/git-gym.git (fetch)
origin  https://github.com/gyhaan/git-gym.git (push)

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git add .

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git commit -m 'Other Repo'
[main c4f4e52] Other Repo
 1 file changed, 1 insertion(+)

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 306 bytes | 306.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/gyhaan/git-gym.git
   60c9a46..c4f4e52  main -> main

Hp@OWGA MINGW64 ~/Desktop/Practice/git-gym (main)
$ git push git-copy main
Enumerating objects: 35, done.
Counting objects: 100% (35/35), done.
Delta compression using up to 8 threads
Compressing objects: 100% (33/33), done.
Writing objects: 100% (35/35), 6.90 KiB | 1009.00 KiB/s, done.
Total 35 (delta 17), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (17/17), done.
To https://github.com/gyhaan/git-gym-2.git
 * [new branch]      main -> main
```

### Exercise 2
