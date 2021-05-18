+++
title = "Team formation and Repo setup"
date =  2021-05-13T17:57:41+03:00
weight = 1
+++

## Team formation

For this chapter, we're going to be **working in groups of 3-4 participants**. I'm going to allocate these groups randomly by sending you to break out rooms. Within your break out rooms, you will have **5 mins** to introduce yourselves and decide on a **group owner**. 

#### The group owner <i class="fas fa-user-circle"></i> will:

- be the main administrator of the project 
- be the one that makes a copy of the template repository
- will be setting up repository permissions and adding collaborators.
- will open issues for the rest of the team to work on and assign them to members of the team.
- will be reviewing the code, merging pull requests and handling merge conflicts.

#### The rest of the team <i class="fas fa-users"></i> will:

- be assigned a specific task (issue).
- create a new branch to work in.
- follow the instructions in their assigned issue to complete the task in their branch.
- create a pull request from their branch to the new `main` branch.
- make any corrections requested by the owner.

## Complete team details

Once you have decide on a team repo owner, please copy the template provided in the course [collaborative notepad](https://docs.google.com/document/d/1-CkHO417wtfJZ35X4q5tk_hcgP9W3mfEG5AsN2SIU1A/edit?usp=sharing) and complete your team's details

#### Template

> **Team members (github usernames):** <br>
> **Team repo URL:** <br>
> **Team repo owner (github username):**  


## <i class="fas fa-user-circle"></i> Make a copy of project template

The project we will be working with and contributing to will be based on the repo: https://github.com/RSE-Sheffield/python-calculator

This is slightly different than the previous repository we worked with in that it has been set up as a template. As such we don't fork the repository. Instead we make a copy of the template.

The **project owner of each team will make a copy of the template** and the rest of the team will **contribute to their own team copy of the repository**.

To make a copy, first click on the {{% button href="https://github.com/RSE-Sheffield/python-calculator/generate" %}}**Use this template** {{% /button %}} button

{{< figure src="/images/ag-use-tmpl.png" >}}

For consistency, use the same name **`python-calculator`** for your own team projects. Add `Basic calculator functions in python` as the repo description.

{{< figure src="/images/ag-create-tmpl.png" >}}


Create your copy and the details of your team repository to the collaborative notepad so your team mates can access it.

## <i class="fas fa-user-circle"></i> Protect the `main` branch

{{% notice info %}}

You can create a branch protection rule to enforce certain workflows for one or more branches, such as requiring an approving review or passing status checks for all pull requests merged into the protected branch.
People with admin permissions to a repository can manage branch protection rules.

{{% /notice %}}

Click on **<i class="fas fa-cog"></i>  Settings** on the top-right of the repo.

On the left-hand navigation bar, go to **Branches**


Next, under **Branch protection rules** click on the {{% button href="" %}}**Add rule** {{% /button %}} button

{{< figure src="/images/ag-br-protect-rule.png" >}}

In the **Branch name pattern field**, enter **`main`**. This will apply the rule to any branch whose name matches the pattern `main`.

Next we'll apply a branch protection rule. Under **Protect matching branches**, check the **Require pull request reviews before merging** checkbox. Leave the **Required approving reviews** as **1**. 

{{< figure src="/images/ag-br-protect-rule-add.png" >}}

This rule means that all contributions to the main branch will have to be made from a separate branch through a pull request and will also require at least one approving review from a team member before it is merged. This means that at least one other person will have a look at any code contributed to the main branch, adding the opportunity to catch any errors before they are merged.

{{% notice info %}}

Find out more about [Branch protection rules](https://docs.github.com/en/github/administering-a-repository/managing-a-branch-protection-rule)

{{% /notice %}}
## <i class="fas fa-user-circle"></i> Add your team mates as collaborators

Next, each team owner will add the rest of the team members as collaborators.

{{% notice info %}}

For each repository that you administer on GitHub, you can see an overview of every team or person with access to the repository. From the overview, you can also invite new teams or people, change each team or person's permissions, or remove access to the repository.

{{% /notice %}}

Still under **<i class="fas fa-cog"></i>  Settings** , on the left-hand navigation bar, go to **Manage access**

Click on the {{% button href="" %}}**Invite a collaborator** {{% /button %}} button.

{{< figure src="/images/ag-collaborator-new.png" >}}

Next, search for your team mates' github username and once you've found your team member, select their acccount to add.

{{< figure src="/images/ag-collaborator-new-search.png" >}}



Once selected, click on the {{% button href="" %}}**Add _team-member-username_ to this repository** {{% /button %}} button.

{{< figure src="/images/ag-collaborator-new-add.png" >}}

The team member you added will now be visible on the **Manage access** panel and will show a **Pending invite** status until they accept the invitation.



{{< figure src="/images/ag-collaborator-new-pending.png" >}}

#### <i class="fas fa-redo-alt"></i> Repeat the process untill all team members are added.

{{% notice info %}}

Find out more about [Managing teams and people with access to your repository](https://docs.github.com/en/github/administering-a-repository/managing-teams-and-people-with-access-to-your-repository)

{{% /notice %}}

## <i class="fas fa-users"></i> Accept the invitation to the repository

Before we move on, **make sure the rest of your team has accepted the invitation to the repository**.

{{< figure src="/images/ag-collaborators-all.png" >}}