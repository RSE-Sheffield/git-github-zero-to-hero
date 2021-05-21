+++
title = "Resolve Issues in Branches"
date =  2021-05-13T17:58:45+03:00
weight = 3
+++



A **powerful tool for keeping track of tasks, enhancements, and bugs for your projects is the issues** feature of GitHub. You can access the issues associated with a repository through the <i class="fas fa-exclamation-circle"></i> **Issues** tab.

They allow **storing conversations about tasks in the project repository**, visible to the whole team throughout the life cycle of the project, rather that them being buried in hard to navigate email chains! 💯 

It's also **easy to see the status of tasks** as issues can be closed when completed, leaving the tasks still pending visible by default.

You can **write in markdown** so they are **great for having discussions around code**.

They can also be **assigned** to a specific team member, **labelled** and associated with specific project **milestones**.



{{% notice info %}}

For more information, check out the [Mastering Issues](https://guides.github.com/features/issues/) GitHub Guide

{{% /notice %}}

## <i class="fas fa-user-circle"></i> Open and assign issues

To organise the tasks for each team member, **the owner will first open an issue for each person** which will contain detailed instructions on how to complete the task.

I've actually used a nice feature of issues to make this easy for owners called **GitHub Issue templates**. The markdown files that power the feature are stored in the `.github/ISSUE_TEMPLATE` folder of the project. Let's see how they work.

{{% notice info %}}

For more information, check out [Configuring issue templates for your repository](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository) in the GitHub Docs

{{% /notice %}}



### <i class="fas fa-user-circle"></i> Open issue from templates

To create a new issue navigate to the <i class="fas fa-exclamation-circle"></i> **Issues** tab 

{{< figure src="/images/ag-issues-tab.png" >}}

Click {{% button href="" %}} **New issue** {{% /button %}} 

{{< figure src="/images/ag-issue-init.png" >}}

Because we are using GitHub Issue templates, we are immediatelly presented with the 3 issue templates I've created. 

To demonstrate, I'm going to open the **Add subtraction function** issue. To initiate the process, I click on {{% button href="" %}} **Get started** {{% /button %}} next to the issue template I want  to open.

_You can override the templates and create an issue with custom content by clicking on_ ***Open a blank issue*** _at the bottom of the page._

{{< figure src="/images/ag-issue-sub-init.png" >}}

### <i class="fas fa-user-circle"></i> Inspect issue content

Because we're working from an issue template, the title and contents of the issue are already pre-populated.

The contents of this particular issue contain detailed step-by-step instructions on how to **add a `subtract` function as well as a test** to our `pythoncalculator` package. At the top of the issue there's also a **checklist** of all the steps involved which team mates can use to **keep track of and communicate their progress**.

The **special `-[ ]` list notation** means the **checkboxes will be interactive** when the issue is submitted.

When we're creating our issue, the main body contains two tabs:

- **Write:** were you enter the contents of the issue in markdown
- **Preview:** were you can preview what the content will look like when it is rendered once the issue is submited. 

Toggle the tabs below to explore this feature. Note how the checklist is rendered in the Preview tab.

{{< tabs groupId="issues" >}}
{{% tab name="Write" %}}
{{< figure src="/images/ag-issue-sub.png" >}}
{{% /tab %}}
{{% tab name="Preview" %}}
{{< figure src="/images/ag-issue-sub-preview.png" >}}
{{% /tab %}}
{{% /tabs %}}



### <i class="fas fa-user-circle"></i> Assign team mate to issue

Now that I'm happy with the content of the issue (which needs no editing...aren't GitHub issue templates awesome?! 😜), I'm **ready to assign the task to one of my team mates**.

To do this, I click on **Assignees** on the top-right which launches a drop-down menu of team mates associated with the project and **select the team mate I want to assign**.


{{< figure src="/images/ag-issue-sub-assign.png" >}}

{{% notice tip %}}

You can **assign an issue to a team mate, add more or remove assignees at any point**, even after you've opened the issue. If your repo is public, **you can also assign issues to users who are not collaborators** on your repo. Just type in their username in the drop down menu textbox. 

{{% /notice %}}

### <i class="fas fa-user-circle"></i> Submit issue

Once I've assigned the issue to a team mate, I click {{% button href="" %}} **Submit new issue** {{% /button %}} to create it.

The issue has now been **opened** and given a unique number (in this case #2). 

{{< figure src="/images/ag-issue-sub-cmpl.png" >}}

{{% notice tip %}}

You can use the special **`#issue-number`** notation anywhere in GitHub's markdown (e.g. other issues, pull requests etc) to refer to it which will add a link to it automatically!

{{% /notice %}}

The issue is also now listed under the <i class="fas fa-exclamation-circle"></i> **Issues** tab.

{{< figure src="/images/ag-issue-sub-list.png" >}}

## <i class="fas fa-users"></i> Resolve assigned issue

Now that tasks have ben assigned through issues, it's **time for team mates to get to work!**

Let's **follow an example workflow by one of my team mates**, bobturneruk, who will be tackling the _add a subtract function_ issue we I just opened and assigned to him.

### Example: Resolve subtract function issue

#### <i class="fas fa-users"></i> Create `subtract` branch

{{% notice warning %}}

**Make sure to create a new branch to start work in!**

{{% /notice %}}

To begin resolving the task, Bob **first needs to creates a new branch off the `main` branch** to work in. Before that, he checks that his **<i class="fas fa-laptop"></i> local `main` branch** is in synch with the **<i class="fas fa-cloud"></i> origin `main` branch**.

{{% notice tip %}}

If your <i class="fas fa-laptop"></i> local `main` branch is behind the <i class="fas fa-cloud"></i> origin `main` branch, **click on Pull <i class="fas fa-download"></i>** to pull the remote changes to your <i class="fas fa-laptop"></i> local `main` branch.

{{% /notice %}}

Start by clicking the {{% button href="" %}} **Branch** <br> **<i class="fas fa-code-branch"></i>**{{% /button %}} button and **giving the branch an appropriate name** (`subtract`).

{{< figure src="/images/ag-sub-branch-init.png" >}}

The `subtract` branch has now been created and been **checked out** (indicated by the fact that the the **<i class="fas fa-check-square" style="color:#7CFF7E; background-color:black; padding:2px"></i> <i class="fas fa-code-branch"></i> subtract** branch in the **<i class="fas fa-laptop"></i> local** repository is now checked). 

{{< figure src="/images/ag-sub-branch.png" >}}

#### <i class="fas fa-users"></i> Add `subtract.py` file

The next step in Bob's instructions is to create a new `subtract.py` file and paste the code for the `subtract` function.

A nice feature of GitKraken is that, as well as a basic text editor, it also **allows us to create new files!**

To create a new file, **first launch GitKraken's fuzzy finder** with 
<img src="/images/command-symbol.png" width="2px" style="align:left; display:inline; margin:0;"/> **| Ctrl + P**

Next, type **File**. This launches a dropdown menu of action you can perform on files. Select **Create file**.

{{% notice info %}}

For more information check out the GitKraken documentation on [Adding a file](https://support.gitkraken.com/working-with-files/adding-and-removing/#adding-a-file) and [GitKrake's fuzzy finder](https://support.gitkraken.com/start-here/fuzzy-finder/).

{{% /notice %}}



{{< figure src="/images/ag-sub-file-create.png" >}}

Next, **type in the path to the new file you want to create**, In Bob's case it's `pythoncalculator/subtract.py` and hit **Enter|Return**.

{{< figure src="/images/ag-sub-file-fun-create.png" >}}

This **creates the new file** and **opens it up for editing!**.

Next, **paste the function code** provided in the issue instructions and save,

{{< figure src="/images/ag-sub-file-fun-edit.png" >}}

We now need to **stage and commit the new file**. Follow the steps we've been practicing and commit your file with an appropriate commit message (e.g `add subtract function`).

{{% notice tip %}}

Including the text `resolves #issue-number-you-were-assigned` will **link the issue to your pull request** and **automatically close it once your pull request has been merged!** ✨ Find out more, including additional keywords you can use to [link pull requests to issues](https://docs.github.com/en/github/managing-your-work-on-github/managing-your-work-with-issues-and-pull-requests/linking-a-pull-request-to-an-issue)

{{% /notice %}}

{{< figure src="/images/ag-sub-file-fun-commit.png" >}}

{{< figure src="/images/ag-sub-file-init-edit-init.png" >}}

{{< figure src="/images/ag-sub-file-init-edit.png" >}}

{{< figure src="/images/ag-sub-file-init-commit.png" >}}

{{< figure src="/images/ag-sub-file-test-create.png" >}}

{{< figure src="/images/ag-sub-file-test-edit.png" >}}

{{< figure src="/images/ag-sub-file-test-commit.png" >}}

{{< figure src="/images/ag-sub-push.png" >}}

{{< figure src="/images/ag-sub-pr-init.png" >}}

{{< figure src="/images/ag-sub-pr-cmpl.png" >}}





