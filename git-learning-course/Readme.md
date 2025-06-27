## Git hidden folder 

`.git` is the folder which tells that your project is a git repo.

if we want to create a git repo in new project , we create the folder and then initalize that repo using `git init`

``` 
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init 
touch README.md
git status 
git add .
#open README.md and make changes to it 
git commit -a -m "add readme file" 
```
 
## Cloning 

we can clone in three ways : HTTPS , SSH , Github CLI

since I am using github codespaces , I will create a temporary directory in codespace
```sh 
mkdir /workspace/tmp
cd /workspace/tmp
```

### HTTPS 

```sh
 git clone https://github.com/hey-farhan/github-examples.git

 cd github-examples
```
>you will need to generate a personal access token (PAT) from your GitHub account to authenticate when using HTTPS.
https://github.com/settings/tokens

 - Give it access to Contents(Read and Write) and check the box for `repo` scope , for commits .

### SSH



## Commits 

when we want to commit code , we will use `git commit` . Using it without any flags will open the default editor to write a commit message.

use git commit -m <message> to commit with a message directly from the command line.(without opening the editor)




## Remotes 

## Stashing 

## Merging

## Add 

when we want to stage changes that will be included in the next commit, we use `git add`. This command adds changes from the working directory to the staging area.
```
git add <file> # stage a specific file
git add . # stage all changes in the current directory
```
## Status 
it shows the current state of the working directory and staging area. It displays which files are staged, unstaged, or untracked.



## Reset 

`git reset` is used to undo changes in the git history. It can be used to remove commits, unstage files, or even discard changes in the working directory.

>git reset will reset git add .

## .gitconfig 
file stores is what stores your git configuration settings. This file is typically located in your home directory (`~/.gitconfig` on Unix-like systems or `C:\Users\<YourUsername>\.gitconfig` on Windows).


when you first install git , you need to set your username and email address. This is important because every commit you make will be associated with this information.

```sh
git config --global user.name "Your Name"
git config --global user.email "your email"

# To view your current configuration settings, you can use:  
git config --list
```
### Push
when we want to push our changes to the remote repo/origin, we use `git push`. This command uploads the local repository content to a remote repository.

```sh
git push origin main
# push changes to the main branch of the remote repository
```


