# TeachBooks versioning with changelog
Versions combined with a changelog can be a very effective way to communicate book changes. Inspired by versioning systems in software management (i.e. semantic and CalVer versioning) version is used extensively in the world of software management to deal with versions. This is more suited than the more traditional way of versioning paper books (version 1, 2, etc.), because of the amount of edits which online books allow. TeachBooks versioning comes in two flavors:

1. `academic_year.additions.errata` versioning for books tailed-made for courses in which content is added / adapted during the course and might be restructured extensively every year while remaining to be available in the original form.
2. `major.errata` versioning for books which are more stable over years, in which big changes are covered only by the version number.

We've come up with guidelines how to use the two TeachBooks-versioning options (adapted from {cite:p}`semver`):

`````{tab-set}
````{tab-item} academic_year.additions.errata
1. A normal version number MUST take the form `academic_year.additions.errata` where `academic_year` is the academic year in which the book is used, and `additions`, and `errata` are non-negative integers, and MUST NOT contain leading zeroes. Each element MUST increase numerically. For instance: 2025.9.0 -> 2025.10.0 -> 2025.11.0
2. Once a versioned book has been released, the contents of that version MUST NOT be modified. Any modifications MUST be released as a new version.
3. Errata versions MUST be incremented if a small change is made which should be communicated to the reader in both the source code and in the book itself. If the small change is not crucial (like a simple typo), you might consider not defining it as a new version but combining it with other changes in the next errata or additions version.
4. Additions version MUST be incremented if an addition is made to the book. It MUST be communicated in both the source code and in the book itself. It MAY include errata level changes. The errata version MUST be reset to 0 when the addition version is incremented.
5. Academic year version MUST be incremented if a fresh book is started for which additions will follow later. It MUST be communicated in both the source code and in the book itself. Additions and errata versions MUST be reset to 0 when academic version is incremented.
6. Precedence refers to how versions are compared to each other when ordered.
   1. Precedence MUST be calculated by separating the version into academic year, additions and errata identifiers in that order.
   2. Precedence is determined by the first difference when comparing each of these identifiers from left to right as follows: Academic year, additions and errata versions are always compared numerically. Example: 2024.0.0 < 2025.0.0 < 2025.1.0 < 2025.1.1.
7. The way in which the version number is incremented after the initial release should be explained in the README of the source code and in the book itself.
````
````{tab-item} major.errata
1. A normal version number MUST take the form `major.errata` where `major`, and `errata` are non-negative integers, and MUST NOT contain leading zeroes. Each element MUST increase numerically. For instance: 9.0 -> 10.0 -> 11.0
2. Once a versioned book has been released, the contents of that version MUST NOT be modified. Any modifications MUST be released as a new version.
3. Errata versions MUST be incremented if a small change is made which should be communicated to the reader in both the source code and in the book itself. If the small change is not crucial (like a simple typo), you might consider not defining it as a new version but combining it with other changes in the next major version.
5. Major versions MUST be incremented if a substantial restructure or additions is made. It MUST be communicated in both the source code and in the book itself. Errata versions MUST be reset to 0 when the major version is incremented.
6. Precedence refers to how versions are compared to each other when ordered.
   1. Precedence MUST be calculated by separating the version into major and errata identifiers in that order.
   2. Precedence is determined by the first difference when comparing each of these identifiers from left to right as follows: major and errata versions are always compared numerically. Example: 1.0 < 2.0 < 2.1.
7. The way in which the version number is incremented after the initial release should be explained in the README of the source code and in the book itself.
````
`````

## Changelog
To communicate changes, we advise creating a changelog in the book. The [template](https://github.com/TeachBooks/template/blob/main/book/changelog.md) contains an empty changelog to fill:

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

An example can be found [here](https://ciem5000-2025.github.io/book/changelog.html)

## Note on version change on page
When making errata changes or additions, it's advised to notify the reader not only in the changelog, but also on the relevant pages. You can do so using the `versionadded` and `versionchanged` admonitions:

```md
::::::{versionchanged} <version_number> <date of version release>
<explanation of change on current page>
::::::
```

and

```md
::::::{versionadded} <version_number> <date of version release>
<explanation of addition on/of current page>
::::::
```

Leads to for example:
::::::{versionchanged} v2025.3.5 2025-02-23
TeachBooks versioning added
::::::

## Implement tags and releases
Tags can be added to your source code by adding the version number as a tag to a specific commit. You can do so only locally. In GitHub Desktop this is done by clicking 'Create Tag...` for a specific commit in the History tab.

```{figure} figures/tags.png
---
width: 500px
align: center
---

```

Once the tags is pushed to GitHub/GitLab. You can create a release of the version by clicking `Release` on the `Code` page of your repository. There you can select a tag and generate release notes. It's recommended to add the relevant part of the changelog too. An example can be found [here](https://github.com/CIEM5000-2025/book/releases/tag/v2025.2.0)
