# Reminders for Git 

## Basic Commands

    git status

shows the current state of your staged and changed files

    git add _filename_

adds a specific file to the queue

    git add . 

adds all changed files to the queue

    git commit -m "commit message"

commits changes aka creates a save point

    git push 

sends your commits to the server

    git remote update 

updates info about remote repo, follow up with git status


## some setup commands

    ls -al ~/.ssh

Lists the files in your .ssh directory, if they exist (usually id\_rsa.pub / id\_rsa)

    ssh-keygen -t rsa -b 4096 -C "berni.fradl@gmail.com"

Creates a new ssh key, using the provided email as a label / Passphrase question optional

    eval "$(ssh-agent -s)"

Turn on ssh-agent

    ssh-add ~/.ssh/id_rsa

Add your SSH key to the ssh-agent.

    clip < ~/.ssh/id_rsa.pub

Copies the contents of the id_rsa.pub file to your clipboard to paste it to github (create new ssh)

    ssh -T git@github.com

Test the connection.

## some troubleshoot commands

    git push --set-upstream origin master

    git config --global push.default simple

the difference to matching is basically that, simple only pushes the branch your currently working on and matching tries to push all branches that match the name to a branch on the remote repo.
