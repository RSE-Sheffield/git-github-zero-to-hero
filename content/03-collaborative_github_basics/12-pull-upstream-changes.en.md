---
title: Pulling Upstream Changes
weight: 12
---

Now that everyone has contributed to the [**RSE-Sheffield** repository](https://github.com/RSE-Sheffield/collaborative_github_exercise) (the **upstream** repository), the `params/` folder contains a number of files, one for each successful pull request.

This is also clear form the commit locator

However your local copy of the repository only contains the template and your own file. 

> Q: How can I merge changes from the **upstream** repository to my **local** repository?

GitKraken makes it really simple. 


### Add the **Upstream** Remote repository

On the left side menu bar, hover over the **<i class="fa fa-cloud" aria-hidden="true"></i> REMOTE** menu until a small {{% button icon="fas fa-plus" %}}{{% /button %}} button appears.

<img src="/images/gk-hover-add-remote.png" />

This should open the **<i class="fa fa-cloud" aria-hidden="true"></i> Add Remote** Tab. Select the **`RSE-Sheffield/collaborative_github_exercise`** repository from the **GitHub Repo** dropdown menu and click the {{% button %}}**Add Remote**{{% /button %}}  button.

<img src="/images/gk-add-remote.png" />

Once added, the RSE-Sheffield repository will be visible under the **<i class="fa fa-cloud" aria-hidden="true"></i> REMOTE** menu

<img src="/images/gk-remote-added.png" />


### Pull upstream changes

To pull the upstream changes from the **`RSE-Sheffield`** repository, **grab** the **`RSE-Sheffield`** button from the history panel and drag it over to your <i class="fa fa-laptop" aria-hidden="true"></i> local `master` branch until a **<i class="fas fa-crosshairs"></i>** icon appears next to it and **drop**.

<img src="/images/gk-pull-upstream.gif" />

Once you drop it onto the <i class="fa fa-laptop" aria-hidden="true"></i> local `master` branch successfully, a pop up menu will appear. Select **Fast-forward master to RSE-Sheffield/master**. That ensures that you **do not create a circular commit of your initial commit** to the upstream repo when you are merging it back into your <i class="fa fa-laptop" aria-hidden="true"></i> local repo. Find out more about [fast-forward git merging](https://ariya.io/2013/09/fast-forward-git-merge).

<img src="/images/gk-fast-forward.png" />

Once the merge is complete, your <i class="fa fa-laptop" aria-hidden="true"></i> local `master` will now be showing as synched with the **`RSE-Sheffield`** remote

<img src="/images/gk-local-synched.png" />

and you will have copies of all the files contributed in your `params/` folder! :tada:

<img src="/images/gk-local-synched-files.png" />



### Synch **origin** remote

The **origin** remote is **your fork of the repository** that's labelled with your GitHub profile avatar. As you can see, **it is now lagging behind** the upstream remote and your <i class="fa fa-laptop" aria-hidden="true"></i> local copy which are now both in sync. That's because it's still missing all the files contributed by the other participants.

To synch your **origin** remote, <i class="fa fa-arrow-up" aria-hidden="true"></i> **Push**  the changes you've just pulled into your <i class="fa fa-laptop" aria-hidden="true"></i> local repository.

<img src="/images/gk-all-synched.png" />

> ### Once you've pushed, all the repositories should now be showing as synced. :tada:

## Run the analysis

To run the analysis, open the project in Rstudio, click on the `plot_trait_evolution.Rmd`, then click on the Knit button. This should render including everybody's species! See more on [Rmarkdown notebooks](https://rmarkdown.rstudio.com/authoring_quick_tour.html#Overview) 
