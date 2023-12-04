# A Brief Turorial on Git

This is a tutorial for windows users written by a Linux user, so it will definitely contain some errors. 

## Installing Git

- Visit the official Git website at [git-scm.com](https://git-scm.com/).
- Download the latest version for Windows.
- Run the downloaded installer.
- Follow the installation instructions. You can leave most options at their default settings, but ensure that:
    * [ ] "Git Bash" is included 
    * [ ] "Use Git from the Windows Command Prompt" is selected.


## Installing Sublime (optional)

### Text editor
Much of the value of git is lost without good editor support. `Sublime Text` is a neat editor with integrated editor support. 
- Download it and install `Sublime Text` from [here](https://www.sublimetext.com/)


### Git client
Working from the command line may be very effective, but can be off-putting at first. A good git client offers a more
attractive experience and can also help guide you through your first steps in mastering git.

- Download and install `Sublime Merge` git client [here](https://www.sublimemerge.com/)

## Quick Start

### Setup a local repository
- Create a new folder for your project and type
```shell
git init
```
This will create a .git subfolder

- type
```shell
git status
```
This will print a message like the following:

    On branch <branch_name>

    No commits yet

    nothing to commit (create/copy files and use "git add" to track)

By default <branch_name> is "master" but this is considered obsolete by most services. If it is "master", go ahead and
rename it to "main":

```shell
git branch -m main 
```

Now type again:
```shell
git status
```
to verify that the name of the branch has changed.

### Working with files
- Add some files to the folder 

### Add Files to Staging Area:

- To add a specific file:
    ```bash
    git add filename
    ```
- To add all files:
    ```bash
    git add .
    ```

#### Commit Changes:

- Commit your changes with a message:
    ```bash
    git commit -m "Your commit message"
    ```   
#### View Commit History:

- To see the commit history:
    ```bash
    git log
    ```

#### Branching

1.   Create a New Branch:
    - To create and switch to a new branch:
        ```bash
        git checkout -b new-branch-name
        ```

2. Switch Between Branches:
    - To switch to an existing branch:
        ```bash
        git checkout branch-name
        ```   
3. Merge Branches:
    - To merge a branch into your current branch:
        ```bash
        git merge branch-name
        ```

#### Working with Remote Repositories
1. Add a Remote Repository:
     -  To link a remote repository (like one on GitHub):
        ```bash
        git remote add origin https://github.com/username/repository.git
        ```
2. Push Changes to Remote:
   - To push your committed changes:
        ```bash
        git push -u origin master
        ```

2. Pull Changes from Remote:

   - To update your local repository with changes from the remote:
        ```bash
       git pull origin master
        ```


## Authenticating with github
- Authenticating with github may require a bit of effort.
- GitHub no longer supports username and password authentication for interaction with the repositories (push/pull)
- One option is to use personal access tokens. This is what we will follow here.
- To create your PAT, follow these [instructions](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic)
- Instructions on how to use personal access tokens [here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#using-a-personal-access-token-on-the-command-line)
- When using PAT, make sure to work with the HTTPS and not the SSH addresses of the remotes


