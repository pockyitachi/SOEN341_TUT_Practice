# GitHub Team Collaboration Tutorial

Welcome to our GitHub collaboration exercise!  
In this tutorial, you will learn how to work together on a shared repository using branches, pull requests, issues, and project boards.

---

## 🎯 Learning Goals
By the end of this session, you should be able to:
- Clone a GitHub repository
- Create and work on your own branch
- Make changes and push them to GitHub
- Open and review pull requests
- Resolve simple merge conflicts
- Use Issues and Project Boards to manage teamwork
- Understand the purpose of branch protection rules

---

## 🗂 Step-by-Step Activities

### 1. Setup
1. Accept your invitation to join this repository.
2. Clone the repo to your computer:
   ```
   git clone https://github.com/<org-or-username>/<repo-name>.git
   cd <repo-name>
   ```
3. Configure your name and email (if not set):
   ```
   git config user.name "Your Name"
   git config user.email "you@example.com"
   ```

---

### 2. Add Yourself to Contributors
1. Create a new branch with your name:
   ```
   git checkout -b add-yourname
   ```
2. Open the file **`contributors.md`** and add your name at the bottom of the list.
3. Save your changes, then commit and push:
   ```
   git add contributors.md
   git commit -m "Add <Your Name> to contributors"
   git push origin add-yourname
   ```

---

### 3. Open a Pull Request (PR)
1. Go to the repository on GitHub in your browser.
2. You will see a suggestion to **Compare & Pull Request** for your branch — click it.
3. Fill in the PR form:
   - **Title**: `Add <Your Name> to contributors`
   - **Description**: Briefly describe your change.
4. Assign a teammate as a **Reviewer** (right side of the PR page).
5. Submit the Pull Request.

---

### 4. Review and Merge a Pull Request
1. Open a teammate’s Pull Request.
2. Click **Files changed** and review their edits.
3. Leave at least one comment.
4. Click **Review changes → Approve** when satisfied.
5. Once approved, click **Merge pull request → Confirm merge**.
6. Delete the branch after merge (optional but recommended).

---

### 5. Work with Issues
1. Go to the **Issues** tab → click **New Issue**.
2. Give it a descriptive title (e.g., *Add About Page*).
3. Write a short description of the task.
4. Assign the Issue to yourself or a teammate.
5. (Optional) Link your Issue to your Pull Request (right sidebar → **Linked issues**).

---

### 6. Use the Project Board
1. Go to the **Projects** tab and open the class project board.
2. Find your Issue card and move it across the workflow:
   - **To Do** → **In Progress** → **Done**.
3. This simulates real agile teamwork.

---

### 7. Branch Protection Rules (Instructor Demo)
The `main` branch is protected:
- No direct pushes allowed.
- All changes must go through Pull Requests.

**Test it:**
1. Try pushing directly to `main`:
   ```
   git checkout main
   echo "test" >> test.txt
   git add test.txt
   git commit -m "Test push to main"
   git push origin main
   ```
2. GitHub should block the push with a message. ✅

---

### 8. Merge Conflict Resolution (Advanced)
Sometimes two people edit the same line, causing a **merge conflict**.  
To resolve:
1. Update your local `main` branch:
   ```
   git checkout main
   git pull origin main
   ```
2. Merge `main` into your branch:
   ```
   git checkout add-yourname
   git merge main
   ```
   or
   ```
   git pull origin main
   ```
3. Git will show a conflict in `contributors.md`.  
   Open the file, keep both names, and remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
4. Mark as resolved:

   ```
   git add contributors.md
   git commit -m "Resolve merge conflict"
   git push origin add-yourname
   ```
5. Your PR can now be merged.

---

## ✅ Wrap-Up
You now know how to:
- Use branches for independent work
- Submit and review code via Pull Requests
- Track tasks with Issues and Projects
- Protect important branches
- Handle merge conflicts

Collaboration in GitHub is about communication as much as code. 🚀
