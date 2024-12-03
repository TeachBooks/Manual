# User types

Different types of users will interact with the website or the Jupyter Books differently and will therefore need to know more or less about the composition of the book. For now we will differentiate 5 types of users.

1. **Students providing feedback via the book website**.<br>  
    <img src="figures/type 1.jpg" alt="Example Image" align="right" width="130" style="margin: 20px;"><br>There are multiple tools of providing feedback in the built book:<br>a) using the issue button in the top-right corner to directly create issues visible to the editor team.<br>b) Using the [hypothesis](https://jupyterbook.org/en/stable/interactive/comments/hypothesis.html)-extension which allows public/private highlighting and annotating parts of the book. Using the [Utterances](https://jupyterbook.org/en/stable/interactive/comments/utterances.html)-extension which allows commenting on pages for books which are hosted on GitHub visible for everyone. Those comments are converted to issues on GitHub for the editors to handle.

2. **Colleague providing feedback on a draft website**. <br>
    In a similar manner as students, colleages and team members can leave content-related comments on the website through extensions or GitHub/GitLab features (e.g., Issues). In this way, multiple teachers can give input in the draft of the textbook and course material without requiring a complete understanding of Jupyter Books or GitLab/GitHub. The responsible teacher (or student assistants) can then make adaptations to the book as recommended by their colleagues.

3. **Colleague making adjustments via the browser**. <br>
    This type of user requires only very basic knowledge in GitLab/GitHub in order to make changes to the website themselves. Most iportantly, there is no need to install any software! Making adjustments to a file only requires the user to be able to login into GitLab/GitHub and edit .md or .ipynb files. The changes can be done directly in the main or release branch, or, if unsure, a new branch can be used for the changes then the set-up and merging can be taken care of by someone more familiar in GitLab/GitHub. Files can be edited individually or many-at-a-time using the VS Code-style browser application.

4. **Colleague making adjustments locally**. <br>
    User 4 is a hybrid between type 3 and 5. Basically this user is making changes by editing the .md files locally using, for example, VS Code. Therefore, this user requires a little bit more knowledge on git (think of pulling and pushing changes) but their main focus remains to make adjustments to the content of the book by editing .md files whereas user type 5 has more knowledge to make changes to python files the book as well. This user can build the book online and therefore does not need to have special software installed besides a text editor (e.g., Python is not required).

5. **Colleague making adjustments and incorporating them in the book locally**. <br>
    <img src="figures/type 5.jpg" alt="Example Image" align="right" width="120" style="margin: 20px;"><br>This user has more knowledge in GitLab/GitHub than the previous user and can take care of branching and merging directly. They know how to work with software for editing .md and .ipynb files. They can use the Deploy Book Workflow online to view their changes in the book and coordinate peer review, and/or build the book locally.

<br style="clear:both;">

```{Note}

At this point, you might already be trying to see which user type fits you the best. We are aware that the lines between user types can be a bit blurry, especially between type 3, 4 and 5. In case you're (1) a user type 3 and want to dabble in git or (2) a user type 4/5 and want to make some quick edits with only a few clicks, then you might consider using a more advanced online editor in GitHub (GitHub Dev) as explained further on in [Collaborative book-editing > Edit](../workflows/edit_book.md) > User type 3 > GitHub > Using VS Code in your browser.
```
