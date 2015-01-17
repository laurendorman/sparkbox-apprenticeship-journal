# Git Real 2

## Chapter 1

### Rebase
* `$ git rebase |branch|` – Pulls in branch you are looking to rebase from.
* `$ git rebase -i HEAD~|#|` – The `-i` uses interactive rebase to edit the most recent # of commits specified.

### Interactive Rebase
* Can reorder commits simply by copying/pasting the commits in the necessary order.
* Use `reword` to change the commit message, this will bring open another window for you to change the message.
* Use `edit` to stop the specified commit.
* `$ git reset HEAD^` – Undo the changes that were just replayed.
* `$ git rebase --continue` – Finish the rebase, which resumes replaying the changes from the temp area.
* Use `squash` to add the commit to the previous commit, making them unite as one.


## Chapter 2

### Stashing Commands
* `$ git stash save` – Storing work that is not yet complete, it is an active WIP.
* `$ git stash list` – Lists all stashes that are stored.
* `$ git stash apply` – To continue working on the changes.
* `$ git reset --hard HEAD` – File reset, clears the mess from the index file and working tree.
* `$ git stash pop` – Gets staged changes back.
* `$ git stash save --keep-index` – Keep the index while stashing all unstaged changes.
* `$ git stash save --include-untracked` – Causes untracked files to be stashed too.
* `$ git stash list --stat` – Lists stashes and the file change information.
* `$ git stash show stash@{#}` --patch – Shows the particular stash you are looking to inspect, which shoes that specific stashes changes.
* `$ git stash save "message"` – Adds a message to the stash.
* `$ git stash branch |name|` – Checks out a new branch and drops the stash.

## Chapter 3

### Purging History
* `$ git clone |repository| |new location|` – Clone the repository in a new location.
* `$ git filter-branch --tree-filter "rm -f |unwanted file|"` – Removes the unwanted file from the entire tree.
* `$ git filter-branch --index-filter "git rm --cached --ignore-unmatch |unwanted file|"` – The `--index-filter` option runs the command against each commit without checking it out, so that it expedites the process. The --ignore-unmatch option will see to it that the command succeeds even if the file isn't present.
* `$ git filter-branch -f --tree-filter "git rm --cached --ignore-unmatch |unwanted file|"` – The `-f` will force an overwrite of the backup.
* `git filter-branch -f --prune-empty -- --all` – The `--prune-empty` option drops the commits that are empty and do not alter any files.

## Chapter 4

### Line Endings
* `$ git config --global core.autocrlf input` – Changes CR/LF (Windows) to LF (Unix) on commit.
* `$ git config --global core.autocrlf true` – Convers line endings form Unix to Windows on checkout.
* `*.bat text eol=crlf` coverts line endings for Windows, *.sh text eol=lf converts line endings for Unix.
* `$ git cherry-pick |sha|` – Moving a commit to a different branch, typically used to add a feature from the development branch to the production branch.
* `$ git cherry-pick --edit |sha|` – Change the message of the commit, providing more information, i.e. where it was added from.
* `$ git cherry-pick --no-commit |sha| |sha|` – Cherry-picking two commits without actually committing them to the current branch.
* `$ git commit -m "message"` – After cherry-picking, customize the commit message.
* `$ git cherry-pick -x |sha|` – Track which commit that you've cherry-picked from, since we've picked so many cherries.
* `$ git cherry-pick --signoff |sha|` – Signing off tracks who cherry-picked the commit, it adds the users name and email to the commit message.

## Chapter 5

### Submodules
* `$ git submodule add git@example.com:css.git` – Command that adds files from another repo. Submodules allows you to use shared code. A Git repo inside of a Git repo.
* `$ git add .gitmodules` – Stages the submodule(s).
* `$ git commit -m "message"` – As per usual, it commits the changes.
* `$ git submodule init` – Initializes the submodules so that they download their own contents.
* `$ git submodule update` – Checks for updates that have been made to the submodule.
* `$ git branch |name| |sha|` – Create a branch with a specific (usually most recent) commit.
* `$ git merge |branch|` **OR** `$ git merge |sha|` – Merges to the master.
* `$ git push --recurse-submodules=check` – Checks to see whether there are any un-pushed submodules.
* `$ git push --recurse-submodules=on-demand` – Allows for submodules ti be pushed automatically.
* `$ git config alias.|name| "|command|"` – Creates an alias for lengthy commands, if used in the terminal directly it can only be used during that session.

## Chapter 6

### Reflogging
* `$ git reset --hard |sha|` – When you do not need your latest commit, perhaps because it causes a bug.
* `$ git log --pretty=oneline` – Displays logs in a clean, one line format.
* `$ git reflog` – A second log, located in your local repo, that shows commits that may have been rolledback.
* `$ git reset --hard |sha|` **OR** `$ git reset --hard |sha| HEAD@{#}` – Allows you to restore a removed commit.
* `$ git log --walk-reflog` – Displays the full log format, including shortnames and messages.