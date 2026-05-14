# Bundle 6 

## Exercise 1

### Objective

Make a new feature branch, add a new `Menu` page to the `git-cafe-exercise` project, and submit the changes through a Pull Request.

---

### Steps Followed

#### 1. Created a Feature Branch

```bash
git checkout -b ft/menu-page
```

---

#### 2. Added the Menu Page

Created a new file:

```txt
menu.html
```

Added content related to the restaurant menu.

---

#### 3. Staged and Committed Changes

```bash
git add menu.html
git commit -m "Add menu page"
```

---

#### 4. Pushed Changes to GitHub

```bash
git push -u origin ft/menu-page
```

---

#### 5. Created a Pull Request

Opened a Pull Request from:

```txt
ft/menu-page → main
```

and requested review.

---

#### Skills Practiced

- Feature branch workflow
- Git commits
- Pushing branches
- Pull Requests
- GitHub collaboration workflow

## Exercise 2:

```bash
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git checkout -b fix/contact-title
Switched to a new branch 'fix/contact-title'
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> 
                                                        git add index-4.html             
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git commit -m "Fix contact page title"
[fix/contact-title 6a4206b] Fix contact page title
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> ^C
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git push -u origin fix/contact-title
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 327 bytes | 327.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'fix/contact-title' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/git-cafe-exercise/pull/new/fix/contact-title
remote: 
To https://github.com/Manzi-Elvis/git-cafe-exercise.git
 * [new branch]      fix/contact-title -> fix/contact-title
branch 'fix/contact-title' set up to track 'origin/fix/contact-title'.
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> 
```
Next:  Make a Pull Request On GitHub:
```
base: main
compare: fix/contact-title
```

Then: Request review
Add a reviewer to the PR.


## Exercise 3:
```bash
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git checkout -b fix/contact-title
Switched to a new branch 'fix/contact-title'
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git add index-4.html             
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git commit -m "Fix contact page title"
[fix/contact-title 6a4206b] Fix contact page title
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> ^C
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git push -u origin fix/contact-title
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 327 bytes | 327.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'fix/contact-title' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/git-cafe-exercise/pull/new/fix/contact-title
remote: 
To https://github.com/Manzi-Elvis/git-cafe-exercise.git
 * [new branch]      fix/contact-title -> fix/contact-title
branch 'fix/contact-title' set up to track 'origin/fix/contact-title'.
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> 
 *  History restored 

PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git checkout fix/contact-title
Already on 'fix/contact-title'
Your branch is up to date with 'origin/fix/contact-title'.
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git add index-4.html
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git commit -m "Fix contact telephone number"
[fix/contact-title 1594c3a] Fix contact telephone number
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 329.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Manzi-Elvis/git-cafe-exercise.git
   6a4206b..1594c3a  fix/contact-title -> fix/contact-title
PS C:\Users\elvis\Documents\PROJECTS\git-cafe-exercise> 
```
## Exercise 4:

### Objective - PR Review Exercise

Review Pull Requests from peers, request changes, approve the updated work, and merge the PRs.

---

### Steps I Followed

#### 1. Accessed Peer Pull Requests

Received access/review permissions to peer repositories and opened their Pull Requests on GitHub.

---

#### 2. Reviewed the Code

Checked the modified files and analyzed the changes made in the PRs.

---

#### 3. Requested Changes

Used the GitHub review system to request improvements and suggest corrections where necessary.

---

#### 4. Re-Reviewed Updated Changes

After the requested changes were applied, I reviewed the updated code again to confirm everything was correct.

---

#### 5. Approved and Merged the PRs

Approved the Pull Requests and merged them into the main branch.

---

#### Skills Practiced

- Pull Request reviews
- Team collaboration workflow
- Requesting code changes
- PR approval process
- Merge workflow on GitHub
