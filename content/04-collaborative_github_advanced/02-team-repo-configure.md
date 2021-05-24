+++
title = "Make first owner contribution"
date =  2021-05-13T17:58:07+03:00
weight = 2
+++

To demonstrate contributions through branches we'll first start with a small contribution to the python package metadata by the <i class="fas fa-user-circle"></i> owner. 

But first, to complete any work on the repo locally, we first need to download the repo to our computers. So let's go ahead and all do that.

## <i class="fas fa-user-circle"></i> <i class="fas fa-users"></i> Make a local copy of the repository

Open GitKraken and on the left-hand navigation bar, click on {{% button href="" %}} <i class="fas fa-cloud-download-alt"></i> Clone a repo {{% /button %}}

{{< figure src="/images/ag-gk-clone.png" >}}

Next, choose **GitHub.com** as the source of the repository. This allows GitKraken to search through any repositories you have access to.

 On the next panel, first choose your destination directory (I've chosen my `~/Desktop/`). 

Then, in the **Repository to clone** box, start typing `python-calculator` until the repo associated with  your account appears. Select it and click {{% button href="" %}} Clone the repo! {{% /button %}} 

{{< figure src="/images/ag-gk-clone-pc.png" >}}

{{% notice note %}}

To clone any repository you don't have direct access to, use the **Clone with URL** option. You can download any public repository on GitHub like this but if you are not a collaborator, you will not be able to push. To contribute to such a repository you are best making a fork and then a pull request from your own fork to the upstream repo..

{{% /notice %}}

If all went well, at the top of the application you should see a banner reading _Successfully cloned repo 'python-calculator'_.

Click on the {{% button href="" %}}**Open Now** {{% /button %}} button.

You should now see the git status of your **<i class="fas fa-laptop"></i> local** and **<i class="fas fa-cloud"></i> origin** repositories and all the files associated with the project. Everything should be up to date.


{{< figure src="/images/ag-gk-open.png" >}}


## <i class="fas fa-user-circle"></i> Create a new branch

Let us first get the <i class="fas fa-user-circle"></i> owner of each repo to make a contribution via a branch and pull request and get another member of the team to review it.

To create a new branch from the `main` branch, first make sure that, in the left-hand navigation panel, the **<i class="fas fa-check-square" style="color:#7CFF7E; background-color:black; padding:2px"></i> <i class="fas fa-code-branch"></i> main** branch in the **<i class="fas fa-laptop"></i> local** repo is checked.

When you're ready, click on the {{% button href="" %}} **Branch** <br> **<i class="fas fa-code-branch"></i>**{{% /button %}} button on the top panel. 

In the new branch text box that appears, enter a name for the new branch, e.g. `edit-metadata`. Press **Return** or **Enter** to create the new branch.

{{< figure src="/images/ag-gk-branch-new.png" >}}

If you hover over the branch indicator, you'll now see there are two branches, all in the same git state 👍

{{< figure src="/images/ag-gk-branch-metadata.png" >}}

## <i class="fas fa-user-circle"></i> Edit `setup.cfg`

The `setup.cfg` file in a python package stores metadata about the project. Each owner will now edit that file to add their **author details** as well as complete the **details of the team repository**.

We can edit the file in GitKraken by first navigating to the file in the bottom-right file panel. Once you've double-checked you're in the correct branch, click on {{% button href="" %}} **<i class="fas fa-pencil-alt"></i> Edit this file**{{% /button %}}.

{{< figure src="/images/ag-gk-cfg-edit-init.png" >}}

Next, edit the:

- <i class="fas fa-check-square" ></i> **author** field with your name.
- <i class="fas fa-check-square" ></i> **author_email** field with your email.
- <i class="fas fa-check-square" ></i> Complete the **url** with your github account details.
- <i class="fas fa-check-square" ></i> Complete the **Bug Tracker** field under **project_urls** again with your github account details.

Press <img src="/images/command-symbol.png" width="2px" style="align:left; display:inline; margin:0;"/> **| Ctrl + S** to save your changes.

{{< figure src="/images/ag-gk-cfg-edit-details.png" >}}
## <i class="fas fa-user-circle"></i> Commit changes to `setup.cfg`

The right hand side panel now indicates that you have a single unstanged file (`setup.cfg`) with uncommitted changes.  

Click on the {{% button href="" %}} **Stage file**{{% /button %}} or {{% button href="" %}} **Stage all changes**{{% /button %}} button.

{{< figure src="/images/ag-gk-cfg-stage.png" >}}

This stages `setup.cfg` and opens up the commit panel. Add a commit message to your commit, e.g. ***Add author and github repo details***.

Click {{% button href="" %}} **Commit changes to 1 file**{{% /button %}}

{{< figure src="/images/ag-gk-cfg-commit.png" >}}

Your commit has now been made to the `edit-metadata` branch and you can see it is ahead of the both the **<i class="fas fa-laptop"></i> local** and **<i class="fas fa-cloud"></i> origin** `main` branch.

{{< figure src="/images/ag-gk-cfg-commit-cmpl.png" >}}

## <i class="fas fa-user-circle"></i> Push changes to GitHub

Click on {{% button href="" %}} **Push** <br> **<i class="fas fa-upload"></i>**{{% /button %}} to push to GitHub.

This will create a new branch in the **<i class="fas fa-cloud"></i> origin** repository. By default it will name it the same as the **<i class="fas fa-laptop"></i> local** branch (`edit-metadata`), so just click on {{% button href="" %}} **Submit**{{% /button %}} to continue.

{{< figure src="/images/ag-gk-cfg-push-init.png" >}}

Once the push is complete, you will notice that there is now an **<i class="fas fa-cloud"></i> origin** commit indicator associated with the branch, indicating that the **<i class="fas fa-laptop"></i> local** and  **<i class="fas fa-cloud"></i> origin** branch are in synch while both <i class="fas fa-cloud"></i> origin and <i class="fas fa-laptop"></i> local `main` branches are 1 commit behind `edit-metadata`.

{{< figure src="/images/ag-gk-cfg-push-cmpl.png" >}}

## <i class="fas fa-user-circle"></i> Make pull request

We can make a pull request from within GitKraken!

To do so, on the left-hand navigation panel, hover over **PULL REQUESTS** and click on the {{% button href="" %}} **<i class="fas fa-plus-square" style="color:#7CFF7E"></i> Create pull request**{{% /button %}} button when it appears.

{{< figure src="/images/ag-gk-cfg-pr-init.png" >}}

Next configure the **details of the pull request** including the **source and target repository** (in this case your copy of the repository) and the **source and target branches**, in this case you want to merge the `edit-metadata` branch into the `main` branch.

{{< figure src="/images/ag-gk-cfg-pr-details-br.png" >}}

We also need our pull request reviewed before it can be merged. A nice feature of pull requests is than you can **request a review** from a team mate. Let's do this. 

If you scroll down to **Reviewers** you will be able to **select a reviewer from your team mates**. Go ahead and select someone. 

Finally, at the very bottom, click on {{% button href="" %}} **Create Pull Request**{{% /button %}} to submit it.

{{< figure src="/images/ag-gk-cfg-pr-details-rev.png" >}}

You should now see **1** indicated next  to **PULL REQUESTS**. If you click on it to expand you can see your pull request listed and if you hover over it, you can see 
more details.

{{< figure src="/images/ag-gk-cfg-pr-cmpl-details.png" >}}

Clicking on the three **<i class="fas fa-ellipsis-v"></i> vertical dots** next to the PR opens up a menu that allows you to **View the pull request on GitHub.com**

{{< figure src="/images/ag-gk-cfg-pr-gh-view-init.png" >}}

Clicking on that, navigates you to the PR page on GitHub. You can see that the Continuous integration tests have passed (indicated by <i class="fas fa-check-circle"  style="color:#2AA745"></i> **All Checks have passed**). However merging is blocked until an approving review is submitted (indicated by <i class="fas fa-times-circle" style="color:#ed2a2a"></i> <span style="color:#ed2a2a">**Review Required**</span> and <i class="fas fa-times-circle" style="color:#ed2a2a"></i> **<span style="color:#ed2a2a">Merging is blocked**)</span>.

{{< figure src="/images/ag-gk-cfg-pr-gh-view.png" >}}

## <i class="fas fa-users"></i> Review Pull Request

Next, the **team member the owner requested a review from should perform the review**. Other team member's could also do this but to keep things simple let's just let the assigned reviewer do this.

In the pull request **Files changed** tab, the reviewer has the opportunity to **inspect the changes made in the pull request**.

{{< figure src="/images/ag-cfg-pr-inspect.png" >}}

They can also initiate a review by clicking {{% button href="" %}} **Review changes** {{% /button %}} in which they can:
- add a comment
- approve the review
- explicitly request changes


{{< figure src="/images/ag-cfg-pr-rev-gen-init.png" >}}

Alternatively, the can initiate a review by inserting a comment next to a specific line of code.

{{< figure src="/images/ag-cfg-pr-rev-code-init.png" >}}


## <i class="fas fa-user-circle"></i> Merge Pull Request

Once **an approving review has been submitted** (and as long as all checks are passing), the **PR is  free to be merged!**

{{< figure src="/images/ag-cfg-pr-review-cmpl.png" >}}


{{< figure src="/images/ag-cfg-pr-merge-init.png" >}}

Follow through until the PR has been merged! 

To **keep the repo tidy**, as the `edit-metadata` branch is now redundant (i.e. I don't expect any further contributions in this branch regarding the particular feature it was created for), I'm going to go ahead and click **Delete branch**. 

{{< figure src="/images/ag-cfg-pr-merge-cmpl.png" >}}

This removes the <i class="fas fa-cloud"></i> origin `branch`. Later we'll also delete <i class="fas fa-laptop"></i> local branch also.

{{< figure src="/images/ag-cfg-pr-merge-clean.png" >}}
