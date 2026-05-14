# Bundle 3

## Exercise 1:

```bash
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 3 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
Updating b3fa951..d1bdf2c
Fast-forward
 services.html | Bin 72 -> 70 bytes
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Our Team</h1>" > team.html
PS C:\Users\elvis\Desktop\Git Learning> git add team.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Add team page"
[ft/team-page 4b278c4] Add team page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 team.html
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/ft/team-page
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\elvis\Desktop\Git Learning> ^C
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\elvis\Desktop\Git Learning> git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
PS C:\Users\elvis\Desktop\Git Learning> git log --oneline
4b278c4 (HEAD -> ft/team-page, origin/ft/team-page) Add team page
d1bdf2c (origin/main, origin/HEAD, main, ft/contact-page) Merge pull request #3 from Manzi-Elvis/ft/service-redesign
2d21b61 Resolve services page merge conflict
b3fa951 Update services page on main
6bfdc4a Redesign services page
1c45581 Bundle 2: Exercise 1
c4dd3bf Merge pull request #2 from Manzi-Elvis/dev
5171f19 Merge pull request #1 from Manzi-Elvis/ft/bundle-2
59f6fee (origin/ft/bundle-2, ft/bundle-2) Add services page
053a887 (origin/dev, dev) Exercise 2
044374e Add home and about pages
777de25 ...
51ba6ac Exercise 1
PS C:\Users\elvis\Desktop\Git Learning> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\elvis\Desktop\Git Learning> git cherry-pick 4b278c4
[ft/contact-page 44b8c13] Add team page
 Date: Thu May 14 14:49:49 2026 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 team.html
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Contact Us</h1>" > contact.html
PS C:\Users\elvis\Desktop\Git Learning> git add contact.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Add contact page"
[ft/contact-page 3d3e7cc] Add contact page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 contact.html
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 613 bytes | 32.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/ft/contact-page
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Frequently Asked Questions</h1>" > faq.html
PS C:\Users\elvis\Desktop\Git Learning> git add faq.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Add FAQ page"
[ft/faq-page 575cf0f] Add FAQ page
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 faq.html
PS C:\Users\elvis\Desktop\Git Learning> git revert 4b278c4
fatal: cannot lock ref 'HEAD': is at e60fa18ecf5c19a630608347afeac7e326444e03 but expected 575cf0f1a1c68c235aa1b0c8686bc441ae636c21
PS C:\Users\elvis\Desktop\Git Learning> git status
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

nothing to commit, working tree clean
PS C:\Users\elvis\Desktop\Git Learning> git revert 4b278c4
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

nothing to commit, working tree clean
PS C:\Users\elvis\Desktop\Git Learning> dir


    Directory: C:\Users\elvis\Desktop\Git Learning


Mode                 LastWriteTime         Length Name                                                             
----                 -------------         ------ ----                                                             
-a----         5/14/2026   2:09 PM             44 about.html                                                       
-a----         5/14/2026   2:53 PM             44 contact.html                                                     
-a----         5/14/2026   2:55 PM             76 faq.html                                                         
-a----         5/14/2026   2:09 PM            227 home.html                                                        
-a----         5/14/2026   2:48 PM          10169 README.md                                                        
-a----         5/14/2026   2:49 PM             70 services.html                                                    


PS C:\Users\elvis\Desktop\Git Learning> git push origin ft/faq-page
Everything up-to-date
PS C:\Users\elvis\Desktop\Git Learning> 
```


## Exercise 2:

```bash
PS C:\Users\elvis\Desktop\Git Learning> git checkout ft/faq-page
Already on 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.
PS C:\Users\elvis\Desktop\Git Learning> git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
PS C:\Users\elvis\Desktop\Git Learning> git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 8 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
PS C:\Users\elvis\Desktop\Git Learning> git pull origin main
From https://github.com/Manzi-Elvis/Git
 * branch            main       -> FETCH_HEAD
Updating d1bdf2c..f010d61
Fast-forward
 contact.html | Bin 0 -> 44 bytes
 faq.html     | Bin 0 -> 76 bytes
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 contact.html
 create mode 100644 faq.html
PS C:\Users\elvis\Desktop\Git Learning> echo "<p>Main branch update</p>" >> index.html
PS C:\Users\elvis\Desktop\Git Learning> git add index.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Update main page content"
[main bed9dd2] Update main page content
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html
PS C:\Users\elvis\Desktop\Git Learning> git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 344 bytes | 49.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Manzi-Elvis/Git.git
   f010d61..bed9dd2  main -> main
PS C:\Users\elvis\Desktop\Git Learning> git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
PS C:\Users\elvis\Desktop\Git Learning> git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
PS C:\Users\elvis\Desktop\Git Learning> echo "<h1>Redesigned Home Page</h1>" > home.html
PS C:\Users\elvis\Desktop\Git Learning> git add home.html
PS C:\Users\elvis\Desktop\Git Learning> git commit -m "Redesign home page"
[ft/home-page-redesign 627b35a] Redesign home page
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\elvis\Desktop\Git Learning> git push -u origin ft/home-page-redesign
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 12 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (11/11), 2.44 KiB | 415.00 KiB/s, done.
Total 11 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/Manzi-Elvis/Git/pull/new/ft/home-page-redesign
remote: 
To https://github.com/Manzi-Elvis/Git.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
PS C:\Users\elvis\Desktop\Git Learning>
```