# SRS
Student Registration System

___________________________________________________________
Open your project folder.

Create a virtual environment

Virtual environment isolates our project. Anything we install within the virtual environment does not affect the rest

of the computer and vice-versa.

on cmd: vitualenv . (to install virtual environment)

Activate the virtual environment by running activate.bat files within the scripts folder.

git status git commands
git init
This creates a .git folder on our project folder that means git is initialized.

git status
This shows all the folders that are not added to git.

git add -all
This adds all the files to git.

git commit -m "commit message"
This commits all folders to git.

git log
This shows the log of all commits in our repository. This displays most recent commits first.

Now we need to push our existing repository. First, we will need to add push our remote origin which is our remote
repository that we created on GitHub. Copy the HTTPs web URL and paste in cmd.

git remote add origin weburl

Now, we will need to push our local repository to our remote repository or GitHub account we use.

git push -u origin master

In case we get an error 'failed to push some reps to weburl, run below commands

git pull --rebase origin master

git push origin master

Now we can see your project on your GitHub repository.

