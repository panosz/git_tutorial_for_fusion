# A Brief Turorial on Git

This is a tutorial for windows users written by a Linux user, so it will definitely contain some errors. 

## Installing Git

### Download Git for Windows:
- Visit the official Git website at [git-scm.com](https://git-scm.com/).
- Download the latest version for Windows.

###   Install Git:
- Run the downloaded installer.
- Follow the installation instructions. You can leave most options at their default settings, but ensure that "Git Bash" is included and "Use Git from the Windows Command Prompt" is selected.

## Setup

- Create a new folder for your project and type
```shell
git init
```
This will create a .git subfolder


- type
```shell
git status
```
This will print a message:

    On branch <branch_name>

    No commits yet

    nothing to commit (create/copy files and use "git add" to track)

By default <branch_name> is "master" but this is considered obsolete by most services. If it is "master", go ahead and
rename it to "main":

```shell
git branch -m main 
```

Now type again
```shell
git status
```
to verify that the name of the branch has changed.
