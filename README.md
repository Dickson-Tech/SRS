# STEPS TO POST THE LOCAL DJANGO PROJECT TO GITHUB REPOSITORY
Student Registration System

___________________________________________________________
Open your project folder.

Create a virtual environment

Virtual environment isolates our project. Anything we install within the virtual environment does not affect the rest

of the computer and vice-versa.

on cmd: vitualenv . (to install virtual environment)

Activate the virtual environment by running activate.bat files within the scripts folder.
___________________________________________________________________________________________

git status git commands
___________________________________________________________________________________________
1. git init -->
This creates a .git folder on our project folder that means git is initialized.

2. git status -->
This shows all the folders that are not added to git.

3. git add -all -->
This adds all the files to git.

4. git commit -m "commit message" ---> eg: git commit -m "First Commit, Student Registration System"
This commits all folders to git.

5. git log -->
This shows the log of all commits in our repository. This displays most recent commits first.
________________________________________________________________________________________________________________________________
Now we need to push our existing repository. First, we will need to add push our remote origin which is our remote
repository that we created on GitHub. Copy the HTTPs web URL and paste in cmd.

6. git remote add origin weburl

Now, we will need to push our local repository to our remote repository or GitHub account we use.

7. git push -u origin master

In case we get an error 'failed to push some reps to weburl, run below commands

Here are the **full steps to push a new project to GitHub and pull it later**, with common errors and solutions highlighted:

---

## **1. Create a New Repository on GitHub**

1. Log in to [GitHub](https://github.com).
2. Click the "+" icon (top right) → **New repository**.
3. Fill in the repository name, description, and visibility (public/private).
4. **Do not initialize with a README** if you already have local files.
5. Click **Create repository**.

---

## **2. Set Up Your Local Project**

If you already have project files on your computer:

- Open your terminal and navigate to your project directory:
  ```sh
  cd path/to/your/project
  ```

If starting from scratch:

- Create a new folder and enter it:
  ```sh
  mkdir myproject
  cd myproject
  ```

---

## **3. Initialize Git Locally**

```sh
git init
```
This creates a `.git` folder and makes your directory a Git repository.

---

## **4. Add Your Files and Commit**

```sh
git add .
git commit -m "Initial commit"
```

---

## **5. Link Your Local Repository to GitHub**

GitHub will display a remote URL (after repo creation). It looks like:
- HTTPS: `https://github.com/YourUsername/your-repo.git`
- SSH: `git@github.com:YourUsername/your-repo.git`

Add the remote:
```sh
git remote add origin https://github.com/YourUsername/your-repo.git
```

---

## **6. Push Your Code to GitHub**

```sh
git push -u origin main
```
- If your branch is called `master`, use `master` instead of `main`.

---

### **Common Errors and Solutions**

#### **A. Authentication Failed**

**Error:**  
`remote: Authentication failed for 'https://github.com/YourUsername/your-repo.git'`

**Solution:**  
- Make sure you are logged in.  
- For HTTPS: Use a [personal access token](https://github.com/settings/tokens) instead of your password.
- For SSH: Ensure your SSH key is added to GitHub (`ssh-add ~/.ssh/id_rsa`).

#### **B. Remote Already Exists**

**Error:**  
`fatal: remote origin already exists.`

**Solution:**  
Remove the existing remote and re-add:
```sh
git remote remove origin
git remote add origin <url>
```

#### **C. Branch Name Mismatch**

**Error:**  
`error: src refspec main does not match any`

**Solution:**  
- Check your branch name (`git branch`).  
- Use the correct branch in your push command.

#### **D. Non-Fast-Forward Updates**

**Error:**  
`! [rejected] main -> main (non-fast-forward)`

**Solution:**  
- Someone pushed changes before you.
- Pull first: `git pull origin main`  
- Resolve any merge conflicts.
- Then push again.

#### **E. Permission Denied (SSH)**

**Error:**  
`Permission denied (publickey)`

**Solution:**  
- Add your SSH key to your GitHub account.
- Start the ssh-agent and add your key.

---

## **7. Clone/Pull the Repository Later**

To get the project on another machine or folder:

**Clone the repo:**
```sh
git clone https://github.com/YourUsername/your-repo.git
```

**To update your local repo with remote changes:**
```sh
git pull origin main
```

---

### **Common Errors When Pulling**

#### **A. Merge Conflicts**

**Error:**  
`CONFLICT (content): Merge conflict in filename.ext`

**Solution:**  
- Open the conflicted file(s), look for `<<<<<<<`, `=======`, and `>>>>>>>`.
- Edit and resolve the conflict.
- Add and commit:
  ```sh
  git add filename.ext
  git commit -m "Resolved merge conflict"
  ```

#### **B. Authentication Issues**

Same as pushing—ensure your credentials are correct and up-to-date.

---

## **Summary Table**

| Step                        | Command/Action                                    | Common Error                       | Solution                                |
|-----------------------------|---------------------------------------------------|-------------------------------------|------------------------------------------|
| Create GitHub repo          | On GitHub website                                 | N/A                                 | N/A                                      |
| Initialize locally          | `git init`                                        | N/A                                 | N/A                                      |
| Add files & commit          | `git add .` `git commit -m "msg"`                 | N/A                                 | N/A                                      |
| Add remote                  | `git remote add origin <url>`                     | Remote exists                       | Remove and re-add remote                 |
| Push                        | `git push -u origin main`                         | Auth failed, branch mismatch, etc.  | See errors above                         |
| Clone repo                  | `git clone <url>`                                 | Auth failed                         | Use correct credentials                  |
| Pull                        | `git pull origin main`                            | Merge conflict, auth failed         | Resolve conflicts, check credentials     |

---

**Tip:**  
If you ever get stuck, use `git status` to see what’s going on, and search error messages for solutions.
Use this command: *git pull --rebase origin master*

or Use this: *git push origin master*
________________________________________________________________________________________________________________________________
Now we can see your project on your GitHub repository.

