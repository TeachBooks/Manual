# Versioning and URLs

```{admonition} User types
:class: tip
This page is useful for user type 4-5.
```

Online books can be easily updated, however, this might confuse readers. Therefore, it's good practice to be aware of this and, where needed, provide explicit version to the readers. It's recommended to do this in multiple ways, which can be combined:
- Publish versions on separate (fixed) URLs
- Use some sort of semantic versioning with tags
- Keep both source code as (export of) websites of archived versions
- Publishing your book more officially

## Publish version on separate (fixed) URLs
When making books for education, typically your book can change substantially for consequential academic years. Using the [](../external/deploy-book-workflow/README.md), you can release the different version of your book all under the same root URL. If you name each students' version of each year to the `<current academic year>`, the students URL includes that academic year too. It is recommended to yearly update the current academic year branch as the `PRIMARY BRANCH` when using the [GitHub workflow](gh-workflow-settings). This ensures that students are redirected to a consistent URL, even when new versions of the book are added later. Eventually, you can add old branches to the list of `BRANCHES_ARCHIVED` when using the [GitHub workflow](gh-workflow-settings) to include a banner on the page indicating its archived state.

If you plan on maintaining only one public version, it is advisable to set `BEHAVIOR_PRIMARY` from the default `redirect` to `copy`. This ensures that the primary branch is copied to the root, making the URL more compact.

Don't forget to explain how you organize these URLs in your README and eventually in the book itself too with a sentence like this:

> This is the 2024-2025-version of this book. Go to `<link to root URL>` to view the most recent version of this book, or adapt the year in `<link to root URL>/<year>` to the year when you took the course.

If you've many version of the book, at some point you might reach the 1 GB GitHub Pages limit. This is only expected for extremely large books with a lot of non-text-based (binary) content. To prevent going over that limit, store large content not used for building the website (like images) on an external server. This can be another GitHub repository or a (paid) object store

## Semantic versioning

## Publishing your book with publisher
You can choose to publish your online book with a publisher. This could increase findability of your book, but may have versioning, copyright and licensing consequences

For TU Delft employees, you can decide to publish via TU Delft OPEN interactive textbooks. Publishing will give you a copyright check, ISBN or DOI number, and registration in several shared databases but limits the amount of changes you can make to your book: for substantial changes a new published version is needed with an updated copyright checks. Small changes like typos can always be made, which are processed in the published version every hour.
In case of editing a book for a course during that actual course and/or your book has limited value outside your course's content, we advise you only to publish an archived version of your book whenever the academic year is over.