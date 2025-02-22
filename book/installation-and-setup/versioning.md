# Versioning and URLs

> This page reuses adapted CC BY 3.0 content from Tom Preston-Werner {cite:t}`semver`. {fa}`quote-left`{ref}`Find out more here.<external_resources>`

```{admonition} User types
:class: tip
This page is useful for user type 4-5.
```

Online books can be easily updated, however, this might confuse readers. Therefore, it's good practice to be aware of this and, where needed, provide explicit version to the readers. It's recommended to do this in multiple ways, which can be combined:
- Publish versions on separate (fixed) URLs
- Use some sort of semantic versioning with tags
- Keep both source code as (export of) websites of all versions
- Publishing your book more officially

## Publish version on separate (fixed) URLs
When making books for education, typically your book can change substantially for consequential academic years. Using the [](../external/deploy-book-workflow/README.md), you can release the different version of your book all under the same root URL. If you name each students' version of each year to the `<current academic year>`, the students URL includes that academic year too. It is recommended to yearly update the current academic year branch as the `PRIMARY BRANCH` when using the [GitHub workflow](gh-workflow-settings). This ensures that students are redirected to a consistent URL, even when new versions of the book are added later. Eventually, you can add old branches to the list of `BRANCHES_ARCHIVED` when using the [GitHub workflow](gh-workflow-settings) to include a banner on the page indicating its archived state.

If you plan on maintaining only one public version, it is advisable to set `BEHAVIOR_PRIMARY` from the default `redirect` to `copy`. This ensures that the primary branch is copied to the root, making the URL more compact.

Don't forget to explain how you organize these URLs in your README and eventually in the book itself too with a sentence like this:

> This is the 2024-2025-version of this book. Go to `<link to root URL>` to view the most recent version of this book, or adapt the year in `<link to root URL>/<year>` to the year when you took the course.

If you've many version of the book, at some point you might reach the 1 GB GitHub Pages limit. This is only expected for extremely large books with a lot of non-text-based (binary) content. To prevent going over that limit, store large content not used for building the website (like images) on an external server. This can be another GitHub repository or a (paid) object store

## Semantic versioning
Semantic versioning is used extensively in the world of software management to deal with versions {cite:p}`semver`. This is more suited than the more traditional way of versioning paper books (version 1, 2, etc.), because of the amount of edits which online books allow. There's [guidelines](https://semver.org/) about how to use a 'x.y.z' version numbers for software, for which we propose the following alternative for books:

1. A normal version number MUST take the form X.Y.Z where X, Y, and Z are non-negative integers, and MUST NOT contain leading zeroes. X is the major version or yearly version, Y is the minor version, and Z is the patch version. Each element MUST increase numerically. For instance: 1.9.0 -> 1.10.0 -> 1.11.0. or 2025.9.0 -> 2025.10.0 -> 2025.11.0
2. Once a versioned book has been released, the contents of that version MUST NOT be modified. Any modifications MUST be released as a new version.
3. Major version zero (0.y.z) is for initial development. Anything MAY change at any time. The book content should not be shared with readers as it's not considers as stable.
4. Version 1.0.0 defines the first released book. The way in which the version number is incremented after this release should be explained in the README of the source code and in the book itself.
5. Patch version Z (x.y.Z | x > 0) MUST be incremented if a small change is made which should be communicated to the reader in both the source code and in the book itself. If the small change is not crucial (like a simple typo), you might consider not defining it as a new version but combining it with other changes in the next version.
6. Minor version Y (x.Y.z | x > 0) MUST be incremented if a big change / addition is made to the book. It MUST be communicated in both the source code and in the book itself. It MAY include patch level changes. Patch version MUST be reset to 0 when minor version is incremented.
7. Major version X (X.y.z | X > 0) MUST be incremented if a substantial restructure is made to the book. A new academic year is a great example for this. It MUST be communicated in both the source code and in the book itself. It MAY also include minor and patch level changes. Patch and minor versions MUST be reset to 0 when major version is incremented.
8. Precedence refers to how versions are compared to each other when ordered.
   1. Precedence MUST be calculated by separating the version into major, minor, patch and pre-release identifiers in that order.
   2. Precedence is determined by the first difference when comparing each of these identifiers from left to right as follows: Major, minor, and patch versions are always compared numerically. Example: 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1.

### Changelog
To communicate changes, we advise creating a changelog in the book. The [template](https://github.com/TeachBooks/template/blob/main/book/changelog.md) contains an example:

```md
# Changelog

## `<latest version>`: `<date>`
- `<Added/modified/deleted>` [](`<relative link to changed file>`)
- ...
- Full Changelog: `[<previous version>...<current version>](<link to diff as provided by GitHub>)'

## `<previous version>`: <...>
- <...>

<...>
```

### Implement tags and releases
Tags can be added to your source code by adding the version number as a tag to a specific commit. You can do so only locally. In GitHub Desktop this is done by clicking 'Create Tag...` for a specific commit in the History tab.

```{figure} figures/tags.png
---
width: 300px
align: center
---

```

Once the tags is pushed to GitHub/GitLab. You can create a release of the version by clicking `Release` on the `Code` page of your repository. There you can select a tag and generate release notes. It's recommended to add the relevant part of the changelog too. An example can be found [here](https://github.com/CIEM5000-2025/book/releases/tag/v2025.2.0)

## Keep source code and website of all versions
Although you might only want to share the most recent version of the book with your readers, it might be useful too the have the source code and website of older versions somewhere too.

Git allows you to go back in the git history to the source code of old versions. To make this as easy as possible for readers, use tags and releases instead of having the readers scroll through a long list of (not alway very descriptive) commit descriptions.

To share the built book / website of old versions for your book on GitHub you've a few options:
- add a zip of the built book to the release in GitHub as binary asset. This requires readers to download the zip and open the html files locally, but doesn't require you to host it somewhere. This zip can be easily downloaded as an artifact from [the GitHub action](../external/deploy-book-workflow/README.md). An example can be found [here](https://github.com/TUDelft-books/CME4501/releases/tag/v2024.1.0)
- create a branch for each tag. When doing this, [the GitHub workflow](../external/deploy-book-workflow/README.md) will build it on GitHub pages. It's advised to use the version as branch name. You can create a branch from a tag locally by running: `git branch <new_branch name> <tag/version>`. Note that when you've many version and a large book, this approach might easily fill up your 1 GB GitHub pages limit.
- Use [Read the Docs](../features/pull_request_build.md) to build a website for all your tags. Refer to the URL of this built from your GitHub release. To enable this functionality in Read the Docs, apply the following settings in [your Read the Docs dashboard](https://app.readthedocs.org/dashboard/): go to `Setup` - `Settings` - `Automation rules` - `Add rule` and set `Description`: 'Build all tags', `Match`: `Custom Match`, `Custom match`: `.*`, `Version type`: `Tag`, `Action`: `Activate version`

If you've your own webserver, you can publish each version on it manually.

## Publishing your book with publisher
You can choose to publish your online book with a publisher. This could increase findability of your book, but may have versioning, copyright and licensing consequences

For TU Delft employees, you can decide to publish via TU Delft OPEN interactive textbooks. Publishing will give you a copyright check, ISBN or DOI number, and registration in several shared databases but limits the amount of changes you can make to your book: for substantial changes a new published version is needed with an updated copyright checks. Small changes like typos can always be made, which are processed in the published version every hour.
In case of editing a book for a course during that actual course and/or your book has limited value outside your course's content, we advise you only to publish an archived version of your book whenever the academic year is over.