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
