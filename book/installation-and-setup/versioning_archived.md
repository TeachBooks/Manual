# Keep source code and website of all versions
Although you might only want to share the most recent version of the book with your readers, it might be useful too the have the source code and website of older versions somewhere too.

Git allows you to go back in the git history to the source code of old versions. To make this as easy as possible for readers, use tags and releases instead of having the readers scroll through a long list of (not alway very descriptive) commit descriptions.

To share the built book / website of old versions for your book on GitHub you've a few options:
- add a zip of the built book to the release in GitHub as binary asset. This requires readers to download the zip and open the html files locally, but doesn't require you to host it somewhere. This zip can be easily downloaded as an artifact from [the GitHub action](../external/deploy-book-workflow/README.md). An example can be found [here](https://github.com/TUDelft-books/CME4501/releases/tag/v2024.1.0)
- create a branch for each tag. When doing this, [the GitHub workflow](../external/deploy-book-workflow/README.md) will build it on GitHub pages. It's advised to use the version as branch name. You can create a branch from a tag locally by running: `git branch <new_branch name> <tag/version>`. Note that when you've many version and a large book, this approach might easily fill up your 1 GB GitHub pages limit.
- Use [Read the Docs](../features/pull_request_build.md) to build a website for all your tags. Refer to the URL of this built from your GitHub release. To enable this functionality in Read the Docs, apply the following settings in [your Read the Docs dashboard](https://app.readthedocs.org/dashboard/): go to `Setup` - `Settings` - `Automation rules` - `Add rule` and set `Description`: 'Build all tags', `Match`: `Custom Match`, `Custom match`: `.*`, `Version type`: `Tag`, `Action`: `Activate version`

If you've your own webserver, you can publish each version on it manually.