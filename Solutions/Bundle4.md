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