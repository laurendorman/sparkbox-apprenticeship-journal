# Trying Git

## Commands
* `$ git init` – Initializes a Git repository.
* `$ git status` – Checks the current state of your project, will notify you of untracked files. Should be ran before all commits.
* `$ git add |file|` – Adds the file to the staging area.
* `$ git commit -m "message"` – Stores the staged changes and commits them to the repository.
* `$ git add "*.extension"` – Adds all files with the extension specified. Must include quotes.
* `$ git log` – Shows all changes (commits) applied during the session.
* `$ git remote add origin |respository URL|` – Adds a remote repository.
* `$ git push -u origin master` – Pushes and publishes the changes. `-u` tells Git to remember where we are pushing so that the command `$ git push` is the only thing needed for your next push.
* `$ git pull origin master` – Will pull down any new changes since your last visit.
* `$ git diff HEAD` – Shows the changes that have been committed since your last visit.
* `$ git diff --staged` – Shows which files have changes that have been staged.
* `$ git reset |directory|/|file|` – Unstages the file.
* `$ git checkout -- |file|` – Undoing changes since the last commit.
* `$ git branch |name|` – A branch to make separate commits while working on features or experimenting.
* `$ git checkout |branch|` – Switch branches.
* `$ git rm "*.extension"` – Removes all of the files from the disk and staging.
* `$ git merge |branch|` – Merges branch with master (if you've checkout to master, of course).
* `$ git branch -d |branch|` – Once successfully merged, you may delete the branch.
* `$ git push` – Pushes all of the changes to your remote repository.git rm