
# Version control through Git, GitHub & GitKraken for researchers

<!-- badges: start -->
[![Netlify Status](https://api.netlify.com/api/v1/badges/a663c5ba-6e5c-4420-b8b2-4228f094463a/deploy-status)](https://app.netlify.com/sites/srse-git-github-zero2hero/deploys)
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
<!-- badges: end -->

This repo contains the source code of the website of the ***Git & Github through GitKraken - From Zero to Hero!*** course.

## Prepation for course:

### Scheduling  emails

There are up to 4 emails that need to be scheduled for this course. There are parametarised `.Rmd` templates in the `emails/` directory to generate the contents of these emails. 

- **2 weeks prior to the event - `attendance_reminder_email.Rmd`:** an attendance reminder to encourage participants who cannot attend anymore to cancel
- **1 week prior to the event - `setup_email.Rmd`:** a reminder of the setup instructors as well as information about the session platform and joining link
- **On the morning of the event - `joining_reminder_email.Rmd:`** A reminder of the joining link
- **Day after the event - `feedback_survey_email.Rmd`** a request to complete a survey. 
The parameters required are:

- `lead_instructor`: name of the lead instructor
- `session_joining_link`: link to the blackboard collaborate room (if teaching on-line)
- `event_date`: the date of the session in ISO format (`YYYY-MM-DD`)
- `event_start_time`: defaults to "10:00"
- `lunch_time`: defaults to "13:00"
- `prefilled_survey_link`: the unchanging part of the survey link containing the identifier of the date of course question to be pre-populated with the `event_date` parameter.

To use these, open each `.Rmd`, edit parameters in the YAML header and knit to render to html. The html content should then be copied (from the viewer or the generated HTML document) and pasted into the eventbrite message content box.

Make sure to send a test message to yourself and to check each link prior to finalising the email.

### Preparing the materials

To prepare for each session, materials created during the previous session need to be cleared or deleted. All steps are detailed in the [**Prepare materials for next session** GitHub Issue template])https://github.com/RSE-Sheffield/git-github-zero-to-hero/issues/new?assignees=&labels=session-setup&template=prepare-materials-for-next-session.md&title=Prepare+materials+for+session+on+%5BDATE-OR-SESSION-DESCRIPTION%5D+for+%5BINSTRUCTOR-NAME%5D). Each instructor (lead and support) should open an individual issue and complete the instructions.

### Onboarding new instructors

Similarly, there is a [GitHub Issue template for **Setting up new Lead Instructors**](https://github.com/RSE-Sheffield/git-github-zero-to-hero/issues/new?assignees=&labels=onboarding&template=setup-new-lead-instructor.md&title=Setup+New+Lead+instructor+%5BName+of+Instructor%5D). Complete instructions to ensure new Instructors have all required software and materials downloaded, installed and functional.

### Resources

The `resources` folder contains useful resources for teaching:

- `bb_comms.png`: Screenshot to demonstrate setting your status in blackboard collaborate. Upload to session and use in the introduction to make sure all participants can give feedback using status when asked questions.

***


It is powered by [Hugo](https://gohugo.io/) and the following themes:

* [Hugo theme learn](https://github.com/matcornic/hugo-theme-learn)
* [Hugo theme reveal-hugo](https://github.com/dzello/reveal-hugo)

Slides for each section are listed in the menu and opened in a new tab (thanks to a [custom menu layout](/blob/master/layouts/partials/menu.html), compared to the original Hugo learn theme).

Some Markdown content is generated with [R Markdown](https://rmarkdown.rstudio.com/), using [hugodown](https://github.com/r-lib/hugodown/).

The website is deployed by [Netlify](https://www.netlify.com/).

### Why these tools?

Why use Hugo for both the website and slidedecks, and not, say Hugo+hugodown for pages and xaringan for slides?
This way the source of slides is html produced by Hugo from Markdown content.
It allows me to use:

* downlit syntax highlighting for slides created from R Markdown with hugodown output format;
* Chroma syntax highlighting for other languages;
* emojis! `:grin:` works in slides;
* Shortcodes in slides, should I choose to.

Also, because slides are in the content, they are indexed by the Hugo learn theme so searchable!


## Credits

The workshop materials website template is based on the [hugo-theme-learn](https://github.com/matcornic/hugo-theme-learn), [reveal-hugo](https://github.com/dzello/reveal-hugo) Hugo themes and further work and configuration by Maëlle Salmon for her course site on [**Scientific blogging with R Markdown**](https://github.com/maelle/rmd-blogging-course).