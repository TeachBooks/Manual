# APA references

```{admonition} User types
:class: tip
This page is useful for user type 4 and 5.
```

{bdg-primary}`(To be converted into) Sphinx Extension`

## Introduction

This extension allows you to have APA formatting which is not a default option.

## Installation
To use APA-references, a python package needs to be manually loaded into your book

**Step 1: Add zip file to book root**

Add the zip-file [`_ext.zip`](_ext.zip) to the root of your file so that it looks like:

```
book
├── _ext.zip
│   ├── pybtexapastyle/
│   ├── apastyle.py
│   ├── bracket_citation_style.py
├── _config.yml
├── _toc.yml
├── requirements.txt
├── <book files>
```

**Step 2: Add to `requirements.txt`**

Add a specific version of `docutils` to your requirements file:
```
docutils==0.17.1
```

**Step 3: Enable in `_config.yml`**

In your `_config.yml` file, add a `bibtex_default_style`, `bybtex_reference_style` and the local extensions `apastyle` and `bracket_citation_style.py`
```
sphinx:
  config:
    ...
    bibtex_default_style: myapastyle
    bibtex_reference_style: author_year_round
  local_extensions:
    apastyle: _ext/
    bracket_citation_style: _ext/
  ...
```

## Usage
All references are now made in APA-style. See for example this reference: {cite}`jason_moore` which shows up on the [references page](../references.md) too.

For more options on the in-line citation style, see https://jupyterbook.org/en/stable/content/citations.html#change-the-in-line-citation-style.

### Known issue
During the build, warning will be raised with `... WARNING: duplicate label for keys ...`. In most cases, these warnings can be ignored.

## Contribute
This tool needs to be developed further to make it into a proper sphinx-extension. The process is described here: https://github.com/orgs/TeachBooks/projects/17. If you've ideas or questions, please reach out to us at info@teachbooks.io!