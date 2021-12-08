---
name: Setup New Lead instructor
about: Instructions for initial setup of a lead instructor. Required for onboarding.
title: Setup New Lead instructor [Name of Instructor]
labels: onboarding
assignees: ''

---

Documentation for most setup instructions is available in the course material [**setup**](https://srse-git-github-zero2hero.netlify.app/setup/) chapter.

- [ ] Install git
- [ ] Create GitHub account
- [ ] Install GitKraken
- [ ] Sign-in to GitKraken with GitHub account.
- [ ] Ensure SSH keypair for accessing GitHub is configured in GitKraken.
- [ ] Clone [`RSE-Sheffield/collaborative_github_exercise` repo](https://github.com/RSE-Sheffield/collaborative_github_exercise). Clone it to somewhere where you won't get it mixed up with the fork you will clone during teaching.
- [ ] Ensure you have admin access to `RSE-Sheffield/collaborative_github_exercise`
- [ ] Open RSE-Sheffield/collaborative_github_exercise project in Rstudio
- [ ] Run `renv::restore()` to install dependencies.
- [ ] Test that you can knit `plot_trait_evolution.Rmd` succesfully. _If it succeeds, it's fine to revert the resulting `plot_trait_evolution.html` to it's previous state instead of committing the changes. However, make sure they are cleared in the git tab one way or the other so as not to confuse the demo._
