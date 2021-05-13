---
title: Merging a Pull Request
weight: 9
---

### Response from the upstream repo owners

Once a PR is made, it isn’t automatically accepted. The repository owner doesn’t have to accept it, and they might even ask for changes or refuse it outright if the pull request has errors or doesn’t suit them for some reason. The owner of the upstream repository now has the opportunity to digest your pull request through a variety of tools. 

<br>

#### facility to inspect changes

For starters they have the opportunity to **inspect the changes** you have made to the code by clicking on the PR **files changed tab**. In this case they can clearly see that a whole new file was added. They can also check that the changes won't break the existing code. In this case they might check that the parameters submitted follow the guidelines set out in the exercise, ie that colour is a character vector enclosed in `"..."`. This testing process is what continuous integration systems are designed to automate.

<img src="/images/pr-filechanges.png" width="700px" />

<br>


#### facility to to respond to suggested changes

They also have an opportunity to discuss your changes in the **conversation tab**. Perhaps they are unclear about something or maybe they spotted something that needs changing. 

More often than not, you'll get a big THANK YOU! for your contribution and maybe even a :raised_hand: emoji!

<img src="/images/pr-response.png" width="700px" />

<br>

#### merge your changes

Once they are happy with your changes they can go ahead an merge them by clicking on the **Merge pull request** button.

This creates a new commit in the upstream repository, documenting the merge of your changes into thhe upstream code base.

<img src="/images/pr-merged.png" width="700px" />

<br>

