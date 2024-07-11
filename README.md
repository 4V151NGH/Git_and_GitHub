# Git and GitHub

## Git download link: [https://git-scm.com/downloads](https://git-scm.com/downloads)

## Add git configs:
*$ git config --global user.email "your_email@example.com"*

*$ git config --global user.name "Your Name"*

### Check existing git configs:
*$ git config --list*

## SSH setup with GitHub
1. Generate SSH key pair:
   
   *$ ssh-keygen -t ed25519 -C "your_email@example.com"*
   
3. Copy the public key:
   
   *$ clip < ~/.ssh/id_ed25519.pub*
   
5. Go to Github > Settings > SSH and GPG keys.
6. Click "New SSH key" button.
7. Add a "Title" and paste the copied key.
8. Click "Add SSH key and it's all set.

## Initialize git and link to a GitHub repository:
*$ git init*

*$ git remote add origin https://github.com/username/repository_name.git*

## Basic git commands
* *$ git status* - shows the current state of your repository.
  
* "*$ git add .*" **OR** "*$ git add <filename.ext>*" - adds the changes to the staging area.
  
* *$git commit -m "commit message"* - commits the changes to local repostory with a message.
  
* "*$ git log*" **OR** "*$ git log --oneline*" - history of the commits.

* *$ git reflog* - detailed log of the commits.

* *$ git branch* - all braches in the repository.

* *$ git branch new-branch* - create a new branch.

* *$ git checkout new-branch* - switch two another branch. (MAKE SURE TO COMMIT THE CHANGES BEFORE SWITCHING BRANCH)

* *$ git merge new-branch* - run this from "main" branch to merge new-brach to main branch.

* *$ git rebase main* - run this from "new-branch" to change the starting poing to new-brach to the latest commit in main branch.

* *$ git reset <commit-hash>* - jump to a prior commit. (CHANGES MADE AFTER THAT COMMIT WILL BE LOST)

* *$ git push origin main* - This will push all the commits to the main branch of GitHub repository.

* *$ git push -u origin main* - this sets up a upstream remote so you don't have to provide branch name again and again during push/pull.
