---
title: Another Way to Collaborate
weight: 11
---

### :point_right: Give someone repository access rights!

If you are working in a team with others you trust, you can **edit repository settings so everyone who is working on the code can make commits directly to the same repository**. 

This means they will not have to make a fork, but will instead be able to just clone the repository and push changes back to it as if it was their own

Sometimes people will do this for small fixes, typos, etc. but still make pull requests for bigger changes - this allows collaborators to review your code before it's merged into the main codebase, ensuring it has enough documentation and test it for bugs.


{{% notice warning %}}
Make sure you **trust anyone you add as a collaborator**! You might want to require that all collaborators have [**Two-Factor Authentication** enabled](https://docs.github.com/en/github/authenticating-to-github/configuring-two-factor-authentication). You can also [**protect the `master` / `main` branch**](https://docs.github.com/en/enterprise/2.16/admin/developer-workflow/configuring-protected-branches-and-required-status-checks) from direct commits without review. 
{{% /notice %}}

{{% notice tip %}}
Use a [**`CONTRIBUTING.md`**](https://docs.github.com/en/github/building-a-strong-community/setting-guidelines-for-repository-contributors) file to **set out guidelines** for collaborator contributions.
{{% /notice %}}

<br>

### Adding collaborators

To add a collaborator to your repository, in your GitHub repository online, go to the <i class="fa fa-cog" aria-hidden="true"></i> **Settings** tab (top leftish), then click on the "Manage Access" link on the left hand side menu. 

![](/images/github-manage-access.png)
