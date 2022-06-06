---
title: Frequently Asked Questions
weight: 1
---

Some of the commonly asked questions encountered whilst running this course are addressed below, grouped into the main
topics. If your questions is not answered here please do not hesitate to ask the course leaders or helpers.

## Git

### I got this error: "Push main: Push failed on refs/heads/main: push declined due to email privacy restrictions"

A quick fix to this is to visit the [GitHub Email Settings](https://github.com/settings/emails) and uncheck `Block
command line pushes that expose my email`. This is not ideal though as its exposes your email address. A better solution
in the long term (described in detail on
[StackOverflow](https://stackoverflow.com/questions/43378060/meaning-of-the-github-message-push-declined-due-to-email-privacy-restrictions))
is to...

1. visit the [GitHub Email Settings](https://github.com/settings/emails) and ensure `Keep my email address private` is
   checked.
2. Copy the `{ID}+{username}@users.noreply.github.com`.
3. Open a [GitKraken CLI](https://www.gitkraken.com/cli#) window.
4. Type `git config --global user.email {ID}+{username}@users.noreply.github.com` replacing `{ID}` and `{username}` with
   the values you copied from above, then hit `Enter`.
5. Amend the author of the previous commit with `git commit --ammend --reset-author`.
6. Push the amended git with either `git push` at the Command Line Interface or using the `Push` button in GitKraken
   Client.

### Can you delete changes?

You can but typically you make subsequent commits to revert changes. It is possible to roll back a branch to any stage
in the history of commits by using `git checkout <hash_id>` but this will mean you are in a "Detached HEAD" state as you
are not at the `HEAD` of that branch. It is possible to reset which commit `HEAD` points to but it is a destructive
process and can cause a lot of problems and is not therefore recommended.

If you have not committed changes locally and only stage them you can delete changes and then stage and commit
any changes or corrections.

### If I have multiple commits do I need to push them individually?

No a push can include multiple commits.

### Why do we need to 'stage'? / What's the benefit of `stage -> commit` instead of having a direct `commit`?

It is so that we can choose which changes to which files we wish to push at a given point in time. You may have a
project where you have modified 14 files on a branch you are working on but at this point in time half of those are
still experimental and not ready to be pushed. You therefore only stage the 7 files that are ready to be pushed, leaving
the others in place locally for inclusion in a later push.


## GitHub

### Can/should data be shared on GitHub?

Technically you can, but GitHub isn't really designed for sharing large files. Further there may be data governance
issues that cover your data. For more information on sharing your data see the [Sharing research data - Research Data
Management - The University Library - The University of Sheffield](https://www.sheffield.ac.uk/library/rdm/publish).


### Wouldn't it be more meaningful if it was named "new push request"?

It depends on your perspective. When you have made changes to a fork and you wish them to be incorporated into the
original repositories branch then from your point of view you are pushing, just as you do from local to GitHub.

However, from the perspective of the original maintainer they, as recipient, see it as "pulling" your changes into their
branch. Given the original is their branch and you are adding to it then the owners perspective takes precedence, hence
why its a request to "pull" your changes into their repository.

### Can one skip forking, make a copy, and submit a PR?

You could but you may not always have permission to submit pull requests directly.

Also you should _never_ make changes directly to a `main` branch, you should always make them to a branch and then merge
that branch via a Pull Request. This helps protect the `main` branch from errors creeping in as Pull Requests get
reviewed. This is what forking is doing, its making a branch from the main repository for you to work on.

Many large code bases have a number of [GitHub Actions](https://github.com/features/actions) that carry out such tasks
as unit, and integration and regression tests, linting of code to ensure it complies to style guides, building and
releasing packages. This, along with careful code review of Pull Requests, helps ensure that newly submitted code does
not break software.

### Does Github not have a staging area?

Not when making edits directly to a single file online via GitHub as typically you are only changing a single file so
there is no need to choose which files to stage. However, rather than committing them directly to the branch you are
working on you do have the option to create a branch and pull request for your changes.


## GitKraken

### Will the trial period of GitKraken expiring be a problem? / How do I get GitKarken/GitHub pro account?

The 7-day trial period only refers to a short window where you get all of the paid features that are available to try
out. After this trial period expires you will still be able to use GitKraken and nothing in this course requires the
paid features.

If you are using a trial version of GitKraken for this course you won't encounter any problems. Longer term though you
will want to setup a GitHub account using your University email address which allows you to take advantage of their
[GitHub Campus Program](https://education.github.com/schools). If your account isn't already registered then you can
find instructions on how to do so at [Apply for an educator or researcher discount - GitHub
Docs](https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/use-github-in-your-classroom-and-research/apply-for-an-educator-or-researcher-discount).

Once you connect to this GitHub account through GitKraken you will automatically receive access to the full GitKraken
Client Stand-Alone through their [GitKraken Resources for Schools](https://education.github.com/schools), which is
contingent on your account being registered with GitHub Campus Program.


### Does GitKraken pick up files added directly to the local repository?

Yes Git and GitKraken are aware of what files are within the repository, and which files are being tracked and which
aren't and which files have changed since the last commit.

## Miscellaneous

### Will we be covering the command line interface? / How should I do this in the terminal?

No, the focus of this course is using GitKraken to interact with Git and GitHub, however the [Git
manual](https:git-csm.com/docs/user-manual.html) contains all the equivalent command line options.  There is `man git`
as well and each command has its own help page accessible with `git pull --help`, `git checkout --help` (generally its
`git <command> --help`). There are also a number of additional resources in the Links section below.
