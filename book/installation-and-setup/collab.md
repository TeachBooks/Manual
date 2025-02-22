# Organize editing team, collaboration and visibility

```{admonition} User types
:class: tip
This page is useful for user type 4-5.
```

## Roles and responsibilities
To ensure smooth collaboration, it is essential to define the roles and responsibilities within your team. Firstly, designate who will be in charge of team organization ('administrators') who should be at least user type 4. Additionally, assign 'maintainers' responsible for combining content, also requiring at least user type 4. 'Editors' should be identified for editing and reviewing content, requiring at least user type 3.

Finally, ensure that team members identify themselves according to the user types. It is crucial to have at least one user type 4 or 5 on the team. While this role can be filled by a teaching assistant (TA), it is recommended that one of the teachers is also comfortable with this user type to provide adequate support and oversight.

## Review process
Furthermore, establish a clear editing and review process.

For the editing process, establish some practical rules on whether to use issues, branches and forks for adding content, fixing typos or making other changes. Furthermore, it can help to write down when you expect (draft) merge/pull requests and how to use the assign and review options in GitHub/GitLab. It is advisable to have at least a maintainer review each piece of content to maintain quality and consistency. Provide explanation on how you organize the book-editing and how you'd like to receive feedback in both the readme as the published book. The use of the [repository button {fa}`github`, suggest edit {fa}`pencil` and issue button {fa}`lightbulb`](https://jupyterbook.org/en/stable/basics/repository.html) is advised.

## Book previews of contributions
Using the [](../external/deploy-book-workflow/README.md), it's very easy to show a preview of the changes for branches within the same repository. Using [](../features/pull_request_build.md) you allow previews of changes for forks of your repository too.

Add the way you organized branches and builds in your README.

## Protect branches

To ensure the integrity of your book's content, it is crucial to set up protected branches in both GitHub and GitLab. Protected branches prevent accidental changes and ensure that only authorized modifications are made. In GitHub, you can configure branch protection rules by navigating to the repository settings, selecting "Branches," and then adding branch protection rules for the branches you want to protect. Similarly, in GitLab, you can protect branches by going to the repository settings, selecting "Repository," and then configuring the branch protection settings.

Once the branches are protected, it is advised to assign appropriate permissions to team members based on their roles. In GitHub, you can manage permissions by navigating to the repository settings, selecting "Manage access," and then inviting collaborators with specific roles such as "Admin," "Write," or "Read." In GitLab, permissions can be managed by going to the project settings, selecting "Members," and then adding users with roles like "Maintainer," "Developer," or "Reporter."

Additionally, it is advisable to document the branch protection strategy and the assigned permissions in the readme file. This documentation should explain the rationale behind the branch protection rules and provide clear instructions on how team members can request access or permission changes. By doing so, you create a transparent and organized workflow that facilitates collaboration and minimizes the risk of unauthorized changes. We would advise a [ruleset](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository):
- Bypassable by repository admins
- Targeting default branch
- Restrict deletions
- Require a pull request before merging with 1 required approval
- Block force pushes

## Private, internally or public
Choose whether you want to share your source code and built book privately, internally or publicly. In any case, you need to obey copyright-rules. We advise public repositories and books in line with a vision on open education.

## For TU Delft employees: publishing via TU Delft OPEN interactive textbooks
Decide on whether or not to publish your book via TU Delft OPEN interactive textbooks. Publishing will give you a copyright check, ISBN or DOI number, and registration in several shared databases but limits the amount of changes you can make to your book: for substantial changes a new published version is needed with an updated copyright checks. Small changes like typos can always be made, which are processed in the published version every hour.
In case of editing a book for a course during that actual course and/or your book has limited value outside your course's content, we advise you only to publish an archived version of your book whenever the academic year is over.