#GIT commands

git init - create a new git repo
git status - view changes to the project code
git add - add files to staging area
git commit - creates a new commit with files from staging area
git log - view recent commits

# Git commands

git init - create a new git repo

git status - view the changes to your project code

git add - add files to the staging area

git add <filename> || .

git commit - creates a new commit with files from the staging area

git commit -m "Initial commit"

-m denotes a message initial

"" actual text string

git log - view recent commits

# secured Shell - SSH

Open Git Bash.

Enter ls -al ~/.ssh to see if existing SSH keys are present:

\$ ls -al ~/.ssh

# Lists the files in your .ssh directory, if they exist

Check the directory listing to see if you already have a public SSH key.

#Generating a new SSH key
Open Git Bash.

Paste the text below, substituting in your GitHub email address.

\$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
This creates a new ssh key, using the provided email as a label.

Generating public/private rsa key pair.

# Adding your SSH key to the ssh-agent

#start the ssh-agent in the background
$ eval $(ssh-agent -s)

> Agent pid 59566

# Add your SSH private key to the ssh-agent

\$ ssh-add ~/.ssh/id_rsa

# Add the SSH key to your github account

\$ clip < ~/.ssh/id_rsa.pub

login into your github account -> settings -> ssh & gpg keys -> New SSH Key -> paste in the keys tabs

# push the local master to github master

> open repo, copy the ssh url
> git remote add origin git@github.com:PrakashManoharan/expensifyApp.git

> git remote
> git remote -v
> git push -u origin master