---
name: Schedule emails for next session
about: Instructions for scheduling emails ready for next session. To be completed
  by lead instructor
title: Schedule emails for session on [DATE-OR-SESSION-DESCRIPTION] for [INSTRUCTOR-NAME]
labels: session-setup
assignees: ''

---

Emails need to be scheduled via eventbrite ahead of each session.


### Emails
There are up to 4 emails that need to be scheduled for this course. There are parameterised `.Rmd` templates in the `emails/` directory to generate the contents of these emails.

- **2 weeks prior to the event - `attendance_reminder_email.Rmd`:** an attendance reminder to encourage participants who cannot attend anymore to cancel
- **1 week prior to the event - `setup_email.Rmd` / `setup_email_two_day.Rmd`:** a reminder of the setup instructors as
  well as information about the session platform and joining link, which to use depends on whether the course is running
  on one or two days.
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


### Blackboard Collaborate Session
- Go to [Blackboard Collaborate](https://vle.shef.ac.uk), logging in via MUSE,
- Under `Organisations` open `COM - Research Software Engineering`,
- Select `Create Session` and fill in the details as follows:
  - Session Name: `git & GitHub through GitKraken - from Zero to Hero!`
  - Guest Access: :heavy_check_mark:
  - Make sure that `Guest role` is set to `participant`
  - Set the start and end dates and times suitable for the session, add 30 mins to 1hr extra onto the scheduled end time.
  - Early entry: 15 minutes before start time.
- Click `create`, this will create the session link, make a note of this for the emails.


### Checklist
Complete as necessary (dependent on what has been created in the past).

**Tick off tasks as they are completed or if they are not required.**
- [ ] attendance reminder email
- [ ] set up blackboard session
- [ ] setup email (appropriate for one or two day course)
- [ ] joining email
- [ ] feedback email

Once all tasks are complete, please close issue.
