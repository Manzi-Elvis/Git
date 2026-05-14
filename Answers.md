# Git Exercises


## Bundle 1

### Exercise 1: 

```bash
PS C:\Users\elvis\Desktop\Git Learning> git init
Initialized empty Git repository in C:/Users/elvis/Desktop/Git Learning/.git/
PS C:\Users\elvis\Desktop\Git Learning> git add .
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "first commit"
[master (root-commit) 8ce82d6] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html
PS C:\Users\elvis\Desktop\Git Learning> git branch -M main
PS C:\Users\elvis\Desktop\Git Learning> git remote add origin https://github.com/Manzi-Elvis/Git.git
>> git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 233 bytes | 58.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> git branch -m main master
PS C:\Users\elvis\Desktop\Git Learning> git branch
* master

PS C:\Users\elvis\Desktop\Git Learning> git push -u origin master
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/master
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\elvis\Desktop\Git Learning> git branch -m master main
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin main
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Manzi-Elvis/Git.git
   8ce82d6..a6c47a0  main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout dev    
M       README.md
Switched to branch 'dev'
PS C:\Users\elvis\Desktop\Git Learning> git branch -d test
Deleted branch test (was a6c47a0).
PS C:\Users\elvis\Desktop\Git Learning> git branch
* dev
  main
```


## Exercise 2:
```bash
PS C:\Users\elvis\Desktop\Git Learning> git checkout dev
M       README.md
Already on 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\elvis\Desktop\Git Learning> git stash push -m "add home page"
Saved working directory and index state On dev: add home page
PS C:\Users\elvis\Desktop\Git Learning> ^C
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>About Page</h1>" > about.html
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\elvis\Desktop\Git Learning> git stash push -m "add about page"     
No local changes to save
PS C:\Users\elvis\Desktop\Git Learning> git stash push -m "add about page"
No local changes to save
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Team Page</h1>" > team.html  
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\elvis\Desktop\Git Learning> git stash push -m "add team page"
No local changes to save
PS C:\Users\elvis\Desktop\Git Learning> git stash list
stash@{0}: On dev: add home page
PS C:\Users\elvis\Desktop\Git Learning> git stash -u
Saved working directory and index state WIP on dev: 777de25 ...
PS C:\Users\elvis\Desktop\Git Learning> git stash list
stash@{0}: WIP on dev: 777de25 ...
stash@{1}: On dev: add home page
PS C:\Users\elvis\Desktop\Git Learning> git stash --include-untracked
No local changes to save
PS C:\Users\elvis\Desktop\Git Learning> git stash list               
stash@{0}: WIP on dev: 777de25 ...
stash@{1}: On dev: add home page
PS C:\Users\elvis\Desktop\Git Learning> git stash push -u -m "about and team pages"
No local changes to save
PS C:\Users\elvis\Desktop\Git Learning> git stash list
stash@{0}: WIP on dev: 777de25 ...
stash@{1}: On dev: add home page
PS C:\Users\elvis\Desktop\Git Learning> git stash pop stash@{0}
error: unknown switch `e`
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\elvis\Desktop\Git Learning> git stash pop "stash@{0}"
Already up to date.
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (ff62bcd3b30415e531ffe3dbb2705b44a9f71352)
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\elvis\Desktop\Git Learning> git add about.html home.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Add home and about pages"
[dev 044374e] Add home and about pages
 2 files changed, 11 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\elvis\Desktop\Git Learning> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 540 bytes | 180.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Manzi-Elvis/Git.git
   777de25..044374e  dev -> dev
PS C:\Users\elvis\Desktop\Git Learning> git clean -f team.html
Removing team.html
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
PS C:\Users\elvis\Desktop\Git Learning> 
```


## Bundle 2:

### Exercise 1:

```bash
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Services Page</h1>" > services.html
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\elvis\Desktop\Git Learning> git add services.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Add services page"
[ft/bundle-2 59f6fee] Add services page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 services.html
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 377.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/ft/bundle-2
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1.83 KiB | 98.00 KiB/s, done.
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
   a6c47a0..c4dd3bf  main       -> origin/main
Updating a6c47a0..c4dd3bf
Fast-forward
 README.md     | 144 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 about.html    | Bin 0 -> 44 bytes
 home.html     |  11 +++++
 index.html    |   0
 services.html | Bin 0 -> 50 bytes
 5 files changed, 154 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html
 delete mode 100644 index.html
 create mode 100644 services.html
PS C:\Users\elvis\Desktop\Git Learning>
```

### Exercise 2:

```bash
PS C:\Users\elvis\Desktop\Git Learning> ^C
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
M       README.md
Already on 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Our Redesigned Services</h1>" > services.html
>> 
PS C:\Users\elvis\Desktop\Git Learning> git add services.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Redesign services page"
[ft/service-redesign 6bfdc4a] Redesign services page
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 338 bytes | 338.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/ft/service-redesign
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
M       README.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Our Main Branch Services</h1>" > services.html
PS C:\Users\elvis\Desktop\Git Learning> git add services.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Update services page on main"
[main b3fa951] Update services page on main
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 348 bytes | 87.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Manzi-Elvis/Git.git
   1c45581..b3fa951  main -> main
PS C:\Users\elvis\Desktop\Git Learning> git checkout ft/service-redesign
M       README.md
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
PS C:\Users\elvis\Desktop\Git Learning> git diff main
diff --git a/README.md b/README.md
index 2837484..07d9354 100644
--- a/README.md
+++ b/README.md
@@ -258,4 +258,10 @@ Fast-forward
  delete mode 100644 index.html
  create mode 100644 services.html
 PS C:\Users\elvis\Desktop\Git Learning>
+```
+
+### Exercise 2:
+
+```bash
+
 
\ No newline at end of file
diff --git a/services.html b/services.html
index 7d0414f..ef4ef07 100644
Binary files a/services.html and b/services.html differ
set mark: ...skipping...
diff --git a/README.md b/README.md
index 2837484..07d9354 100644
--- a/README.md
+++ b/README.md
@@ -258,4 +258,10 @@ Fast-forward
  delete mode 100644 index.html
  create mode 100644 services.html
PS C:\Users\elvis\Desktop\Git Learning> git merge main
warning: Cannot merge binary files: services.html (HEAD vs. main)
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\elvis\Desktop\Git Learning> git add services.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Resolve services page merge conflict"
>> 
[ft/service-redesign 2d21b61] Resolve services page merge conflict
PS C:\Users\elvis\Desktop\Git Learning> git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 253 bytes | 253.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Manzi-Elvis/Git.git
   6bfdc4a..2d21b61  ft/service-redesign -> ft/service-redesign
```

