---
title: A Typical Workflow
weight: 1
---

In a **typical Git + GitHub workflow**, you'll have have your work in a folder (repository) on your **<i class="fa fa-laptop" aria-hidden="true"></i> local computer** and also a linked copy on a **<i class="fa fa-cloud" aria-hidden="true"></i> remote repository** (_origin_), in this case GitHub.

You can make changes in your <i class="fa fa-laptop" aria-hidden="true"></i> local repository (most common) or your <i class="fa fa-cloud" aria-hidden="true"></i> remote repository.

- To synch the <i class="fa fa-cloud" aria-hidden="true"></i> remote repository with local changes you **Push**. 

- To synch a <i class="fa fa-laptop" aria-hidden="true"></i> local repository with remote changes you **Pull**.


{{< figure src="/images/remotes.jpg" attr="© Copyright, Jessica Lord, BSD-2" attrlink="https://github.com/jlord/git-it/" >}}


## Tracking changes

After you make changes to a file you will need to **commit them** so that Git creates a snapshot of the file at it's current state (saving the file does not commit the changes to git). To this you:

- **Add** the file to the **staging** area
- Write an **informative commit message**
- **Commit** the changes


{{< figure src="/images/git-commit-workflow.png" >}}
