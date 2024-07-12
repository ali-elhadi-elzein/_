Now that you know the basic functioning of git, let's learn some advanced concepts.

### Collaboration

This is one of the main reasons why we are learning git. Git allows multiple developers to share a repository and work on the same project without losing any changes. The same concepts that you have learned till now can be extended to work with multiple developers/(Project Collaborators)

In real-world scenario having the repository on your machine won't make much sense since your team members would also need to access the repository. Services like Github, Gitlab solve that problem (Github and git are two different things, Github is an online service that lets you manage your git repositories)

Git also lets you work on your project without the internet since you only need the internet to sync your repository. Even if GitHub is down you can continue working on your project. To learn some of the advanced concepts of git we will connect to a GitHub repository and try running some git commands.

### Creating a Repository in Github

Sign in/Signup to Github and click on New repository (usually this page is hidden under the + icon close to the profile picture), On the Create form give a name for your repository. You can name it anything you want for now ( Use \_ or - instead of spaces ).
Public repositories are available to anyone on the internet. Private repositories are only visible to you and the folks you choose to share them with. Let's go with the public repository option for now.
Uncheck Readme Files and any other option for now and create the repository.

### Linking your local repo to a Github repo

\*_repo is short for repository_

Now that you have a Github repository, we need to link your local GitHub repository to GitHub so that it can sync the changes. To do this we need to locate the URL of your GitHub Repository. You can use the HTTP address/URL of your newly created Github repo for now. The URL will be of the form <https://github.com/>`github_username`/`repository_name`

Once you have the URL the following command will link the local repository to the remote repository

```git
git remote add origin https://github.com/github_username/repository_name
```

Here the word origin is not a keyword, you can name it anything you want. Usage of the word origin is just standard convention.

### Basics of Git Branches

Branching is a feature in git which allows you to isolate your work and work on multiple changes simultaneously. You can switch between branches without creating multiple development environments. Branches are extremely useful when you want to work on different parts of the project simultaneously. To know what is the current branch you can execute the `git status` command we used earlier. The first line of its output will tell you what branch you are on.

By default, you will be in the master or main branch of your repository (master used to be the default branch in GitHub but recently it was changed to main)

### Syncing Repositories

Now that you have linked the Github repository, you can pull (move changes in GitHub into your local repo) or push (move local changes from your local repo into Github's repo) changes, since we already have changes made in local, we can push the changes into GitHub with the following command

```git
git push origin main
```

Origin is a reference to the URL we added earlier and main is the branch we want to push to

Similarly, we can also pull changes from the remote repository with the following command

```git
git pull origin main
```

### Merges and Conflicts

When multiple developers work on a single project and make changes to the same file, the changes made by each developer are not merged together, instead, they are kept in separate branches. Git allows separate branches to be merged together. If the changes are not conflicting git will automatically figure out a way to merge the branches together. But if there are conflicts that need to be resolved, git will not automatically merge the branches

Usually, When multiple developers have made changes to the same file in multiple branches, you have a conflict. We have to manually resolve the conflict and select the version that we want to keep.

### Forking

Forking is a feature in git that allows you to create a copy of your repository on your own account. This is useful when you want to work on a project that you have not created yourself. Forking allows you to create a copy, that you can freely experiment without affecting the original repository.

Forking is usually used to propose changes to the original repository and then merge those changes into the original repository.

In Github, with every repo, you have the option to fork it from the UI. Once the fork is created you can make changes to it.

### Pull Requests

A pull request is a request to merge a branch into another branch or a fork into the main repository. It lets the maintainers of the project know that you wish to merge your code into their project. Pull requests are often used to propose changes to a repository, Which is a great way to share code with others.

Once a pull request is made, you can discuss and review the potential problems and limitations of the changes with the folks who maintain the project. You can continue adding commits to the pull request until you are satisfied with the changes.

_To complete this lesson, we'd like you to practice using git by working through the ._ [Git-it Guide](http://jlord.us/git-it/)

### Ignoring Files
When developing a project, you may not want to git track some specific files, this could be anything from your editor's settings to a secret file you maintain.

Git includes a feature that allows you to do just this, create a file called `.gitignore` in the root of your repository, any files or patterns that you specify in this file will not be tracked by git (unless forced). This is a great way to keep your repository clean and free of any sensitive information. Here is a [template](https://github.com/github/gitignore/blob/main/Python.gitignore) that you can use, add the git ignore file as soon as you create your repo.
### Tips/Tricks for Git

It is incredibly easy to mess up a git repository and the best way to learn how not to do it is to keep experimenting. Trying out various techniques and finding the sweet spot.  
Whatever happens, do **not** try copy-pasting git code unless you know exactly what it's doing **( There is only pain down that path ! )**  
Commit messages and Branch Names should always make sense. Otherwise, years later you'll blame yourself **( That's what I did )**  
There is a sea of open source software out there, try to find something interesting and contribute. That's the recommended way to become a better developer!
