# Git-Commands
Basic commands for using Git

1. Version checking
`git --version`
2. Initialize repository as an empty repository 
`git init`

## Staging Area
1. Adding file or directory into staging area
`git add "file/directory"`<br/>
`git add .` "Add all file and directory"
2. Displays files which is needed to be commited
`git status`

## Local Repository
1. Do a commit and display a message `git commit -m "First Commit !"`
   * Error Counter (FIX BELOW !!): 
     - *** Please tell me who you are 
   1. `git config --global user.email "you@example.com"`
   2. `git config --global user.name "Your Name"`
   
## Remote Repository
1. Add Remote repository into local repository `git remote add origin "git@github.com:william5647/Git-Commands.git"`

## Pull File and Folder from remote repository
1. Pull files and folder in the remote repository `git pull origin master`
   * Error Counter (FIX BELOW !!):
     - fatal: refusing to merge unrelated histories
   1. Use `git pull origin master --allow-unrelated-histories`
   * Error Counter (FIX BELOW !!): 
     - git@github.com: Permission denied (publickey)
     - fatal: Could not read from remote repository
     
## Creating a local working copy of an existing remote repository
1. Cloning files and folder from the remote repository `git clone "remote repo link"`

## Generating a new SSH key
1. Open Git Bash.
2. Creates a new ssh key, using the provided email as a label. `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
3. Press enter to save the key in the default file location `(/c/Users/you/.ssh/id_rsa):[Press enter]`
4. Enter passphrase

## Adding your SSH key to the ssh-agent
1. Start the ssh-agent in the background `eval $(ssh-agent -s)`
2. Add your SSH private key to the ssh-agent `ssh-add ~/.ssh/id_rsa`

## Adding the SSH key to your GitHub account
1. Cat or Copy the SSH key to your clipboard
`cat ~/.ssh/id_rsa.pub` or `clip < ~/.ssh/id_rsa.pub`
2. Go to settings
3. Go to SSH and GPG keys
4. Click New SSH key or Add SSH key
5. Insert your SSH key into the "Key" field

## Push File and Folder into remote repository
1. `git push origin master`

## Branching
1. Creating a new branch `git branch "branchname"` <br\>
    or you can do `git checkout -b "branchname"`
2. Checking the list of available branches `git branch`
3. Point into a branch `git checkout "branchname"`
4. Merging a branch into master branch <br\>
    1. Go to master branch `git checkout master`
    2. Merging `git merge "branchname"`
5. Deleting a branch `git branch -d "branchname"`

## More Advanced Git Commands
1. Git stash - Used when you want to record the current state of the working directory and the index, but want to go back to a clean working directory
    1. Put all the uncomitted changes into a stash `git stash -u`
    2. Modification stash modified can be listed with `git stash list`
    3. Inspecting stash `git stash show`
    4. Returning the files and folder from stash `git stash apply`
 </br>
 2. Git log



Thank you for reading this basic tutorial on using Git !
