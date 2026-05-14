# Bundle 4:

## Exercise 1:

```bash
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
remote: Enumerating objects: 56, done.
remote: Counting objects: 100% (55/55), done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 51 (delta 25), reused 42 (delta 18), pack-reused 0 (from 0)
Unpacking objects: 100% (51/51), 12.67 KiB | 56.00 KiB/s, done.
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
   8c250c4..9fdcf7d  main       -> origin/main
Updating bed9dd2..9fdcf7d
Fast-forward
 Exercises.md         | 186 ++++++++++++++++++++++++
 README.md            | 395 +++++++++++++++++++--------------------------------
 Solutions/Bundle1.md | 180 +++++++++++++++++++++++
 Solutions/Bundle2.md | 180 +++++++++++++++++++++++
 Solutions/Bundle3.md | 134 +++++++++++++++++
 Solutions/Bundle4.md |   0
 Solutions/Bundle5.md |   0
 Solutions/Bundle6.md |   0
 home.html            | Bin 217 -> 64 bytes
 9 files changed, 829 insertions(+), 246 deletions(-)
 create mode 100644 Exercises.md
 create mode 100644 Solutions/Bundle1.md
 create mode 100644 Solutions/Bundle2.md
 create mode 100644 Solutions/Bundle3.md
 create mode 100644 Solutions/Bundle4.md
 create mode 100644 Solutions/Bundle5.md
 create mode 100644 Solutions/Bundle6.md
PS C:\Users\elvis\Desktop\Git Learning> 
 *  History restored 

PS C:\Users\elvis\Desktop\Git Learning> git remote add git-copy https://github.com/Manzi-Elvis/Git-Copy.git
PS C:\Users\elvis\Desktop\Git Learning> git remote -v
git-copy        https://github.com/Manzi-Elvis/Git-Copy.git (fetch)
git-copy        https://github.com/Manzi-Elvis/Git-Copy.git (push)
origin  https://github.com/Manzi-Elvis/Git.git (fetch)
origin  https://github.com/Manzi-Elvis/Git.git (push)
PS C:\Users\elvis\Desktop\Git Learning> echo "<p>Updated Home Page</p>" >> home.html
PS C:\Users\elvis\Desktop\Git Learning> git add home.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Update home page"
[main 32b1cdc] Update home page
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 350 bytes | 87.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Manzi-Elvis/Git.git
   9fdcf7d..32b1cdc  main -> main
PS C:\Users\elvis\Desktop\Git Learning> git push git-copy main
Enumerating objects: 119, done.
Counting objects: 100% (119/119), done.
Delta compression using up to 12 threads
Compressing objects: 100% (109/109), done.
Writing objects: 100% (119/119), 25.13 KiB | 384.00 KiB/s, done.
Total 119 (delta 46), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (46/46), done.
To https://github.com/Manzi-Elvis/Git-Copy.git
 * [new branch]      main -> main
PS C:\Users\elvis\Desktop\Git Learning>
```

## Exercise 2: 

```bash
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
>> 
M       Solutions/Bundle4.md
Already on 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/footer
Switched to a new branch 'ft/footer'
PS C:\Users\elvis\Desktop\Git Learning> echo "<footer>Footer version 1</footer>" >> index.html
PS C:\Users\elvis\Desktop\Git Learning> git add index.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Add footer"
[ft/footer b73d1f4] Add footer
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> echo "<p>Footer links added</p>" >> index.html
PS C:\Users\elvis\Desktop\Git Learning> git add index.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Add footer links"
[ft/footer 8b656ac] Add footer links
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin ft/footer
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 641 bytes | 213.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/ft/footer
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
M       Solutions/Bundle4.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
PS C:\Users\elvis\Desktop\Git Learning> git merge --squash ft/footer
Updating d0187c3..8b656ac
Fast-forward
Squash commit -- not updating HEAD
 index.html | Bin 56 -> 180 bytes
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Solutions/Bundle4.md

PS C:\Users\elvis\Desktop\Git Learning> git commit -m "footer changes squashing"
[ft/squashing 5744fb9] footer changes squashing
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin ft/squashing
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 391 bytes | 391.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/ft/squashing
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
PS C:\Users\elvis\Desktop\Git Learning>
```