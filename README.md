# generate ssh keys

    ssh-keygen -t ed25519-sk -C "YOUR_EMAIL"

Add the public key to github settings->SSH and GPG keys

# Git Clone repository
click on code
get the ssh or https url of the repo
ex: 
    
    windows
    git@github.com:girishjalli18/git-help.git
    or 
     ssh-keygen -t ecdsa-sk -C "your_email@example.com"

    linux
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

clone the project
    
    git clone --recursive git@github.com:girishjalli18/git-help.git


# Useful git commands

## check the global is set

    git config --global user.email "girishjalli18@gmail.com"
    git config --global user.name "Girish Jalli"


## git color output

    vi ~/.gitconfig
add below lines

    [color]
	    diff = auto
	    status = auto
	    branch = auto
	    interactive = auto
	    ui = true
	    pager = true

## Ensure branch is master

    git symbolic-ref --short -q HEAD


## GIT Rebase

    git checkout master
    git pull upstream master
    git checkout dev-branch
 do the development changes
 add files
`git add <file1> <file2>`

    git commit -m "commit message"

rebase to the master

    git rebase -i master


push changes to origin branch


    git push origin branch name

*in VIM - ":wq"

 *resolve conflicts

    git add --all
    git rebase --continue
    git push -f origin dev-branch


## check remote settings
    git remote -v