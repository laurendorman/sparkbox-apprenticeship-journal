# Customizing Your Shell


## dotfiles
* A series of configuration files that store program settings, create command aliases and more.
* Organizing and storing your dotfiles in a repository allows you easily set up a new machine with your favorite preferences and settings.

## Aliases
* Shorthand for long or not-so-easy-to-remember commands.
* You may set temporary aliases by running the alias |name|='desired command', which may be used for your current terminal session.
* Store aliases by putting them in a safe place (hint: your dotfiles).

## Symbolic Links (symlinks)
* Shortcuts that link to individual files or folders without having to deal with the pain of duplicate files.
* To create symbolic links, use the command: ln -s ~/[TARGET DIRECTORY OR FILE] ~/[SHORTCUT]

## Good Starting Points (Files)
* .bash_profile
* .bashrc
* .gitconfig
* .gitignore


## Resources
[GitHub dotfiles][]
[.bash_profile vs .bashrc][]
[Adam's dotfiles][]

[GitHub dotfiles]: https://dotfiles.github.io
[.bash_profile vs .bashrc]: http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html
[Adam's dotfiles]: https://github.com/asimpson/dotfiles