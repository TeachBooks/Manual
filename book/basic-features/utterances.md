# Discussions in your book: Utterances

[Utterances 🔮](https://utteranc.es/) is a lightweight open-source widget which allows you, your colleages and your students to discuss stuff in a blog post in your book. It is build on GitHub issues, so requires a GitHub repository, although the book can be hosted anywhere (so also on GitLab).

The [utterances website](https://utteranc.es/) clearly explains the required steps. One thing to take care of is how you want to do the issue-mapping with respect to multiple deployed versions (draft version, student version, archived versions):
 
 - `Issue title contains page pathname`/`Issue title contains page URL` is useful if you want to isolate the comments on each of the branches.
 - `Issue title contains page title` is useful if you want to show the all comments on all different branches.

The given script can be added anywhere in your book, just copy the html-script into your `.md`-file or a markdown cell in your `.ipynb`-file. The blogpost is not visible when you do a local build of the book, build it online or use a local python server as shown in {ref}`setup-local-server`.

Users need to have a GitHub-account to post a message. Although this might be a burden, it allows students to track their previous posts and set up notifications on follow-up posts.

If you'd like notifications on new posts in your book, which end up as issues in your GitHub repository, you can configure the GitHub `watch` settings to do so as [explained here](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#configuring-your-watch-settings-for-an-individual-repository).

Below you see an example of this feature!

## Example discussion
<script src="https://utteranc.es/client.js"
        repo="TeachBooks/manual"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>