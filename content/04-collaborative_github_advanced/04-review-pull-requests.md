+++
title = "Review and merge Pull Requests"
date =  2021-05-13T17:59:21+03:00
weight = 4
+++

As the owner, it's time to **review the Pull Requests** the rest of your team mates have opened.

We've actually **snuck some errors into the instructions** we provided in your team mates issues. The PR review stage provides opportunity for any problems to be identified and dealt with before merging.

Let's use the first pull request made to the repo as an example. In this case, it was made by team mate **bobturneruk**, tackling [**issue #2** _Add subtraction function_](https://github.com/annakrystalli/python-calculator/issues/2) via [**pull request #5**](https://github.com/annakrystalli/python-calculator/pull/5).

## <i class="fas fa-user-circle"></i> Review 1st Subtract Pull Request 

As I mentioned, there is atleast one error in the Pull Request as a result of erroneous instructions in the issue.

Problems are also indicated by the failing tests which we can inspect.

{{< figure src="/images/ag-pr-sub-test-fail.png" >}}

{{< figure src="/images/ag-pr-sub-test-fail-detail.png" >}}

### <i class="fas fa-user-circle"></i> Identify the errors

The failing tests, and in particular, the linting check by **flake8** points to a **missing colon in the `subtract` function definition**.

**You may also have additional errors if the instructions in the issue were followed incorrectly by your team mates.** No problem though! The review stage will help us inspect and guide our team mates to correct any additional errors.

To **check that everything has been completed correctly**, refer to the [**Appendix**](/04-collaborative_github_advanced/05-appendix) in this chapter, which has the correct files and file content that should have been committed for each issue.
### <i class="fas fa-user-circle"></i> Review pull request and request changes 


Start the review by first inspecting the changes to the files made in the pull request by clicking on the <i class="fas fa-file-medical"></i> **Files changed** tab of the PR.

This tab shows all added and deleted lines of code in each file commited in the PR. It also allows us to **post review comments to an individual line of code**, by clicking on the <i class="fas fa-plus"></i> at the left hand side margin of the line of code.

{{< figure src="/images/ag-pr-sub-review-codeline.png" >}}

This opens a box to add your review comment. Once you've added your first comment, click on {{% button href="" %}} **Start a review**{{% /button %}} to add your comment and initiate a review.

In the case of the `subtract` PR, I **identified the line of code containing the error** (line #1 in `pythoncalculator/subtract.py`) and **added a comment identifying the error** for my team mate to correct.

GitHub has automatically flagged a couple more issues  (2 files that don't end in a newline, indicated by the <i class="fas fa-minus-circle" style="color:#ed2a2a"></i>) so I've also asked my team mate to correct those.

{{< figure src="/images/ag-pr-sub-review-detail.png" >}}

To submit my review, I click on {{% button href="" %}} **Finish your review**{{% /button %}} in the top-right corner and select the **Changes requested** option.

This posts my comments into the PR discussion tab where the author of the PR can respond to them. The fact that I've requested changes is also flagged.

{{< figure src="/images/ag-pr-sub-review-submitted.png" >}}

## <i class="fas fa-users"></i> Correct errors and respond to request for changes

Now my team can go **back to GitKraken** and **make the corrections** to any errors I've flagged 

{{% notice info %}}

Documentation on  [Editing files in GitKraken](https://support.gitkraken.com/working-with-files/editing-files/)

{{% /notice %}}

Once complete, they can then **commit the corrections** in their issue branch and **push again to GitHub**. The new commits will be added to the PR.

Next, my team mate moved back to the PR in GitHub and responded to each error individually to let me know it had been corrected. 

{{< figure src="/images/ag-pr-sub-review-response.png" >}}

## <i class="fas fa-user-circle"></i>  Complete final approving review.

### <i class="fas fa-user-circle"></i>  Check and resolve error conversations

At this point, I went back and **checked the changes to the files myself**. I also ensured that **all checks were passing**.

{{< figure src="/images/ag-pr-sub-review-response-checks.png" >}}



{{% notice warning %}}

If you still spot problems when you're reviewing the changes, repeat the process we've just been through.

If all checks aren't passing, have a look at the logs of the checks and/or re-inspect the changes to the files to spot  any  problems. Then repeat the process we've just been through.

{{% /notice %}}


 Once I was happy each one had been corrected, I responded also and **resolved each point individually**.

{{< figure src="/images/ag-pr-sub-review-response-resolve.png" >}}



We can also see the conversations have an *Outdated* tag associated with them. This indicates that new commits have been made since the discussion was initiated.

### <i class="fas fa-user-circle"></i> Initiate final approving review

Next I'll **submit a final review**, this time selecting the **Approve** option.

{{< figure src="/images/ag-pr-sub-review-approve.png" >}}

### <i class="fas fa-user-circle"></i> Merge Pull Request

Once the **approving review is submitted** and given **all the checks pass**, the pull request is now **ready to merge into the `main` branch! 🎉**

To initiate the merge, I click on {{% button href="" %}} **Merge pull request**{{% /button %}}

{{< figure src="/images/ag-pr-sub-review-merge-init.png" >}}

Next, I click on {{% button href="" %}} **Confirm merge**{{% /button %}}

{{< figure src="/images/ag-pr-sub-review-merge-confirm.png" >}}

The `subtract` branch has now successfully been merged into `main`! 🥳

I've also gone ahead and **deleted the <i class="fas fa-cloud"></i> origin `subtract` branch** to **keep the repo tidy** as the branch is now redundant (i.e. I don't expect any further contributions in this branch regarding the particular feature it was created for).

{{< figure src="/images/ag-pr-sub-review-merge-cmpl.png" >}}

## <i class="fas fa-user-circle"></i> Review 2nd Pull Request 

{{< figure src="/images/ag-pr-2-review-merge-confilct.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-init.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-cmpl.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-commit.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-pre.png" >}}

{{< figure src="/images/ag-pr-2-review-merge.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-issue-closed.png" >}}