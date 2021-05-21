+++
title = "Review 2nd Pull Request handling merge conflicts"
date =  2021-05-21T16:16:40+03:00
weight = 5
+++


## <i class="fas fa-user-circle"></i> Review 2nd Pull Request


Next I'll move onto merging the second pull request. Just like the previous one, I **first inspect the checks and code contributed** and **request modifications** to any errors I've noted **until all checks are passing**. In this example, I'm merging my team mate **robadob**'s contribution who worked on the **

However, once those have been dealt with, I'm still left with **another blocker to merging the pull request, a merge conflict!**

> Merge conflicts happen when you **merge branches that have competing commits**, and **Git needs your help to decide which changes to incorporate in the final merge**.

In the case of our second PR, the **conflict arises from the fact that line 2 of the `pythoncalculator/__init__.py` file has been edited**. However, **the first PR**, which has now been merged into `main`, **also committed an edit to that exact line**, .  

Find out more about [Addressing merge conflicts
](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/addressing-merge-conflicts) and [Resolving a merge conflict on GitHub
]()

{{< figure src="/images/ag-pr-2-review-merge-confilct.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-init.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-cmpl.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-confilct-resolve-commit.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-pre.png" >}}

{{< figure src="/images/ag-pr-2-review-merge.png" >}}

{{< figure src="/images/ag-pr-2-review-merge-issue-closed.png" >}}
