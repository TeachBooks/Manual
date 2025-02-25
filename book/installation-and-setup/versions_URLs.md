# Publish version on separate (fixed) URLs

As soon as you have different versions online, you have to make a decision about URLs. Using the [](../external/deploy-book-workflow/README.md), you can release the different version of your book all under the same root URL.

If you plan on maintaining only one public version, it is advisable to set `BEHAVIOR_PRIMARY` from the default `redirect` to `copy`. This ensures that the primary branch is copied to the root, making the URL more compact.

To share the built book / website of old versions for your book on GitHub you have a few options:
- create a branch for each version. When doing this, [the GitHub workflow](../external/deploy-book-workflow/README.md) will build it on GitHub pages. Here's a few tips:
  - It's advised to use the version as branch name. In case of versions per academic year, you can just name each branch to the current academic year,  this leads to the URL with the same name. In that case.
  - It is recommended to update the primary branch as the `PRIMARY BRANCH` when using the [GitHub workflow](gh-workflow-settings) whenever a new version is considered to be the most primary one. This ensures that readers are redirected to a consistent URL, even when new versions of the book are added later.
  - Eventually, you can add old branches to the list of `BRANCHES_ARCHIVED` when using the [GitHub workflow](gh-workflow-settings) to include a banner on the page indicating its archived state. Alternatively, you can add a banner manually to `_config.yml`.
  - If you're using tags (as will be explained in [later](./versioning_changelog.md)), you can create a branch from a tag locally by running: `git branch <new_branch name> <tag/version>`.
  - If you have many version of the book, at some point you might reach the 1 GB GitHub Pages limit. This is only expected for extremely large books with a lot of non-text-based (binary) content. To prevent going over that limit, store large content not used for building the website (like images) on an external server. This can be another GitHub repository or a (paid) object store.
  - An example can be found in the book 'Engineering Systems Optimization': it has two versions for readers online, the [2023-version](https://oit.tudelft.nl/CME4501/2023) and the [2024-version](https://oit.tudelft.nl/CME4501/2024), recognizable by the URL. Both versions originate from their respective branches in the [GitHub-repository](https://github.com/TUDelft-books/CME4501)
- add a zip of the built book to the release in GitHub as binary asset. This requires readers to download the zip and open the html files locally, but doesn't require you to host it somewhere. This zip can be easily downloaded as an artifact from [the GitHub action](../external/deploy-book-workflow/README.md). An example can be found [here](https://github.com/TUDelft-books/CME4501/releases/tag/v2024.1.0). Note that this requires you to set up tags and releases, as explained in [](versioning_changelog.md)
- Use [Read the Docs](../features/pull_request_build.md) to build a website for all your branches, forks and tags as Read the docs doesn't have a 1 GB limit, but has a very different URL structure and the free community version has advertisement. In case you're using tags and releases, refer to the URL of this built from your GitHub release to make sure that GitHub visitors find their way to Read the Docs.

If you have your own webserver, you can publish each version on it manually.

Don't forget to explain how you organize your URLs and old versions in your README and eventually in the book itself too with a sentence like this (as can be seen in [this book](https://oit.tudelft.nl/CME4501/2024/intro.html) too):

> This is the `<version_number>`-version of this book. Go to `<link to root URL>` to view the most recent version of this book, or adapt the year in `<link to root URL>/<year>` to the year when you took the course.

