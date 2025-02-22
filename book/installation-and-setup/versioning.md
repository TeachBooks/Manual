# Versioning and URLs

```{admonition} User types
:class: tip
This page is useful for user type 4-5.
```

Online books can be easily updated, however, this might confuse readers. Therefore, it's good practice to be aware of this and, where needed, provide explicit version to the readers. It's recommended to do this in multiple ways, which can be combined:
- Publish versions on separate (fixed) URLs
- Use some sort of semantic versioning
- Keep both source code as (export of) websites of archived versions

## Publish version on separate (fixed) URLs
When making books for education, typically your book can change substantially for consequential academic years. If there's many people working on different parts of the book and material is staged for publication to stduents, we recommend using at least two separate branches, one which is released to students, the other one for development.  Using the [](../external/deploy-book-workflow/README.md), it's very easy to share multiple versions of your book on the same root-URL. 

Firstly, create a release branch which contains the students' version of this year. This branch could be named `release`, `main`, or `<current academic year>`. It is recommended to set this branch as the `PRIMARY BRANCH` when using the [GitHub workflow](gh-workflow-settings). This ensures that students are redirected to a consistent URL, even when new versions of the book are added later. If you plan on maintaining only one public version, it is advisable to set `BEHAVIOR_PRIMARY` from the default `redirect` to `copy`. This ensures that the primary branch is copied to the root, making the URL more compact.

Next, establish a development branch that contains all the new content combined but not yet published to students. This branch could be named `dev`, `main`, `<current academic year>-draft`. Using `dev` is recommended if you prefer the default branch to be the most recent published version, as `main` is commonly expected to be the default branch.

Additionally, allow the creation of branches during the editing process. As long as `BRANCHES_TO_DEPLOY` is set to the default `*`, all branches will be built, enabling fellow editors to review their own and each other's versions online. Periodically, it is beneficial to review the list of branches and delete any that have been merged but not deleted.

Eventually, create branches for previous study years, each containing that year's version of the book. These branches could be named `<academic year>`, which will also be reflected in their URLs. Add these branches to the list of `BRANCHES_ARCHIVED` when using the [GitHub workflow](gh-workflow-settings) to include a banner on the page indicating its archived state.

We advise  you to enable two options in the general repository setting regarding pull requests in GitHub:
- Enable `Always suggest updating pull request branches`, suggesting a merge from the default branch into any separate branch before merging into main.
- Enable `Automatically delete head branches` to delete branches after they are merged (you'll still be able to restore those).

Lastly, add a readme explaining the way you organized branches.

## TO BE WRITTEN