
# Terminal & Git Commands CheatSheet

## Terminal Commands

### ls / ls -a => List contends of current directory

- Directories are listed simply as their name
- A file will show it's file extension after like file.pdf
- Tip ⇒ Don't see a file you know is in there?  Try ls -a  That will show all hidden files too.

### cd => Move between directories
- cd dir_name => Moves you into the directory
- cd .. => Moves you 1 directory up in the structure.
- cd ~ = Moves you to the very top directory.
- Tip ⇒ you can move into more than 1 directory at a time if you know the folder paths
    - cd Documents/CodingDojo/Git = instead of typing cd Documents then cd CodingDojo and so on.
- Tip ⇒ Type the first 3 letters of a folder then hit the tab button to let it fill out the rest of the directory name
- Tip ⇒ Have a directory name with a space (Unit 1)?  To enter this folder cd Unit\ 1 would be your command

### Make directories or files

- mkdir directory_name => Makes a directory ⇒ You will not see anything happen  when you type mkdir newfolder for example it does make a folder called newfolder but you won't see it unless you enter ls.
    - Tip ⇒ Want to make a directory with a space in it? (Unit 1) Put single quotes around the desired directory name like this => mkdir 'Unit 1' 
- touch filename.ext = Makes a new file ⇒ Again you will not see anything happen but if you ls again you will see the new file.  

### Remove directories or files
- rmdir dir_name => will remove the dir. It will not show you that it is deleted.
    - The dir you are trying to delete must be completely empty for this to work
- rm filename.ext => will remove the dir and agian will not show you that it is deleted.
- Tip ⇒ system will NOT delete a directory if there is content in it.  Don't see anything in their? Do a ls -a

### Open a file
- code filename.ext =>  This will open the file in your default IDE
    - You must be in the dir that that file is located in for this to work.

### Renaming a file
- mv index.html about.html (this will rename the index file to about)

### Moving a file
- mv index.html ../unit2/index.html (this will take the index file move it up 1 folder then donw to unit2 folder and place it there)

### Copy a file
- cp index.html copy.htmnl

### Copy a Directory
- cp -rf Unit2 copy_Unit2
- It is important to have the -rf to make sure that all files and folders contained inside the origional also get copied.

## Git Commands

### Setting up your terminal to push to github
- git config --global user.name "melissa-24"
    - In this case this would set the user name to my github username which is melissa24
    - Make sure you use --global or it will only work for where you are in the directories right then.
- git config --global user.email mlongenberger@codingdojo.com
    - This would set the email to the one above (make sure they are the same that the email you use here is the email for the github username)
- git config --global user.password ************
    - This one is a bit odd.  You will type your password where the *'s are but nothing will show up so make sure you type carfully.
- git config --global --list
    - This will allow you to see your stored settings.  

### git init
- initializes a new empty repository and create a hidden .git file This is how you will be able to push and save your work to github
    - The .git file contains everything the repository or project needs including commit logs.

### git clone urlLinkHere
- This will create a clone of the repository from github.
- In most terminals you have to hit CTRL + Shift + V for it to paste

### git checkout -b newBranchName
- This is used to create a new branch.  Unless this is done commits will be saved to the master branch.

### git checkout main
- If you are currently working on something in the newBranchName branch but want to switch over to the main branch you would type this.  In most cases you will need to commit your work before it will let you change

### git branch
- This will show you all the branches that are part of the git repository

### git log
- Gives you a log of all the backups or commits

### git blame
- This is a great tool when working on a team.  It allows you to see who wrote what

### git status
- This will give you an update of what files have had changes but have not been committed and are not being tracked.

### git add filename.html / git add *

- If entering for example filename.html then it will add just that file to the commit log.  If using * Then it will add all files changed to the commit log
- Tip.  Type the first few letters of the file name to add and hit the tab button and it will finish the name
- Tip. Have a folder inside the repo?  Add all the files of that folder in 1 command by typing the folder name and adding /  like a folder containing all CSS docs you names CSS  simply do git add CSS/

### git commit -m "enter message here"
- This will submit a commit to the save file.  Inside the "" goes your comment about the commit.  Basically anything but should be relevant to the changes made
- Tip ⇒ Commit often, you can keep creating commits before you push to github.  They will all be uploaded.  A commit just basically creates a retrievable save point

### git push / git push origin newBranchName
- This is used to push all saved commits to github.  
- git push on it's on is only if you are working on the main branch (Don't worry it will say something if you can push)
- Adding origin newBranchName means that you want to push your changes to the branch newBranchName.  

### git pull
- Once in the proper directory entering this command will pull changes from github that are not on your local machine
- Tip => Sometime the terminal will tell you that this needs to be done other times if you do this it will let you know if the local copy matches the github copy
