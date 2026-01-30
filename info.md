- Git : Distributed Version Control System (Free open source).
- Other Systems Like  :  [Github - Gitlab - Bitbucket].
- Github - Gitlab - Bitbucket : are simplify using of Git.
- we can use Git without Github or Gitlab Or Bitbucket.
- Git has its own GUI but in our course we will use CMD.
-------------------------------------------
- What are benefits of using Git ?
- all team can work in the same project
- easy to fix issues
- easy to create new features
- easy to solve conflicts
-------------------------------------------
- what is the Repository (Repo): every project has its own repository containing its source code.
- Clone: can be from local or remote repositories.
- Branch : is the branch (الفرع) of the Repo .
- Local Repository : at your machine.
- Remote Repository : is the remote repository (server).
- Commit : is to make check point in Your Local Repository.
- pull: get the updates from Repo to Your local.
- push: add the updates from local to Your Repo.
- Pull Request (PR): Tell other team members to pull my changes.
- Merge the Request : accept and put your code after review into the Remote Repository 
-------------------------------------------
- sign up: https://github.com/signup

- download Git cmd: https://git-scm.com/downloads
-------------------------------------------
- after signing up create your new repository from the website.
- creating Read-me file
- creating new directory (Folder) at your local: mkdir folder-name 
- then clone Repo to your local :  git clone https://github.com/repo-name 
-------------------------------------------
- after finishing your code ... check this image : life-cycle.jpeg
- git branch ---> get the branch name
- git status
- git add file-name file-name file-name (OR use) git add * // Now files were added to the staging
- if we need to un staging any files : git reset head file-name
- git commit -m "your commit message goes here"
- git push origin to the master ===> branch or any branch
-------------------------------------------
- git pull origin master => to git the latest updates from the master branch
-------------------------------------------
- How to show git configuration: 
- git config -l ===> this will show all git configurations.
- git config --global user.email ===> this gets the email
- git config --global user.email = "test@gmail.com" ===> this sets the email
- Now you can edit the configuration from your editor : - git config --global --edit  
-------------------------------------------
- How to create a new from existing project?
- create new Repo from github.
- git init 
- then after finishing your project code make "git status"
- git add *
- git commit -m "your commit message goes here"
- git remote add origin git://github.com-repoFolder
- git push -u origin master
-------------------------------------------
- create new pull request: this will be with another account for students at the course.
-------------------------------------------
- How to create aliases names for Git cmds ?
- git config --global alias.sta status
- and then try =>> git st =>> it will work as git status.
-------------------------------------------
- How to creating new Branches ?
- git branch ===> this will show us the current branch name like "master"
- git checkout -b new-branch-name OR git branch new-branch-name =>> this will be from master branch .
 
- to delete (safe delete) the branch => git branch -d new-branch-name

- to delete (Force delete) the branch => git branch -D new-branch-name

- git branch -m new-branch-name-two =>> rename the branch
-------------------------------------------
- How to do Stash ?
- make your files normally then make ==> git add . 
- git stash
- then git status 
- try to make new files then push them to master this will work normally .

- after that we need to get the stashed file from the stash : git stash list =>> this will show us all stashes

- if you need to add name to stash ==> git stash save "stash message goes here"

- git stash pop =>> this will get the stash from the list as original copy

- git stash apply =>>  this will get the stash from the list as a new copy

- if we need to get specific stash =>> git stash pop stash@{1 or 2 ...}

- git stash drop stash@{1 or 2 ...}

-finally  git commit -m "your commit message goes here" the push to origin master
-
-------------------------------------------
- How to restore & clean files the Files ?
- make file then add it 
- to restore it on stage =>> git restore --staged file-name

- to clean files: git clean -n
- then git clean -f
-------------------------------------------
- How to reset ?
- add two files one.js & two.js
- then commit  then push
- git log => will show you all logged head with hash code.
- git reset --hard e3837y363uj83yh4egej
- git push origin master --force
-
-------------------------------------------
- How to ignore files or folders in git ?
- first create file with this name =>>> .gitignore
-------------------------------------------
- Tag and Release ?
- make file then add them
- git tag
- git tag v1.0
- git push origin v1.0
 
- make file then add them
- git tag
- git tag v2.0
- if you need to remove tag =>> git tag -a v2.0 -m "this is custom tag two" 
- git push origin v2.0

-------------------------------------------
- adding invitation to your team members.
-------------------------------------------
-- How to create your public key ?
- ssh-keygen -t rsa -b 4096 -C "test@gmail.com"   

شرح 
'ssh-keygen': This is the command to generate, manage, and convert authentication keys for SSH.

'-t rsa': This specifies the type of key to create. rsa stands for Rivest-Shamir-Adleman, a widely used public-key cryptosystem.

'-b 4096': This sets the number of bits in the key. A higher number of bits increases the security of the key. 4096 bits is a strong key size, providing higher security than the default (usually 2048 bits).

'-C "test@gmail.com"': This is a comment added to the key. It's often used to identify the key. In this case, the comment is an email address (test@gmail.com).


- this will generate your key after that type : cat ~/.ssh/id_rsa.pub ===> will show your key then copy it into your git under "Settings -> SSH and GPG Key" then make new SSH key and paste it into it then save

- after that at cmd : ssh -T git@github.com => then add your password you will be auth 
-------------------------------------------
