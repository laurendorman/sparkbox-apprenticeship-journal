# Git Real

## Chapter 1

### Git Help
* `$ git help` – List of all help options.
* `$ git help config` – Lists all configuration options/commands.
* `$ git config --global user.name "name"` – Who gets credit for changes.
* `$ git config --global user.email you@email.com` – What email you use.
* `$ git config --global color.ui true` – Pretty command line colors.

### Creating a Repo
* `$ mkdir |name|` – Creates directory folder.
* `$ cd |name|` – Changes directory folder where you are located.
* `$ git init` – Initializes empty repository and creates metadata file.

### Checking the Status & Staging Files
* `$ git status` – Checks the status of files in your local directory, identifies whether are untracked (unstaged) or have not yet been committed.
* `$ git add |file|` – Stages the file, preparing it for committing. Note: May list multiple files.
* `$ git add --all` – Adds all untracked files to the staging area.
* `$ git add <list of files>` – Adds the list of files.
* `$ git add *.txt` – Add all txt files in current directory
* `$ git add docs/*.txt` – Add all txt files in docs directory
* `$ git add docs/` – Add all files in docs directory
* `$ git add "*.txt"` – Add all text files in the whole project.

### Committing
* `$ git commit -m "message"` – Commits changes to the repo.
* `$ git log` – Shows a timeline listory of all commits.

## Chapter 2

### Unstaged & Staged Differences
* `$ git diff` – Shows the unstaged differences.
* `$ git diff --staged` – Shows the staged differences.

### Unstaging
* `$ git reset HEAD |file|` – Allows you to unstage files.

### Staging & Committing Simultaneously
* `$ git commit -a -m "message"` – Allows you to stage and commit all at once.

### Adding to a Commit
* `$ git commit --amend -m "message"` – Amending allows you to add to the last commit, best practice is to add a new commit message.

### Roll Back a Commit
* `$ git reset --soft HEAD^` – Undo last commit, "soft" puts changes into staging.
* `$ git reset --hard HEAD^` – Undo last commit and all changes.
* `$ git reset --hard HEAD^^` – Undo last 2 commits and all changes.

### Discarding Changes
* `$ git checkout -- |file|` – Discards changes. `--` ensures that you don't checkout a branch accidentally.

### Remote Repos & Pushing
* `$ git remote add origin |repository address|` – Adding a remote repository. Origin is the remote repository name.
* `$ git push -u origin master` – Pushing to the remote repository and setting it as your default push area.

## Chapter 3

### Clone a Repo
* `$ git clone |repository address|` – Clones a repo locally.
* `$ git clone |repository address| |directory|` – Clones a repo locally into a specific directory.

### List Remote Repositories
* `$ git remote -v` – Lists a verbose output of remote repositories.

### Create a Branch & Switching to it (Checking Out)
* `$ git branch |name|` – Used to create a branch.
* `$ git checkout |name|` – Used to switch to branch.
* `$ git checkout -b |name|` – Creates a branch and checks it out simuntaneously.


## Chapter 4

### Pushing & Pulling Changes
* `$ git push` – Sends new commits to GitHub (or other service).
* `$ git pull` – Retrieves the latest changes.

## Chapter 5

### Working with Remote Branches
* `$ git push origin |branch|` – Pushes a branch to remote branch.
* `$ git fetch` – Fetches remote branches.
* `$ git branch -r` – Lists all remote branches.
* `$ git push origin :branch` – Deletes remote branch.

### Cleaning Branches
* `$ git remote show origin` – Shows remote branch statuses.
* `$ git remote prune origin` – To clean up deleted remote branches.

### Working with Tags
* `$ git tag` – Lists all tags, used mostly for release versioning.
* `$ git checkout v[TAG]` – Checking out the code at a certain commit. Allows you to rollback to a certain tag/version.
* `$ git tag -a v[TAG] -m "message"` – Adds new tag.
* `$ git push --tags` – Pushes new tags.