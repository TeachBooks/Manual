(teachbooks-package)=
# Sharing content between books in table of contents

```{admonition} User types
:class: tip
This page is useful for user type 3-5.
```

{bdg-secondary}`Python Package`

## Introduction
When creating books, you might want to reuse material from other people or from other books you made. In some cases you might even want to have the exact same material into your book. You could do so by manually copying material over. However, whenever the source material is updated, you have to do that again. As an alternative, you can use the underlying git system to refer to the source file directly. This allows you to pick a specific version, or keep the most up-to-date version of it. This pages explains how to do so directly in the table of contents using the TeachBooks package. Previously, this was implemented using [submodules] (../external/Nested-Books/README.md), but this implementation is more difficult to use.

## What does it do?

This functionality, part of the [TeachBooks package](https://github.com/TeachBooks/TeachBooks) allows you to refer to `.ipynb` and `.md` files stored on public repositories. These files are then handles as if they were normal files in your book, leading to a the file as a page in your built book.

## Installation
To use this extenstion, follow these steps:

**Step 1: Install the Package**

Install the module `teachbooks` package using `pip`:
```
pip install git+https://github.com/BSchilperoort/TeachBooks@external-git-content
```
    
**Step 2: Add to `requirements.txt`**

Make sure that the package is included in your project's `requirements.txt` to track the dependency:
```
git+https://github.com/BSchilperoort/TeachBooks@external-git-content
```

## Usage

To use the functionality, take the URL of a file and add it to your `_toc.yml` as follows:

```yaml
format: jb-book
root: .

parts:
  - caption: ...
    chapters:
    - file: ...
    .
    .
    .
    - external: <link to GitHub / GitLab source .md or .ipynb file>
    .
    .
    .
```

The link can be pointing to a file on a branch (which will take the most recent version of that file on the branch) or a commit or tag (which will take a specific version of the file). For example:
- `external: https://github.com/TeachBooks/manual/blob/release/book/intro.md` will take the most recent version of the intro page of this book on the release branch
- `external: https://github.com/TeachBooks/manual/blob/06d67e8a0110c94d9147ce07090656dedc7d0e64/README.md` will take the file during the state of a specific commit (06d67e8).
- `external: https://github.com/TeachBooks/manual/blob/v1.1.1/README.md` will take the file during the state of a specific tag (v1.1.1)

If you're building your book online in GitHub, the [deploy-book-workflow](../external/deploy-book-workflow/README.md) will deal with these files during the `teachbooks build` command. If you want to build the book locally, run the command `teachbooks build`.

If the source file is from another book, the contents of the `requirements.txt`, `_config.yml` and `*.bib` file are merged to make sure the page has the same functionality as in the source repository. If this leads to compatibility issue, you'll be warned during the build. Furthermore, licenses of external books will be checked to avoid copyright issues.

## Contribute

This tool's repository is stored on [GitHub](https://github.com/TeachBooks/TeachBooks). If you'd like to contribute, you can create a fork and open a pull request on the [GitHub repository](https://github.com/TeachBooks/TeachBooks).