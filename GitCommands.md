# Git Documentation

## ssh keygen for git
https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/ 

## Clone a repository
git clone git@github.com:<username>/<repository-name>.git


Default stream-name is “origin”

## Tell git who you are
git config --user.name “github-username”  
git config --user.email “github-registered-email_id”

## Add new stream to your repository
git remote add <stream-name> git@github.com:<username>/<repository-name>.git  
Example: git remote add upstream git@github.com:RadialFunction/codaxtr-extractor.git

## Get remote repository name/stream name
git remote -v  
This will output as follows  
stream-name repository-link (fetch)  
stream-name repository-link (push)  

## Remove stream from local machine
git remote rm stream-name  

## Fetch all the branches from remote repository with removing untracked branches from local
git fetch --prune

## Fetch all the branches from remote repository
git fetch <stream-name>

## Create a new branch from main
git checkout main  
`git checkout -b branch-name` or   
`git branch branch-name`  
`git checkout branch-name`  

## Create a new branch with the changes in existing branch
git checkout <existing-branch-name>  
git checkout -b <new-branch-name>  

## Display all the branches
git branch  
git branch -r (To display remote branches also)  
Output:  
stream-name/HEAD -> stream-name/master  
stream-name/branch-name-1  
stream-name/branch-name-2  
…

## Delete branch from local and remote repository
git push <stream> --delete branch-name  
git branch -D branch-name (force delete)  
git branch -d branch-name  


## Sync with remote repository
git checkout master  
git pull upstream master  
git push origin master  
git checkout branch-name  
git merge master  
git push origin branch-name  

## Push items to repository
 
git push stream-name branch-name  

## Update an existing file
git commit -m “commit-message” filename1 filename2 …  
git push stream-name branch-name  

## Remove a file from git-repository
git rm filename1 filename2 …  
git commit -m “commit-message”  
git push stream-name branch-name  

## Moving files from one folder to another
git mv src_directory/filename destination_directory/filename  
git add destination_directory/filename  
git commit -m “commit-message”  
git push stream-name branch-name  

## Undo local change which are not committed
git stash (will stash all the changes)  
git stash -p (to stash specific change, will interactively ask if you want to stash particular change with y/n options)  

## Clean git-repository (Remove all untracked files and directories)
git clean -f (removes untracked files; -f is force)  
git clean -f -d (removes untracked directories and files)  
git clean -n (dry-run, doesn’t remove anything, just shows what would be done)  

