+++
title = "Advanced Collaboration Intro"
date =  2021-05-20T12:51:43+03:00
weight = 1
+++

In this chapter we'll move on to a more advanced but far more realistic collaborative workflow where contributions are made by team mates that are all collaborators on the same repository.

We'll be:
-  working in branches off the `main` branch (similar to forks but internal to the repository).
- pull requests to contribute code back to the `main` branch
- employing code review of pull requests
- deploying continuous integration to run automatic tests and checks on pull requests
- practicing resolving code conflicts between pull requests.



## Github Workflow



{{< figure src="/images/ag-github-flow.png" >}}

Branching is a core concept in Git. There's only one rule: **anything in the `main` branch is always deployable (i.e. it works!)**.





it's extremely important that your new branch is created off of main when working on a feature or a fix. Your branch name should be descriptive, so that others can see what is being worked on.


{{<mermaid>}}
%%{init: { 'logLevel': 'debug', 'theme': 'base', 'gitGraph': {'showBranches': true,'showCommitLabel': false}} }%%
gitGraph
    commit
    commit
    commit
    commit
    commit
    branch feature
    checkout feature
    commit
    commit
    checkout main
{{</mermaid>}}
