**Selecting changes to be added to the Git-timeline (staging)**

For demonstration purposes, we have created a new Markdown file called `new-chapter.md`, which we want to add to the book. Since this is a new file, Git has no knowledge about its existence yet. I.e., the file is *untracked*. To add new files to our repository, we need to *stage* and *commit* them. To do this, open the Source Control menu in the left side bar. Our new file should appear in this menu:

```{figure} ../images/git-new-file.png
---
width: 100%

---
The new file appears in the Source Control menu.
```
Notice that there is a green letter U placed besides the file, meaning that our file is untracked. To add a file to the *staging area*, click on the + that appears when you hover over the file. 

**Adding changes to the Git-timeline (committing)**

Next, in the field that says "Message", write a short description of the changes you have made. This message is what is called the *Commit Message*. After we've done this, the menu should now look something like this:

```{figure} ../images/git-file-added.png
---
width: 100%

---
The new file has been staged, and we've written a Commit Message.
```

Now, we are ready to add the changes to the repository. This is done by *committing* the staged changes. To do this, simply press the big, blue "Commit" button in the Source Control menu. 

**Adding changes to GitLab/GitHub (pushing)**

In the bottom left corner, next to the branch name, click the "Synchronize Changes" button (the one that looks like this: 🔄, highlighted in the image below) to push the changes to GitLab/GitHub.

```{figure} ../images/git-push.png
---
width: 100%

---
After committing, click the 🔄 button to push our changes to the remote repository.
```