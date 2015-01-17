# Git

## Understanding Git
* Git is a Distributed Version Control System (DVCS).
* A file system that controls a file system with commands that work within it.
* Version control does not require an internet connection.
* Pushing a commit does require an internet connection.
* `$ git clone` - Gives you the latest *master* version and allows you to review changes.
* `$ git push` – To share changes with others and send to the web.

## Applications
* Sourcetree (Free).
* Tower (Paid), preferred.
* GitHub for Mac, easy to use.
* Apps hide the complexity of Git and makes many decisions for you.

## Committing
* First commit is typically marked by "init commit."
* .git folder contains statistics of the repo which compose a graph.
* Every commit contains a sha (unique ID for commits), email (authentication) and a message (detailing commit).
* Conflicting commits are overwritten.
* Rebase – Cleans up commits, allows you to move branches around by changing the commit that they are *based* on (hence the name).
* `$ git add` / `$ git commit` – Used for committing changes, creates a sha and stores the changes made.

## Additional Notes
* *master* is the active, working branch – all other branches are for building without breaking.
* A branch allows for building out features and experimenting, it is an error-proof way of incorporating changes.
* Tags highlight important parts in file history – used to mark a release point, such as v1.0, etc., pointing to specific shas.
* Tags can be moved.
* Kaleidoscope is application that uses syntax highlighting as a visual representation of changes, showing which lines will be effected.
* `$ git branch` – Displays all branches available.
* `$ git branch |name|` – Creates new branch from current branch.
* `$ git branch -r` – Remote branches, used to access/fetch remote branches.
