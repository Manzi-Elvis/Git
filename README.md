# Git Exercises

## Exercise 1: 

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