# Git Cheatsheet

## learning git
These are the two best resources I came across for learning git and how git works:
- [YouTube: Scott Chacon of GitHub](https://www.youtube.com/watch?time_continue=2&v=ZDR433b0HJY)
- [eBook: Pro Git by Scott Chacon & Ben Straub](https://git-scm.com/book/en/v2)
  - He recommends relying on these few commands:
  - init, clone (create or clone projects)
  - add, status, diff, commit, reset, rm, mv (basic snapshotting)
  - branch, checkout, merge, log, tag (branch and merge)
  - fetch, pull, push(?) (share, update)

## References
- [GitHub Guides: Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [GitHub Git CHEAT SHEET (pdf)](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
- [Git Cheatsheet "An Interaction From NDP Software"](http://ndpsoftware.com/git-cheatsheet.html#loc=local_repo;)
- [Git docs](https://git-scm.com/docs)
- [A Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-en.html)

## Quick Reference

### Initializing and connecting to remotes
- [Upload existing local repo to new github repo](https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line)

### Branching
- `git checkout -b my_new_branch` create and switch to new branch
- `git branch -a` List all branches, including origin/HEAD and origin/master
- `git branch my_new_branch` Create new branch 
- `git checkout my_new_branch` Switch to other branch 
- `git branch –m my_new_branch renamed_branch` Rename a branch 
- `git branch -d my_new_branch` Delete a branch 
- `git tag v0.1.5` adds lightweight version tag to current commit

### Stage and Unstage
- `git add <file_path>` to stage file
- `git add .` to stage all untracked files. (What does -A do?)
- `git reset HEAD <file_path>` to unstage file

### Commit
- `git commit -m "My first commit, inline"`
- `git commit` to add multi-line comment

### Push
- `git push` throws an error if there are remote repo commits you haven't fetched/pulled yet.

### Merge
- switch to Master branch (or whatever branch you want to merge changes **into**)
- `git merge --squash branch_name` compresses all of `branch_name`'s commits into one and merges that into master.

### Viewing information
- `git log`
  - Options: `--abbrev-commit`
- `git lol` (How to set this up?)
- `git help <command>`

### diff


### .gitignore
[Git docs: gitignore](https://git-scm.com/docs/gitignore)
```
# Exclude files containing:
*pycache*
# Exclude files ending in:
*xml
# Exclude directories and their contents:
/.idea*
/data/private/*
/.vscode*
/docs*
```

## Running git on Windows
- download and install Git for Windows. This installs Git Bash, a terminal where you'll interface with git.

### Git Bash
- ...
#### .bashrc

#### .bash_profile
- .bash_profile (at least on windows) is where my aliases are stored. I thought that was supposed to be the .bashrc, so now I'm left wondering what that file 
- Configuration file for BASH 
- bashrc = BASH Runtime Configuration 
- When you run BASH, it looks for this file in your home directory (`cd ~`) 
- Amongst other things, it stores aliases (e.g. for running notepad++ by typing `npp` 

#### .gitconfig
- Configuration file for Git
- https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup 
- Note: global settings affect all git interactions. Local is ... local to a single repository

Commands:
- `git config --global --list` lists all my global configurations 
- `git config --global –e` OR `npp ~/.gitconfig` edits config file in editor 
- `git config --global alias.<alias-name> "<full command>"` adds a git alias 
- `git config --list --show-origin` displays all current setting and where they come from (I assume this will show both local and global settings...) 

#### Bash commands
- `cd` changes directory, `cd ..` goes one directory up, `cd -` returns to previous directory. See https://mhoffman.github.io/2015/05/21/how-to-navigate-directories-with-the-shell.html
- `ls` lists all files and directories. `ls -al` does the same in a structured format.

#### Configure notepad++ as editor
- Install Notepad++ 
- Add Notepad++.exe's path to the path variable 
- In Bash:
  - `notepad++` runs notepad++ 
  - `notepad++ <file_path>` opens a file in notepad++ 
  - Create "alias" (a shortcut):
    - Navigate to home directory: `cd ~`
    - `notepad++ .bashrc` to open .bashrc in notepad++. 
    - `alias npp='notepad++.exe -multiInst -nosession'`. Save and close. 
    - Restart BASH window to be able to use the alias. 
  - Open a file by: `npp <file_path>` 
  - [notepad++ command line switches](http://docs.notepad-plus-plus.org/index.php/Command_Line_Switches)

## PyCharm IDE
- Can be configured to interface with git.
- The terminal uses your Bash settings.
