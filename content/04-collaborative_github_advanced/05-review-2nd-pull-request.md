+++
title = "Review 2nd Pull Request: handling merge conflicts"
date =  2021-05-21T16:16:40+03:00
weight = 5
+++


## <i class="fas fa-user-circle"></i> Review 2nd Pull Request


Next I'll move onto merging the second pull request. Just like the previous one, I **first inspect the checks and code contributed** and **request modifications** to any errors I've noted **until all checks are passing**. 

### Example: Merge in the `divide` Pull Request.

In this example, I'm merging my team mate **robadob**'s contribution who worked on **adding a division function** ([**issue #4** _Add subtraction function_](https://github.com/annakrystalli/python-calculator-demo/issues/4) via [**pull request #7**](https://github.com/annakrystalli/python-calculator-demo/pull/7).

Rob actually spotted and corrected the sneaky error in  the instructions so the PR passed all checks straight away. However, I'm now left with **another blocker to merging the pull request, a merge conflict!**

> Merge conflicts happen when you **merge branches that have competing commits**, and **Git needs your help to decide which changes to incorporate in the final merge**.

In the case of our second PR, the **conflict arises from the fact that line 2 of the `pythoncalculator/__init__.py` file has been edited**. However, **the first PR**, which has now been merged into `main`, **also committed an edit to that exact line** which **Rob's branch doesn't know about** (the merge of the first PR happened after Rob made his branch off the `main`). This has resulted in a merge conflict that git doesn't know how to deal with and needs our help!

{{% notice info %}}
Find out more about [Addressing merge conflicts
](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/addressing-merge-conflicts) and [Resolving a merge conflict on GitHub
](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-on-github).

{{% /notice %}}

#### <i class="fas fa-user-circle"></i> Resolve conflict

**Because the conflict is a simple one, we are able to resolve it on GitHub**. For more complex conflicts you may need to pull the branch down and resolve locally.

Click on {{% button href="" %}} **Resolve conflicts**{{% /button %}} to initiate the process.

{{< figure src="/images/ag-pr-2-review-merge-confilct.png" >}}

This **opens a text editor panel** showing you **any files that have conflicts** (in our case `pythoncalculator/__init__.py`) and highlights the **lines of conflicting code** as well as **their origin**.



{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-init.png" >}}

In this text editor, we can **edit the file to tell git what we want to do with the conflicting code**. We want to **keep both `import` statements** so in this case, all we need to do is **delete the lines containing source indicator notation**.

Our **resolved file should similar to the one below** when we're done (they may vary depending on which issues were contributed in each of the first two pull requests).

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-cmpl.png" >}}

#### <i class="fas fa-user-circle"></i> Commit resolved conflict

When we're happy with our file we click on {{% button href="" %}} **Mark as resolved**{{% /button %}}

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-commit.png" >}}

Finally, to **commit our changes to the 2nd PR branch** (in this case the `divide` branch), we the click {{% button href="" %}} **Commit merge**{{% /button %}} and follow through to completion. 

As noted, **the merge commit will be associated with the person who resolved the conflict** (in this case the project owner).

#### <i class="fas fa-user-circle"></i> Review and merge Pull Request

Now all that's left is to **submit an approving review** and **merge**.

First we **submit the approving pull request review** which is now added PR conversation next to <i class="fas fa-check-circle" style="color:#2AA745"></i>.

Note a couple more things:

- Note the special keyword used in Rob's PR description.
- Note that the owner's commit resolving the merge conflict is also now present in the conversation. 🎉

{{< figure src="/images/ag-pr-2-review-merge-pre.png" >}}

**Once the approving review has been submitted and all checks are passing, the PR is ready to be merged!** 

Click {{% button href="" %}} **Merge pull request**{{% /button %}} and follow through to completion. Go ahead and also **delete the PR branch** (in this case `divide`) to keep the repo tidy.


{{< figure src="/images/ag-pr-2-review-merge.png" >}}

#### <i class="fas fa-user-circle"></i> Close issue

Note that the **special keyword `Closes`** in combination with the issue number (**`#4`**) **automatically closed issue number 4**.

If that wasn't the case for your PR, **go ahead and close the issue manually.**

{{< figure src="/images/ag-pr-2-review-merge-issue-closed.png" >}}


#### <i class="fas fa-user-circle"></i> Review remaining Pull Requests

Go ahead and follow the same processes (reviewing and asking for corrections where required and resolving merge conflicts) for any remaining pull requests.