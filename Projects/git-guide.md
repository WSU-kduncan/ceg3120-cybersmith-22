# Project 0 - Git Guide

Entries that are currently crossed out we will either get to later in the course that you could go back and write some details on later.

## Command line git

- status
  - Shows status of the local repository. This status includes:
   - 'number of local commits that have not been synced with remote (GitHub)' 
   - 'list of files in local folder than are NOT being tracked by git'
   - 'list of files in local folder that have changes that need to be committed'
  - 'git status'
- clone
  - Copies a repository to the current system.
  - `git clone git@github.com:WSU-kduncan/ceg3120-cybersmith-22.git`
- add
  - Adds the new or altered file to the staging area in preparation for the next commit.
  - `git add git-guide.md`
- rm
  - Removes files from a git repository.
  - `git rm git-guide.md'
- commit
  - Binds changes to file(s) and prompts the user to write about the changes made. 
  - `git commit -m "completed up until push command"`
- push
  - Syncs local repository with remote repository.
  - `git push`
- fetch
  - Downloads content from a remote repository.
  - `git fetch origin`
- merge
  - Incorporates changes from another repository or branch.
  - `git merge projects`
- pull
  - fetches content from the remote repository and merges it with local repository copy.
  - `git pull git@github.com:WSU-kduncan/ceg3120-cybersmith-22.git`
- branch
  - Lists, creates, or deletes branches
  - `git branch`
- checkout
  - Navigates between the branches created with the 'git branch' command.
  - `git checkout Projects`
- ~~init~~
- ~~remote~~

## git files & folders

- .git folder
  - The .git folder contains remote repository address and a log of the commit history.
  - `cd .git`
- .gitignore file
  - This contains files or folders that Git should ignore.
  - `cat .gitignore`
- ~~.git/hooks~~

## GitHub

- Pull requests
  - Proposed changes to a repository that are either accepted or rejected by the repository's collaborators.
- SSH authentication to repositories
  - Enables a secure encrypted connection to a GitHub repositories 
  - To crete a new SSH key:
    - In the wsl terminal, use the command: `ssh-keygen -t ed25519 -C "your_email@example.com"`
    - Open the folder that contains the new key, open the file that ends with `.pub` and copy the contents
    - On GitHub, navigate to "Settings" > "SSH and GPG keys" > "Add new key"
    - Give the key a name that ids the current semester, wsl, and the corresponding device
    - Paste the contents of the `.pub` file
- ~~Actions~~


## Resources

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Atlassian Bitbucket](https://www.atlassian.com/git/tutorials)