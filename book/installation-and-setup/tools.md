# Choose URLs and tools

```{admonition} User types
:class: tip
This page is useful for user type 4-5.
```

The setup of tools and URLs is dependent on agreements you've made on [collaboration](./collab.md).

## Collaboration in readme
Provide explanation on how you organize the book-editing and how you'd like to receive feedback in both the readme as the published book. The use of the [issue button](https://jupyterbook.org/en/stable/basics/repository.html#add-a-button-to-open-issues) is advised for the published book.

## Branches for separate versions
We recommend using at least two separate branches, one which is released to students, the other one for development. If you're planning adapting the book every year, you should set up your branches in such a way that students will always receive the version they should expect.

Firstly, create a release branch which contains the students' version of this year. This branch could be named `release`, `main`, or `<current academic year>`. It is recommended to set this branch as the `PRIMARY BRANCH` when using the [GitHub workflow](gh-workflow-settings). This ensures that students are redirected to a consistent URL, even when new versions of the book are added later. If you plan on maintaining only one public version, it is advisable to set `BEHAVIOR_PRIMARY` from the default `redirect` to `copy`. This ensures that the primary branch is copied to the root, making the URL more compact.

Next, establish a development branch that contains all the new content combined but not yet published to students. This branch could be named `dev` or `main`. Using `dev` is recommended if you prefer the default branch to be the most recent published version, as `main` is commonly expected to be the default branch.

Additionally, allow the creation of branches during the editing process. As long as `BRANCHES_TO_DEPLOY` is set to the default `*`, all branches will be built, enabling fellow editors to review their own and each other's versions online. Periodically, it is beneficial to review the list of branches and delete any that have been merged but not deleted.

Eventually, create branches for previous study years, each containing that year's version of the book. These branches could be named `<academic year>`, which will also be reflected in their URLs. Add these branches to the list of `BRANCHES_ARCHIVED` when using the [GitHub workflow](gh-workflow-settings) to include a banner on the page indicating its archived state.

We advise  you to enable two options in the general repository setting regarding pull requests in GitHub:
- Enable `Always suggest updating pull request branches`, suggesting a merge from the default branch into any separate branch before merging into main.
- Enable `Automatically delete head branches` to delete branches after they are merged (you'll still be able to restore those).

Lastly, add a readme explaining the way you organized branches.

## Protect branches

To ensure the integrity of your book's content, it is crucial to set up protected branches in both GitHub and GitLab. Protected branches prevent accidental changes and ensure that only authorized modifications are made. In GitHub, you can configure branch protection rules by navigating to the repository settings, selecting "Branches," and then adding branch protection rules for the branches you want to protect. Similarly, in GitLab, you can protect branches by going to the repository settings, selecting "Repository," and then configuring the branch protection settings.

Once the branches are protected, it is advised to assign appropriate permissions to team members based on their roles. In GitHub, you can manage permissions by navigating to the repository settings, selecting "Manage access," and then inviting collaborators with specific roles such as "Admin," "Write," or "Read." In GitLab, permissions can be managed by going to the project settings, selecting "Members," and then adding users with roles like "Maintainer," "Developer," or "Reporter."

Additionally, it is advisable to document the branch protection strategy and the assigned permissions in the readme file. This documentation should explain the rationale behind the branch protection rules and provide clear instructions on how team members can request access or permission changes. By doing so, you create a transparent and organized workflow that facilitates collaboration and minimizes the risk of unauthorized changes. We would advise a [ruleset](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository):
- Bypassable by repository admins
- Targeting default branch
- Restrict deletions
- Require a pull request before merging with 1 required approval
- Block force pushes

## GitHub vs GitLab
Choosing between GitHub and GitLab depends on multiple criteria. GitHub provides more functionalities, but you might prefer the TU Delft-closed GitLab system.

### Book URL
Github allows you to host your book on the GitHub server using GitHub pages (to be recognized by the `<organization/username>.github.io/<book>` url, for example the [template book](https://teachbooks.github.io/template/)), which takes all the steps of hosting out of your hands. Next to GitHub-provided URLs, you can set up a custom owned URL, although this requires some additional skills on a domain which you should own. 

If you're part of TU Delft, you can put your book in the [TUDelft-Book organisation](https://github.com/tudelft-books), which allows you to host your book at `oit.tudelft.nl/<book>`. If you've a private book which is part of the [GitHub Enterprise TU Delft](https://github.com/enterprises/tudelft) and is using SSO, a random url is generated `<random>.github.io/<book>`. For courses we advise you to create a organization with the course name so that the URL represent that course.

On TU Delft's GitLab you need a webserver, which was offered by TeachBooks in the past (to be recognized by the url `teachbooks.tudelft.nl/<book>`), and is still offered by the TU Delft OIT team (to be recognized by the url `interactivetextbooks.tudelft.nl/<book>`).

### Real-time editing book
Editing the book can happen both locally as online on GitHub/GitLab. If done locally, the book can be generated and viewed locally too (typically takes around 1 minute) but this requires you to be at least user type 4 or 5 depending on the book content. The built book can also be viewed online separate from the released version.

On GitHub we developed a [automatic process which builds the book and publishes it online](../external/deploy-book-workflow/README.md) in a very flexible way (publication of multiple version of the book, insights in book building errors, parallel so fast build, custom urls in subdirectories). For a private repository, there is an extensive but limited amount of actions-minutes required for published your book. If this proves to be a limit, consider applying for [Teacher benefits](https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-education-for-teachers/about-github-education-for-teachers#github-education-features-for-teachers) or joining the [GitHub Enterprise of TU Delft](https://github.com/enterprises/tudelft).

On GitLab a webserver is required to process book-changes online. Both we and other people at TU Delft have a simplistic workflow which can be used when you're set up on those Git environments and webservers. This simplistic workflow doesn't build all branches, is not easily adaptable, doesn't cache environments, doesn't give a visual summary, and doesn't allow for parallel processes (for every build a runner needs to be assigned for which there's typically only one available). If you want to use GitLab but still want to make use of the GitHub workflow, you can [mirror your repository to GitHub](https://docs.gitlab.com/ee/user/project/repository/mirror/push.html#set-up-a-push-mirror-from-gitlab-to-github). For the TU Delft OIT webserver you’re required to publish your book more officially, it cannot be used for viewing your book online in an active editing-phase since constant copyright checks have to be performed. The amount of computing power available is dependent on how you set the server yourself.

### Setting up book repository and website
On GitHub you can start right away with a git environment and online book using our [template](../external/template/README.md).

On GitLab you can set up your own git environment, but you need to be given access by [TU Delft OIT](mailto:Interactive-textbooks@tudelft.nl) to view your build book online.

### Book access with SSO
When you’re releasing your book on a server on which you're in control (connected to GitLab or GitHub), you can set up SSO login for visitors of the website. In the past, this was arranged for for TU Delft employees at teachbooks.tudelft.nl. However, this is depreciated.

If you want the same functionality with GitHub pages, your book should be part of the [GitHub Enterprise of TU Delft](https://github.com/enterprises/tudelft). This SSO login is a bit different as you're required to give access to specific accounts. Furthermore, the url of you're book on GitHub pages is a random one, so you might consider using a custom URL.

### Access to source code

Both GitLab and GitHub allow for extensive options for visibility of the source code, both private, public or internally. On GitHub, public allows for collaboration with anyone. For SSO login, your book should be part of the [GitHub Enterprise of TU Delft](https://github.com/enterprises/tudelft). If you'd like a private repo on GitHub, apply for a GitHub Team (free as a teacher as described in the [github documentation](https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-education-for-teachers/about-github-education-for-teachers#github-education-features-for-teachers)) to make use of GitHub pages (for public repos GitHub pages is not restricted).

The TU Delft GitLab requires SSO login for editing the book. Although this is useful for TU Delft employees, it limits the collaboration with people outside of TU Delft.

### Book size limits
In GitLab, an artifact (the book export) can have a maximum size of 150 MB. In GitHub, the total GitHub pages may not exceed 1 GB (including all branches)

### Integration with GitHub Desktop
GitHub has a nice integration with the [GitHub Desktop application](git-setup_local.md). For GitLab it works as well, but has less functionality.

### Intergration with Utteranc.es
[Utteranc.es](../basic-features/utterances.md) requires a GitHub repository to host the discussions. If you're using a GitLab repository, you need a separate GitHub repository and the discussions and book content is not at the same place.

### Summary
Here's a table summarizing the information:
|  | GitHub   | TU Delft GitLab      |
|--|----------|-------------|
| Book url  | GitHub pages (`<organization/username>.github.io/<book>`), for TU Delft books a custom URL (`oit.tudelft.nl/<book>`), for private books on TU Delft GitHub Enterprise with SSO a random URL (`<random>.github.io/<book>`), or custom url `<anything>.<anything>/<book>`> 🌐         | TU Delft OIT (`interactivetextbooks.tudelft.nl/<book>`) 🎓 |
| Real-time book editing | Automated and flexible (multiple version of the book, building error insights, fast, custom urls)  🚀   | Automated but simplistic (not easily adaptable, no caching environments, no visual summaries, no parallel processes) 🛵 For TU Delft OIT: restricted adaptations because of copyright checks 🚫   |
| Setting up book website | Immediate and automated with [template](../external/template/README.md) ⚡️         | Manual setup on personal webserver, or access required by TeachBooks or TU Delft OIT  🚧    |
| Book access with SSO | Only available for GitHub pages on GitHub Enterprise of TU Delft 🎓, optional with custom URL  ✅ | Optional  ✅          |
| Access to source code | Private (if part of organization linked to educational account) /public / internally TU Delft (on GitHub Enterprise of TU Delft) 👥   | Private / public (read-only) / internally TU Delft, editing requires requires SSO login  👥  👀 |
| Book size limits | 1 GB for all branches 📚 | 150 MB per book 📕 |
| GitHub Desktop | Well integrated 😎 | Basic integration 🙂 |
| Utteranc.es | Can be linked to same repository 🏷️ | Requires GitHub repository next to GitLab repository 🏷️🏷️|

If you have doubt about this choice, we advise you to start on GitHub. Moving/duplicating your content to GitLab or hosting to a custom URL is always possible at a later stage.
