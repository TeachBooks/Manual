# Create your own version (branching, cloning, pulling)

Branches are a very useful feature of Git. Branches allow you to work on multiple versions of your codebase simultaneously; you create a copy of your codebase, on which you can work independently of the main codebase. The main branch is the default branch. The content on this branch will be the most up to date version of the book. Therefore, new branches, which are made to add or fix some content in the book, are usually cloned from the main branch. This has many advantages compared to making the edits immediately in the main branch.  Some advantages of working with branches are:

- Isolation: when you work on your own branch, your changes are isolated from the main codebase. Unfinished or unreviewed parts of your book are "hidden". Your own branch helps to keep an overview of the changes made to the book. 
- Collaboration: branches make it easier for multiple project members to work on the same codebase simultaneously. If every member works on their own branch, they can make their changes without having to worry about interfering with another members' changes. In case those changes made in parallel lead to conflicts, they can be resolved during the merging of the branches. 

This systematic workflow guarantees that editing the book goes smoothly. 

The act of making a new branch from an existing one is called *branching*. Usually, you want to branch from the `main` branch, but you can of course also choose to branch from another branch. The branch from which you create a new branch is called the *source* branch.

**Create your own version as ...**

```````````{tab-set}

``````````{tab-item} ... user type 3 ...

**... by directly creating your own version of the book (branching) or selecting an existing version in ...**

```````{tab-set}

``````{tab-item} ... GitHub

```{include} new_branch_github.md
```

``````
``````{tab-item} ... GitLab

```{include} new_branch_gitlab.md
```

``````
```````
``````````

``````````{tab-item} ... user type 4 and 5 ...

As user type 4 and 5, you make changes to the book locally on your computer rather than online on GitHub/GitLab. This allows you to create more complex and interactive sections to your book. Before you can start, there are a few preparatory steps you need to take. 

In order to create your own version, you will first have to open the repository. Then, you will need to clone the repository to your computer. This procedure is called cloning.

If your repository is already cloned on your computer, you are almost ready to start editing the book. However, remember that you are most likely not the only person making changes to the book. To keep an overview of the changes made by you and your colleages, it is important that changes are first made in a 'copy' of the book and are then merged into the final version. This is done through branching! You can create your version of the book by creating a new version (branch) or you can continue the work in an existing version (checkout branch). 

`````````{tab-set}

````````{tab-item} ... when opening repository for first time…

**(a) ... by finding the repository url from ...**

```````{tab-set}

``````{tab-item} ... GitHub

1. Open the repository that you would like to clone. In the top bar on the right, you will a green button called `<> Code`.

```{figure} figures/NewBranch_GitHub.PNG
---
name: NewBranch_GitHub1
---
Overview
```

2. Clicking on the button will display the following screen. Make sure the option `SSH` is selected and copy the link.

```{figure} figures/Clone_GitHub.PNG
---
name: Clone_GitHub
---
Clone using SSH
```

``````
``````{tab-item} ... GitHub through GitHub Desktop

1. Open the repository that you would like to clone. In the top bar on the right, you will a green button called `<> Code`.

```{figure} figures/NewBranch_GitHub.PNG
---
name: NewBranch_GitHub2
---
Overview
```

2. Clicking on the button will display the following screen. Click on `Open with GitHub Desktop`.

```{figure} figures/Clone_GitHub.PNG
---
name: Clone_GitHub1
---
Clone using SSH
```

3. The Browser should then automatically open GitHub Desktop. Customize the path to the location where you would like to save to files locally. Finally, click on `Clone`.

```{figure} figures/CloneRepo_TroughGithubdesk.PNG
---
name: CloneRepo_TroughGithubdesk.PNG
---
Clone through GitHub Desktop
```

You have now directly cloned the repository, so you can skip the next step!
``````

``````{tab-item} ... GitLab

1. Navigate to the repository of your book. Click on the blue button that says "Clone", and copy the link under "Clone with SSH".


```{figure} ../images/gitlab-clone.png
---
name: gitlab-clone
---
The cloning menu.
```
``````

```````


**(b) ... and opening (cloning) the local repository with ...**

```````{tab-set}


``````{tab-item} ... VS Code

1. Open a new VS Code window. You should be greeted with a welcome page. On this page, click "Clone Git Repository". Alternatively, open the Source Control menu from the left side bar, and click on "Clone Repository".

```{figure} ../images/vscode-welcome.png
:name: vscode-welcome

The VS Code welcome screen.
```

2. On the top of your screen, you should get a prompt asking you for a URL. In this field, paste the link you copied from GitLab and press enter. It will ask you to choose the location of the repository. After you've chosen a location, a final prompt will show up asking if you want to open the repository. Click on "Open".

3. You now have a local copy of the repository.
``````

``````{tab-item} ... GitHub Desktop

1. You have previously copied the link of the repository you would like to clone from GitLab or GitHub. In GitHub Desktop, navigate to the top bar, click on `File` and then on `Clone repository`.

<figure align="center">
    <img src="figures/CloneRepo_Githubdesk.png" alt="Example Image" width="350">
</figure>

2. In the top bar click on `URL`.

<figure align="center">
    <img src="figures/CloneRepo_TroughGithubdesk.PNG" alt="Example Image" width="400">
</figure>

3. Simply paste the link, specify the working directory (location where you would like to save the folder locally) and click on 'Clone'.

4. You now have a local copy of the repository.

``````
```````
**You have now cloned the repository to your computer and you can start branching. <br> 
Have a look at the other section!**
````````

````````{tab-item} ... when working  in previously opened repository…

**(a) by creating my own version (branching) or select an existing version (checkout branch) ...**

Although it is possible to create new branches in VS Code or GitHub Desktop directly, creating new branches on the remote repository (on GitLab or GitHub) is better for collaborating because the new branch becomes immediately visible to everyone working in the repository as opposed to becoming visible after being pushed/published to the remote repository.

`````{tab-set}
````{tab-item} ... GitHub

```{include} new_branch_github.md
```

````

````{tab-item} ... in GitLab

```{include} new_branch_gitlab.md
```

````
`````

**(b) and updating my local repository (checking out and pulling) ...**

```````{tab-set}
``````{tab-item} ... with Git in VS Code

1. Open own version (checking out)

If you want to work in an existing branch you need to *check out* our new branch in VS Code. *Checking out* means that we're changing our working branch (i.e., the one to which we will be committing our changes) from one to the other. 

In VS Code, open the branch menu from the bottom left (see {numref}`git-branch-menu-main`). You'll be be greeted with a menu that looks like the one in {numref}`git-branch-selection-menu`. In this menu, we get an overview of the branches of our repository. Notice that our new branch `chapter-2` appears as `origin/chapter-2`, and has a cloud icon in front of it. This means that the branch only exists on the remote repository. 

Check out the branch by simply clicking on it. Check that the branch is indeed checked out by looking at the branch menu button in the bottom left again; it should now say the name of your branch instead of `main` (in our case `chapter-2`). 

```{figure} ../images/git-branch-menu-main.png
---
name: git-branch-menu-main
---
Location of the branch menu.
```

```{figure} ../images/git-branch-selection-menu.png
---
name: git-branch-selection-menu
---
The branch selection menu, where our new branch has shown up. From this menu you can also select (checkout in git terms) another existing branch.
```

2. Update your local repository

Since you are working in a repository with multiple colleagues, it is good practice to make sure your local repository is up to date. This is especially important when you want to work in an existing branch. In that case you want to make sure that the existing branch shows in your local repository. Therefore, you first need to pull all the changes from the remote repository to your local repository. Simply click the Icon with the two arrows.

```{figure} figures/Pull_VS.PNG
name: Pull_VS

Location of the branch menu.
```

``````
``````{tab-item} ... with GitHub Desktop

1. Open own version (checking out)

The next step is to *check out* our new branch in GitHub Desktop. *Checking out* means that we're changing our working branch (i.e., the one to which we will be committing our changes) from one to the other. 

In GitHub Desktop, the top bar has a menu called `Current Branch`. By clicking on it you can see all the branches you created on the remote repository. 

```{figure} figures/CheckOutBranch_GitHubDesktop.PNG

Branches overview
```
2. Check out the branch by simply clicking on it. The following window will pop up.

```{figure} figures/CheckOutBranch_GitHubDesktop2.PNG

Leave changes
```
Leave your changes (stashed) on your working branch, in this case I was working in the branch called `collaboration git`.

3. Check that the branch is indeed checked out by looking at the branch menu at the the top left again; the current branch should say the name. 

4. Update your repository

Since you are working in a repository with multiple colleagues, it is good practice to make sure your local repository is up to date. This is especially important when you want to work in an existing branch. In that case you want to make sure that the existing branch shows in your local repository. Therefore, you first need to pull all the changes from the remote repository to your local repository.  

This synchronizes the remote repository with your local repository on your computer. Click on `Fetch` in the top bar. Then on the same place, click on 'Pull'. 

<figure align="center">
    <img src="figures/Fetch.PNG" alt="Example Image" width="650">
</figure>


``````
```````
**Now that you have created and checked out your new branch, you can start [making and committing changes](edit_book.md).**

````````
`````````
``````````
```````````
