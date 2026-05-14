# Bundle 5
## Exercise 1:

### Steps:
1. Go to your repository on GitHub
2. Open your repository
3. Click: Settings
4. On the left sidebar click: Pages
5. Under: Build and deployment
6. set: Source → Deploy from a branch
7. Select: Branch → main Folder → /(root)
8. Click: Save

Wait about 1–3 minutes.
GitHub will generate a public link like:
https://manzi-elvis.github.io/Git/

Open the link in:

- another browser
- incognito mode
- or share it with someone

If it opens publicly without login, then GitHub Pages is enabled successfully.

## Exercise 2:

### Steps I Followed

#### 1. Forked the Repository

I forked the original project repository from TheGymRwanda:

```txt
https://github.com/TheGymRwanda/git-cafe-exercise
```

This created my own copy of the project on GitHub.

---

#### 2. Cloned My Fork Locally

I cloned my forked repository to my local machine using:

```bash
git clone https://github.com/Manzi-Elvis/git-cafe-exercise.git
```

Then I moved into the project folder:

```bash
cd git-cafe-exercise
```

---

#### 3. Edited the Project

I opened the project in VS Code:

```bash
code .
```

Inside the `index.html` file, I changed:

```html
Welcome to our place
```

to:

```html
Welcome to our restaurant
```

---

#### 4. Staged and Committed the Changes

I staged the modified file:

```bash
git add index.html
```

Then committed the changes:

```bash
git commit -m "Update welcome text"
```

---

#### 5. Pushed the Changes to GitHub

I pushed my changes to my forked repository:

```bash
git push origin main
```

---

#### 6. Created a Pull Request

Finally, I opened a Pull Request from my fork to the original repository.

#### PR Configuration

```txt
Base Repository:
TheGymRwanda/git-cafe-exercise

Head Repository:
Manzi-Elvis/git-cafe-exercise
```

This allowed my contribution to be reviewed and potentially merged into the original project.

---

#### Skills Practiced

- Forking repositories
- Cloning repositories
- Editing project files
- Git staging and committing
- Pushing changes to GitHub
- Creating Pull Requests
- Open source contribution workflow

---

#### Outcome

Successfully contributed to an external GitHub repository using the standard open-source contribution workflow.