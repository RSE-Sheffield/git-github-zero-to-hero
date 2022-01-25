+++
title = "Synch local repository"
date =  2021-05-22T13:27:33+03:00
weight = 6
+++



Now, let's take a minute and go back to GitKraken Client to inspect what the repo looks like from the ground.

Right at the top of the commit graph you should see <i class="fas fa-cloud"></i> **origin `main` ahead of all other branches** and now containing **all the commits made by the entire team**.

You should **see the  <i class="fas fa-laptop"></i> local branch you used to make your contributions** in below, and likely still checked out (indicated by the <i class="fas fa-check-square" style="color:#166de0; background-color:whites; padding:2px"></i> on the branch label).

Finally, right at the bottom, you should **see your <i class="fas fa-laptop"></i> local `main` branch which is behind all other branches**. 

So let's go ahead and **synch our <i class="fas fa-laptop"></i> local `main` with the  <i class="fas fa-cloud"></i> origin `main`**.


{{< figure src="/images/ag-synch-local-view.png" >}}

## <i class="fas fa-user-circle"> </i><i class="fas fa-users"></i> Checkout `main` branch

First we need to **checkout the <i class="fas fa-laptop"></i> local `main` branch**. You can either double click on the branch label or check it out on the left panel by <i class="fas fa-check-square" style="color:#7CFF7E; background-color:black; padding:2px"></i> next to **main**. 

{{< figure src="/images/ag-synch-local-checkout-main.png" >}}

## <i class="fas fa-user-circle"></i> <i class="fas fa-users"></i> Pull remote changes

Then, click on {{% button href="" %}} **Pull** <br> <i class="fas fa-download"></i>{{% /button %}} to pull the remote changes.

This should **synch our <i class="fas fa-laptop"></i> local `main` with the  <i class="fas fa-cloud"></i> origin `main`**.

Finally, to also keep your local repo tidy and clean of any stale branches, let's also delete the local branch we worked in to contribute to the `main` branch. In my case that's the `edit-metadata` branch.

To delete it, **right click on the branch label** and then select **Delete _branch-name_**. You can also delete it through the **left panel by clicking on**  **<i class="fas fa-ellipsis-v"></i>** next to the branch name and then again, **selecting to delete**.

{{< figure src="/images/ag-synch-local-pull.png" >}}


**You should now have a nice and clean git graph with the <i class="fas fa-laptop"></i> local and <i class="fas fa-cloud"></i> origin `main` branches synched and up to date!** 🥳 🎉 ✨


{{< figure src="/images/ag-synch-local-clean.png" >}}

