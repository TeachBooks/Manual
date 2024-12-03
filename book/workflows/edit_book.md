# Edit (merge conflicts, staging, committing, pushing)

Suppose we are writing a new chapter, or are updating an existing chapter for our Jupyter Book. We've created a new branch on which we are going to make the changes.

**Edit files as ...**
`````````{tab-set}
````````{tab-item} ... user type 3 ... 

**... by directly adding changes on a single file to the Git-timeline (committing) in ...**

```````{tab-set}
``````{tab-item} ... GitLab

In GitLab, you can directly make changes in the files on the remote repository. You can make changes to the files already in the repository using the text editor but you can also upload new files!

1. Navigate to the repository you want to work in and make sure you're in the correct branch.

2. Create a new file by clicking on the plus button in the top bar. You can either create an entirely new file by clicking `New File` or if you already have created a file you can upload it by clicking `Upload File`.

```{figure} figures/User3_NewFile.PNG
width: 60%
align: center

Create new file
```

3. In the new window, you can start typing your content. Give your file a name and make sure to use the markdown extension: `Chapter1.md`. Once you are done, commit the new file to the repository by clicking the blue button `Commit changes`.

```{figure} figures/User3_NewFile2.PNG
align: center

Edit new file
```

4. In case you want to make changes to an existing file, navigate to the file in your remote repository. Then click the blue button called `Edit` and select the option `Edit single file`.

```{figure} figures/User3_EditFile.PNG
align: center

Web Editor
```

5. Make your changes in the text editor and when you are ready, commit your changes to the remote repository by clicking on the blue `Commit changes` button.

```{figure} figures/User3_NewFile2.PNG
align: center

Commit changes
```

6. In case you added a new file, you also need to include it table of contents of your book! The table of contents is specified in a file called `toc.yml` and it is already included in your repository if you used the teachbooks template. You can edit it and commit the changes in the same manner as you did with markdown `file.md` files.

```{figure} figures/User3_toc.PNG
align: center

Table of contents (TOC)
```
``````

``````{tab-item} ... GitHub... 

`````{tab-set}
````{tab-item} ... using 'Edit in place'

How to make an edit and make a commit is demonstrated in the gif below. <br> Don't worry if the steps are too fast, all steps are elaborated on in the following step-by-step tutorial.
 
```{figure} figures/user3-collaboration.gif
---
name: user3_edit_demo
---
Demonstration, video available [here](https://youtu.be/LG1vzrOLQHA)
```

In GitHub, you can directly make changes in the files on the remote repository. You can make changes to the files already in the repository using the text editor but you can also upload new files!

1. Navigate to the repository you want to work in and make sure you're in the correct branch.

2. Create a new file by clicking on the button called `Add file` in the top bar. You can either create an entirely new file by clicking `Create new File` or if you already have created a file you can upload it by clicking `Upload files`.

```{figure} figures/HubUser3_NewFile.PNG
---
width: 80%
align: center
---
Create new file
```

3. In the new window, you can start typing your content. Give your file a name and make sure to use the markdown extension: `file_name.md`. Once you are done, commit the new file to the repository by clicking the green button `Commit changes`.

```{figure} figures/HubUser3_NewFile2.PNG
width: 80%
align: center

Edit new file
```

4. In case you want to make changes to an existing file, navigate to the file in your remote repository. Then click the downward pointing arrow on the very left in the top bar. Select the option `Edit in place`.

```{figure} figures/HubUser3_EditFile.PNG
width: 80%
align: center

Edit in place
```

5. Make your changes in the text editor and when you are ready, commit your changes to the remote repository by clicking on the green `Commit changes` button.

```{figure} figures/HubUser3_EditFile2.PNG
width: 80%
align: center

Commit changes
```

6. In case you added a new file, you also need to include it table of contents of your book! The table of contents is specified in a file called `toc.yml` and it is already included in your repository if you used the teachbooks template. You can edit it and commit the changes in the same manner as with markdown `(file.md)` files.

```{figure} figures/HubUser3_toc.PNG
width: 80%
align: center

Table of contents
```
````

````{tab-item} ... using 'VS Code in your browser'

Using this feature, you can open VS Code in your browser and edit the files in your repository. By doing this, you completely by-pass the need to open (and install) VS Code and GitHub Desktop on your laptop making it the optimal way to quickly fix something. You can make changes to the files already in the repository but you can also upload new files!

```{include} github_dev.md
```

````
`````
``````
```````
````````

````````{tab-item} ... user type 4 ...

```````{tab-set}
``````{tab-item} ... for a brand new version (branch)...

**... by (a) making changes on a single or multiple file(s) <br> 
         (b) selecting changes to be added to the Git-timeline (staging) <br>
         (c) adding changes to the Git-timeline (committing) and <br>
         (d) adding changes to GitLab/GitHub (pushing) with ...**

`````{tab-set}
````{tab-item} ... Git in VS Code

How to make an edit and make a commit using VS Code is demonstrated in the figure below, all steps are elaborated on in the following step-by-step tutorial.
 
```{figure} figures/User4_updated-ezgif.com-optimize.gif
---
name: user4_clone_edit_demo
---
Demonstration, video available [here](https://youtu.be/bThimdDRXTc)
```

1. Make some changes to a file in for example VS Code and save them.

2. Select the files ready to be added to Git-timeline (staging).

    For demonstration purposes, we have created a new Markdown file called `new-chapter.md`, which we want to add to the book. Since this is a new file, Git has no knowledge about its existence yet. I.e., the file is *untracked*. To add new files to our repository, we need to *stage* and *commit* them. To do this, open the Source Control menu in the left side bar. Our new file should appear in this menu:

```{figure} ../images/git-new-file.png

The new file appears in the Source Control menu.
```
    Notice that there is a green letter U placed besides the file, meaning that our file is untracked. To add a file to the *staging area*, click on the + that appears when you hover over the file. 

3. Adding changes to the Git-timeline (committing)

    Next, in the field that says "Message", write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, the menu should now look something like this:

```{figure} ../images/git-file-added.png

The new file has been staged, and we've written a Commit Message.
```
    Now, we are ready to add the changes to the repository. This is done by *committing* the staged changes. To do this, simply press the big, blue "Commit" button in the Source Control menu. 

4. In the bottom left corner, next to the branch name, click the "Synchronize Changes" button (the one that looks like this: 🔄, highlighted in the image below) to push the changes to GitLab.

```{figure} ../images/git-push.png

After committing, click the 🔄 button to push our changes to the remote repository.
```
````
````{tab-item} ... GitHub Desktop

1. Make some changes to a file in for example VS Code and save them.

2. The staging GitHub Desktop assumes you want to stage all files. These files will show up on the left side bar when you open GitHub Desktop. You can unselect some of them (unstaging them) by clicking on the *check*. 

<figure align="center">
    <img src="figures/Stage_GitHubDekstop.PNG" alt="Example Image" width="400">
</figure>

3. Add changes to Git-timeline locally (committing). In the field that says `Summary(Required)`, write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, click the blue button `Commit to repository`.

4. Now we need to add changes to GitHub/GitLab. This is called pushing to the local repository. After committing,  click on `Push origin` in the top bar. 

<figure align="center">
    <img src="figures/Push_GitHubDesktop.PNG" alt="Example Image" width="650">
</figure>
````
`````
``````

``````{tab-item} ... for an existing version (branch)...

**... by (a) regularly obtaining updates from colleagues from GitLab/GitHub (pulling), <br>
         (b) solving potential incompatible changes (merging conflicts), <br>
         (c) making changes on a single / multiple file(s), <br>
         (d) selecting changes to be added to the Git-timeline (staging), <br>
         (e) adding those to the Git-timeline (committing) and <br>
         (f) adding changes to GitLab/GitHub (pushing) with ...**

`````{tab-set}
````{tab-item} ... Git in VS Code

1. If you collaborate with colleagues on your branch, you can get the updates from your colleagues as well by pulling from GitLab/GitHub. This synchronizes the remote repository with your local repository on your machine. On the left side-bar click on the icon that looks like a branch. 

<figure align="center">
    <img src="figures/VSCode_Pull.PNG" alt="Example Image" width="400">
</figure>

By clicking on the 🔄 button, you will pull your colleages' changes.

2. When multiple people work on one chapter, it is possible that conflicts will arise if you and your colleagues have made incompatible changes in the same branch. In that case, when pulling from the remote repository, Git in VS Code will recognize conflicts and help you to solve potential incompatible changes (merging conflicts). Open the files that are marked as conflicitng. 

<figure align="center">
    <img src="figures/Conflicts2.PNG" alt="Example Image" width="650">
</figure>

The figure above shows the conflicts. If you look closely you can see that the last couple of words of the paragraph are different in the main branch than in the branch we were working in. There are a couple of options in the top bar: 

- `Accept Current Change` will keep the change in your branch
- `Accept Incoming Change` will keep the change from the main branch (the branch you are merging into your branch)
- `Accept Both Changes` will retain both paragraphs

Choose one of the options to resolve the merge conflict. You now have updated your work with work from your colleagues and resolved potential conlicts. You are now ready to continue working on the content.

3. Make some further changes to a file in for example VS Code and save them.

4. Select the files ready to be added to Git-timeline (staging) 

For demonstration purposes, we have created a new Markdown file called `new-chapter.md`, which we want to add to the book. Since this is a new file, Git has no knowledge about its existence yet. I.e., the file is *untracked*. To add new files to our repository, we need to *stage* and *commit* them. To do this, open the Source Control menu in the left side bar. Our new file should appear in this menu:

```{figure} ../images/git-new-file.png

The new file appears in the Source Control menu.
```

Notice that there is a green letter U placed besides the file, meaning that our file is untracked. To add a file to the *staging area*, click on the + that appears when you hover over the file. 

5. Adding changes to the Git-timeline (committing)

Next, in the field that says "Message", write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, the menu should now look something like this:

```{figure} ../images/git-file-added.png

The new file has been staged, and we've written a Commit Message.
```
Now, we are ready to add the changes to the repository. This is done by *committing* the staged changes. To do this, simply press the big, blue "Commit" button in the Source Control menu. 

6. In the bottom left corner, next to the branch name, click the "Synchronize Changes" button (the one that looks like this: 🔄, highlighted in the image below) to push the changes to GitLab.

```{figure} ../images/git-push.png

After committing, click the 🔄 button to push our changes to the remote repository.
````
````{tab-item} ... GitHub Desktop

1. If you collaborate with colleagues on your branch, you can get the updates from your colleagues as well by pulling from GitLab/GitHub. This synchronizes the remote repository with your local repository on your machine. Click on `Fetch` in the top bar. Then on the same place, click on 'Pull'. 

<figure align="center">
    <img src="figures/Fetch.PNG" alt="Example Image" width="650">
</figure>

2. When multiple people work on one chapter, it is possible that conflicts will arise if you and your colleagues have made incompatible changes in the same branch. In that case, when pulling from the remote repository, GitHub Desktop will recognize conflicts and help you to solve potential incompatible changes (merging conflicts). 

<figure align="center">
    <img src="figures/Conflicts1.PNG" alt="Example Image" width="650">
</figure>

In this case there are two conflicted files. GitHub Desktop is suggesting to resolve the changes in VS Code (in that case have a look at the section treating VS Code). By clicking on the small downwards arrow you can also solve the conflict directly in GitHub Desktop by choosing the branch of the file you want to keep.

<figure align="center">
    <img src="figures/Conflicts2.PNG" alt="Example Image" width="650">
</figure>

The figure above shows the conflicts. If you look closely you can see that the last couple of words of the paragraph are different in the main branch than in the branch we were working in. There are a couple of options in the top bar: 

- `Accept Current Change` will keep the change in your branch
- `Accept Incoming Change` will keep the change from the main branch (the branch you are merging into your branch)
- `Accept Both Changes` will retain both paragraphs

Choose one of the options to resolve the merge conflict. You now have updated your work with work from your colleagues and resolved potential conlicts. You are now ready to continue working on the content.

3. Make some further changes to a file in for example VS Code and save them.

4. The staging GitHub Desktop assumes you want to stage all files. These files will show up on the left side bar when you open GitHub Desktop. You can unselect some of them (unstaging them) by clicking on the *check*. 

<figure align="center">
    <img src="figures/Stage_GitHubDekstop.PNG" alt="Example Image" width="400">
</figure>

5. Add changes to Git-timeline locally (committing). In the field that says `Summary(Required)`, write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, click the blue button `Commit to repository`.

6. Now we need to add changes to GitHub/GitLab. This is called pushing to the local repository. After committing, click on `Push origin` in the top bar. 

<figure align="center">
    <img src="figures/Push_GitHubDesktop.PNG" alt="Example Image" width="650">
</figure>

````
````{tab-item} ... using 'VS Code in your browser'

Using this feature, you can open VS Code in your browser and edit the files in your repository. This can be really useful for **quick fixes** when you dont want to launch GitHub Dekstop or VS Code. However, we would recommend to limit the use of this feature to quick changes as the other workflows allow for more complex tasks.

```{include} github_dev.md
```

````
`````
``````
```````
````````

````````{tab-item} ... user type 5 ...

```````{tab-set}
``````{tab-item} ... for brand new version (branch)

**... by (a) making changes on a single or multiple file(s) <br> 
         (b) checking changes locally <br>
         (c) selecting changes to be added to the Git-timeline (staging) <br>
         (d) adding changes to the Git-timeline (committing) and <br>
         (e) adding changes to GitLab/GitHub (pushing) with ...**

`````{tab-set}
````{tab-item} ... Git in VS Code

The steps above are demonstrated in the figure below, all steps are elaborated on in the following step-by-step tutorial.
 
```{figure} figures/User5_wholeshabang-ezgif.com-optimize.gif
---
name: user5_demo
---
Demonstration, video available [here](https://youtu.be/2ttjBevkEP8)
```

1. Make some changes to a file in for example VS Code and save them.

2. Once all the changes are made, it can be useful to check the changes locally on your device.<br />
     
By doing that you can preview how it will look on the website. If all the required environments and packages are downloaded, checking changes locally is fairly easy. 

Navigate to the terminal in VS code, located at the bottom of the window or by clicking on `Terminal` in the top bar.
You will firstly need to activate the right environment. Type the following command:

```
conda activate jupyter-book-env
```

(or the environment in which you have installed the `teachbooks` package!)

Then we can build the book locally. Make sure you are in the right repository in VS code and type the following command:

```
teachbooks build <path-to-book>
```

Alternatively:

```
jupyter-book build <path-to-book>
```

Note: use `--all` for the `teachbook` or `jupyter-book` command whenever building a book to make sure the table of contents fully updates. Or alternatively, delete the old `_build` folder before building the new book.

Where book is the name of the folder containing all the files that make up your book. After `teachbooks` is done running you will get the following:

```{figure} figures/buildbook.PNG

Output
```
Paste the last line into your browser to see the updated changes. 

```{Note} 

Sometimes there are problems building the book. It could be that the building requires extensions that are not present in your environment. To prevent issues, make sure to update your environment by routinely updating your packages. You can do this by executing the following line in your environment in the command line.

`pip install -r requirements.txt --upgrade`

```

If your book includes interactive element a webserver is required to host the book. If you want to do this locally, you can make use of (the teachbooks package to start up a local webserver)[setup-local-server]

3. If you are satisfied with your changes, you can select the files ready to be added to Git-timeline (staging) 

For demonstration purposes, we have created a new Markdown file called `new-chapter.md`, which we want to add to the book. Since this is a new file, Git has no knowledge about its existence yet. I.e., the file is *untracked*. To add new files to our repository, we need to *stage* and *commit* them. To do this, open the Source Control menu in the left side bar. Our new file should appear in this menu:

```{figure} ../images/git-new-file.png

The new file appears in the Source Control menu.
```

Notice that there is a green letter U placed besides the file, meaning that our file is untracked. To add a file to the *staging area*, click on the + that appears when you hover over the file. 

4. Adding changes to the Git-timeline (committing)

Next, in the field that says "Message", write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, the menu should now look something like this:

```{figure} ../images/git-file-added.png

The new file has been staged, and we've written a Commit Message.
```
Now, we are ready to add the changes to the repository. This is done by *committing* the staged changes. To do this, simply press the big, blue "Commit" button in the Source Control menu. 

5. Adding changes to GitLab/GitHub (pushing)

In the bottom left corner, next to the branch name, click the "Synchronize Changes" button (the one that looks like this: 🔄, highlighted in the image below) to push the changes to GitLab/GitHub.

```{figure} ../images/git-push.png

After committing, click the 🔄 button to push our changes to the remote repository.
````

````{tab-item} ... GitHub Desktop

1. Make some changes to a file in for example VS Code and save them.

2. Once all the changes are made, it can be useful to check the changes locally on your device.<br />
     
By doing that you can preview how it will look on the website. If all the required environments and packages are downloaded, checking changes locally is fairly easy. 

Navigate to the terminal in VS code, located at the bottom of the window or by clicking on `Terminal` in the top bar.
You will firstly need to activate the right environment. Type the following command:

```
conda activate jupyter-book-env
```

(or the environment in which you have installed the `teachbooks` package!)

Then we can build the book locally. Make sure you are in the right repository in VS code and type the following command:

```
teachbooks build <path-to-book>
```

Alternatively:

```
jupyter-book build <path-to-book>
```

Note: use `--all` for the `teachbook` or `jupyter-book` command whenever building a book to make sure the table of contents fully updates. Or alternatively, delete the old `_build` folder before building the new book.

Where book is the name of the folder containing all the files that make up your book. After `teachbooks` is done running you will get the following:

```{figure} figures/buildbook.PNG

Output
```
Paste the last line into your browser to see the updated changes. 

```{Note} 

Sometimes there are problems building the book. It could be that the building requires extensions that are not present in your environment. To prevent issues, make sure to update your environment by routinely updating your packages. You can do this by executing the following line in your environment in the command line.

`pip install -r requirements.txt --upgrade`

```

If your book includes interactive element a webserver is required to host the book. If you want to do this locally, you can make use of (the teachbooks package to start up a local webserver)[setup-local-server]

3. If you are satisfied with your changes, you can select the files ready to be added to Git-timeline (staging) 

The staging GitHub Desktop assumes you want to stage all files. These files will show up on the left side bar when you open GitHub Desktop. You can unselect some of them (unstaging them) by clicking on the *check*. 

```{figure} figures/Stage_GitHubDekstop.PNG
width: 50%

Staging
```

4. Add changes to Git-timeline locally (committing). In the field that says `Summary (Required)`, write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, click the blue button `Commit to repository`.

5. Now we need to add changes to GitHub/GitLab. This is called pushing to the local repository. After committing, click on `Push Origin` in the top bar.

```{figure} figures/Push_GitHubDekstop.PNG
width: 100%

Push origin
```
````
`````
``````

``````{tab-item} ... for an existing version (branch)

**... by (a) regularly obtaining updates from colleagues from GitLab/GitHub (pulling), <br>
         (b) solving potential incompatible changes (merging conflicts), <br>
         (c) making changes on a single / multiple file(s), <br>
         (d) checking changes locally, <br>
         (e) selecting changes to be added to the Git-timeline (staging), <br>
         (f) adding those to the Git-timeline (committing) and <br>
         (g) adding changes to GitLab/GitHub (pushing) with ...**

`````{tab-set}
````{tab-item} ... Git in VS Code

1. If you collaborate with colleagues on your branch, you can get the updates from your colleagues as well by pulling from GitLab/GitHub. This synchronizes the remote repository with your local repository on your machine. On the left side-bar click on the icon that looks like a branch. 

<figure align="center">
    <img src="figures/VSCode_Pull.PNG" alt="Example Image" width="400">
</figure>

By clicking on the 🔄 button, you will pull your colleages' changes.

2. When multiple people work on one chapter, it is possible that conflicts will arise if you and your colleagues have made incompatible changes in the same branch. In that case, when pulling from the remote repository, Git in VS Code will recognize conflicts and help you to solve potential incompatible changes (merging conflicts). Open the files that are marked as conflicitng. 

<figure align="center">
    <img src="figures/Conflicts2.PNG" alt="Example Image" width="600">
</figure>

The figure above shows the conflicts. If you look closely you can see that the last couple of words of the paragraph are different in the main branch than in the branch we were working in. There are a couple of options in the top bar: 

- `Accept Current Change` will keep the change in your branch
- `Accept Incoming Change` will keep the change from the main branch (the branch you are merging into your branch)
- `Accept Both Changes` will retain both paragraphs

Choose one of the options to resolve the merge conflict. You now have updated your work with work from your colleagues and resolved potential conlicts. You are now ready to continue working on the content.

3. Make some further changes to a file in for example VS Code and save them.

4. Once all the changes are made, it can be useful to check the changes locally on your device in order to see how it will look on the website. If all the required environments and packages are downloaded, checking changes locally is fairly easy! 

Navigate to the terminal in VS code, located at the bottom of the window or by clicking on `Terminal` in the top bar.

You will firstly need to activate the right environment. Type the following command:

`conda activate jupyter-book-env`

(or the environment in which you have installed the TeachBooks package)

Then we can build the book locally. Make sure you are in the right repository in VS code and type the following command:

```
teachbooks build <path-to-book>
```

Alternatively:

```
jupyter-book build <path-to-book>
```

Note: use `--all` for the `teachbook` or `jupyter-book` command whenever building a book to make sure the table of contents fully updates. Or alternatively, delete the old `_build` folder before building the new book.

Where book is the name of the folder containing all the files that make up your book. After `teachbooks` is done running you will get the following:

```{figure} figures/buildbook.PNG

Output
```
Paste the last line into your browser to see the updated changes. 

```{Note} 

Sometimes there are problems building the book. It could be that the building requires extensions that are not present in your environment. To prevent issues, make sure to update your environment by routinely updating your packages. You can do this by executing the following line in your environment in the command line.

`pip install -r requirements.txt --upgrade`

```

If your book includes interactive element a webserver is required to host the book. If you want to do this locally, you can make use of (the teachbooks package to start up a local webserver)[setup-local-server]

5.  Select the files ready to be added to Git-timeline (staging) 

For demonstration purposes, we have created a new Markdown file called `new-chapter.md`, which we want to add to the book. Since this is a new file, Git has no knowledge about its existence yet. I.e., the file is *untracked*. To add new files to our repository, we need to *stage* and *commit* them. To do this, open the Source Control menu in the left side bar. Our new file should appear in this menu:

```{figure} ../images/git-new-file.png

The new file appears in the Source Control menu.
```
Notice that there is a green letter U placed besides the file, meaning that our file is untracked. To add a file to the *staging area*, click on the + that appears when you hover over the file. 

6. Adding changes to the Git-timeline (committing)

Next, in the field that says "Message", write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, the menu should now look something like this:

```{figure} ../images/git-file-added.png

The new file has been staged, and we've written a Commit Message.
```
Now, we are ready to add the changes to the repository. This is done by *committing* the staged changes. To do this, simply press the big, blue "Commit" button in the Source Control menu. 

7. In the bottom left corner, next to the branch name, click the "Synchronize Changes" button (the one that looks like this: 🔄, highlighted in the image below) to push the changes to GitLab.

```{figure} ../images/git-push.png

After committing, click the 🔄 button to push our changes to the remote repository.
````
````{tab-item} ... GitHub Desktop

1. If you collaborate with colleagues on your branch, you can get the updates from your colleagues as well by pulling from GitLab/GitHub. This synchronizes the remote repository with your local repository on your machine. Click on `Fetch` in the top bar. Then on the same place, click on 'Pull'. 

<figure align="center">
    <img src="figures/Fetch.PNG" alt="Example Image" width="650">
</figure>

2. When multiple people work on one chapter, it is possible that conflicts will arise if you and your colleagues have made incompatible changes in the same branch. In that case, when pulling from the remote repository, GitHub Desktop will recognize conflicts and help you to solve potential incompatible changes (merging conflicts). 

<figure align="center">
    <img src="figures/Merge_Conflict_GitHubDesktop2.PNG" alt="Example Image" width="400">
</figure>

In this case there are two conflicted files. GitHub Desktop is suggesting to resolve the changes in VS Code (in that case have a look at the section treating VS Code). By clicking on the small downwards arrow you can also solve the conflict directly in GitHub Desktop by choosing the branch of the file you want to keep.

Choose one of the options to resolve the merge conflict. You now have updated your work with work from your colleagues and resolved potential conlicts. You are now ready to continue working on the content.

3. Make some further changes to a file in for example VS Code and save them.

4. Once all the changes are made, it can be useful to check the changes locally on your device in order to see how it will look on the website. If all the required environments and packages are downloaded, checking changes locally is fairly easy! 

Navigate to the terminal in VS code, located at the bottom of the window or by clicking on `Terminal` in the top bar.

You will firstly need to activate the right environment. Type the following command:

`conda activate jupyter-book-env`

(or the environment in which you have installed the TeachBooks package)

Then we can build the book locally. Make sure you are in the right repository in VS code and type the following command:

```
teachbooks build <path-to-book>
```

Alternatively:

```
jupyter-book build <path-to-book>
```

Note: use `--all` for the `teachbook` or `jupyter-book` command whenever building a book to make sure the table of contents fully updates. Or alternatively, delete the old `_build` folder before building the new book.

Where book is the name of the folder containing all the files that make up your book. After `teachbooks` is done running you will get the following:

```{figure} figures/buildbook.PNG

Output
```
Paste the last line into your browser to see the updated changes. 

```{Note} 

Sometimes there are problems building the book. It could be that the building requires extensions that are not present in your environment. To prevent issues, make sure to update your environment by routinely updating your packages. You can do this by executing the following line in your environment in the command line.

`pip install -r requirements.txt --upgrade`

```

If your book includes interactive element a webserver is required to host the book. If you want to do this locally, you can make use of (the teachbooks package to start up a local webserver)[setup-local-server]

5. The staging GitHub Desktop assumes you want to stage all files. These files will show up on the left side bar when you open GitHub Desktop. You can unselect some of them (unstaging them) by clicking on the *check*. 

<figure align="center">
    <img src="figures/Stage_GitHubDekstop.PNG" alt="Example Image" width="400">
</figure>

6. Add changes to Git-timeline locally (committing). In the field that says `Summary(Required)`, write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, click the blue button `Commit to repository`.

7. Now we need to add changes to GitHub/GitLab. This is called pushing to the local repository. After committing, click on `Push origin` in the top bar. 

<figure align="center">
    <img src="figures/Push_GitHubDesktop.PNG" alt="Example Image" width="650">
</figure>   
````
````{tab-item} ... using 'VS Code in your browser'

Using this feature, you can open VS Code in your browser and edit the files in your repository. This can be really useful for **quick fixes** when you dont want to launch GitHub Dekstop or VS Code. However, we would recommend to limit the use of this feature to quick changes as the other workflows allow for more complex tasks.

```{include} github_dev.md
```

````
`````
``````
```````
````````
`````````
