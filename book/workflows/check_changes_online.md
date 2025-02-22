# Check changes online

```{Note}

This page is relevant for user type 4 and 5. When making changes to the book it can be useful to get an idea on how they will be realized in the online book. Whereas user type 5 can also build the book locally, user type 4 is more focused on the changes to the content.

However both users would certainly benefit from checking whether their changes look good in the book!
```

Now that you've pushed your changes online, it's time to check the change in the online build book to make sure that your changes are processed correctly. For this step it is assumed you're using TeachBook's GitHub actions or TeachBook's GitLab pipeline.

`````{tab-set}
````{tab-item} In GitHub

Once GitHub Pages is enabled and your book is published, you can view it by visiting the GitHub Pages URL for your repository. A summary can be seen under the <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-play UnderlineNav-octicon d-none d-sm-inline">    <path d="M8 0a8 8 0 1 1 0 16A8 8 0 0 1 8 0ZM1.5 8a6.5 6.5 0 1 0 13 0 6.5 6.5 0 0 0-13 0Zm4.879-2.773 4.264 2.559a.25.25 0 0 1 0 .428l-4.264 2.559A.25.25 0 0 1 6 10.559V5.442a.25.25 0 0 1 .379-.215Z"></path></svg>`Actions`- `All workflows` -  `call-deploy-book` in GitHub. It shows you a descriptive summary.
The summary also provides build error messages, which you might fix in a new commit.

If this is not activated yet, you can do so as describe [here](../external/deploy-book-workflow/README). Here you can also find more information.

````

````{tab-item} In GitLab

At the moment this is not possible.
However, what you can do is 'mirror' your GitLab repository to GitHub. This will copy your content automatically (but maximum once every 5 minutes) to GitHub. This allows you to use the TeachBook's GitHub actions.

Instructions on how to set up mirroring are provided here: https://docs.gitlab.com/ee/user/project/repository/mirror/push.html#set-up-a-push-mirror-from-gitlab-to-github

````

`````

You can keep on [editing](edit_book) and checking your changes until you're satisfied and ready for a review by a colleague.