# Build pull requests from forks

```{admonition} User types
:class: tip
This section is useful for user type 3-5.
```

When using the [deploy-book-workflow](../external/deploy-book-workflow/README.md) you're not able to build pull requests. When you'd like to contribute to the book of someone else with a fork, this requires you to set up the deploy-book-workflow in your fork to be able to show the proposed changes in the book. Furthermore, when proposing your contribution in a pull-request, you'd have to manually refer to your own built book. This process can be made easier by using [Read the Docs](https://about.readthedocs.com/?ref=readthedocs.org) for building the books with changes of a pull request.

Read the docs is not recommended for final versions of your book because of the advertisement in the free version. If you'd like to pay for it, it can replace the functionality of the [deploy-book-workflow](../external/deploy-book-workflow/README.md).

This workflow does not work if you have local sphinx extensions in your book (extensions in `book/_ext` like [](./apa.md)).

## Usage

When opening a pull request, GitHub will shows this line:

![Read the docs in GitHub preview](./figures/readthedocs1.png)

Click 'Details' to see the logs of the build process.

Whenever the build is done, click 'Details' again to see the build book. Tip, click `d` or add `?readthedocs-diff=true` to the url to see the differences on the pages highlighted. Note that this difference functionality is not perfect as it might indicate elements which are not changed and it has issues with buttons, LaTeX and figures.

## Setting up

### Add configuration file to your repository

Add a file `.readthedocs.yaml` to the root of your repository, containing the following content:

```yaml
version: 2

build:
  os: ubuntu-24.04
  tools:
    python: "3.13"
  jobs:
    pre_build:
      - "jupyter-book config sphinx book/"

python:
  install:
    - requirements: requirements.txt
    - requirements: standard-imghdr

sphinx:
  builder: html
  fail_on_warning: true
  configuration: book/conf.py
  ```

You might need to add `standard-imghdr` to your `requirements.txt` file if the build fails when you've configured it in Read the Docs (if the error tells you `ModuleNotFoundError: No module named 'imghdr'`)

### Setup Read The Docs account

Setup an account at [](https://app.readthedocs.org/accounts/login/?next=/dashboard/). We recommend using your GitHub account for authentication.

When authorizing Read the Docs for your GitHub account, you can grant access by Read the Docs for organization you own too. Do this if your book is part of an organization.

### Authorize access to organization
When you didn't do so in the previous step, or you'd like to grant access at a later moment, you can grant/revoke access by Read the Docs to organization your own [`personal GitHub Settings - Integrations - Applications - Authorized OAuth Apps - Read the Docs Community`](https://github.com/settings/connections/applications/fae83c942bc1d89609e2).

### Add project in Read The Docs

On your [dashboard](https://app.readthedocs.org/dashboard/), add a new project. Find your GitHub repository (you might need to refresh your repositories if you've recently updated authorizations)

### Enable Pull Request build

In the setting of your newest project, enable build of pull request by selecting the option in `Building - Pull request builds - Build pull requests for this project`.