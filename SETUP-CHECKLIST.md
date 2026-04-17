# Setup checklist — delete this file when done

Welcome! This website was just generated from the DSL course template. Complete
the steps below to customise it for your course. Everything is editable via
the **GitHub web editor** — no command line needed.

Estimated time: 30-45 minutes total, spread over the first week of setup.

---

## 1. Course identity (5 min)

Edit [`_config.yml`](_config.yml):

- [ ] Replace `course_name` with your course name and code, e.g. `"Deep Learning (GRAD-E1394)"`
- [ ] Write a one-paragraph `course_description`
- [ ] Confirm `course_semester` is correct (e.g. `"Fall 2026"`)
- [ ] Confirm `github_org` matches your course org
- [ ] Uncomment `content_repo` and point it at `https://github.com/{your-org}/content-f{YYYY}`

Commit — the site will rebuild automatically.

## 2. Instructor and TA details (5 min)

Edit [`_data/people.yml`](_data/people.yml):

- [ ] Replace `"Instructor Name"` with the instructor's real name
- [ ] Add a `webpage:` URL (e.g. the Hertie faculty profile)
- [ ] Add each TA under `teaching_assistants:` with name + optional webpage
- [ ] Add each faculty assistant under `faculty_assistants:` (if applicable)
- [ ] (Optional) Upload profile photos to `_images/pp/` and reference them via `profile_pic:`

The home page auto-renders the people sections once the data is in place.

## 3. Session schedule (15-30 min)

For each lecture, create a file `_lectures/NN_topic.md` (where NN is the session number):

```markdown
---
type: lecture
date: 2026-09-10
title: "Session 1: Introduction"
tldr: "Short one-line description of what this session covers."
thumbnail: /static_files/presentations/lec.jpg
links:
    - url: https://github.com/{your-org}/content-f{YYYY}/blob/main/lectures/session-01.pdf
      name: slides
---
**Required Readings:**
- [Reading 1 title](https://github.com/{your-org}/content-f{YYYY}/tree/main/readings/required/session-01)

**Optional Readings:**
- Textbook Chapter X
```

- [ ] Delete the sample file `_lectures/01_introduction.md`
- [ ] Create one file per session

The schedule page auto-generates from these files in date order.

## 4. Assignments (10 min)

For each assignment, create a file `_assignments/NN_name.md`:

```markdown
---
type: assignment
date: 2026-09-17
title: "Assignment 1: Problem Set 1 (10%)"
classroom_link: ""
due_event:
    type: due
    date: 2026-10-01T23:59:00+01:00
    description: "Problem Set 1 due"
---
Description of the assignment and what students need to submit.
```

- [ ] Delete the sample file `_assignments/01_sample_assignment.md`
- [ ] Create one file per assignment
- [ ] (Optional) Once you've created a GitHub Classroom assignment in your satellite org, paste its invite URL into `classroom_link:`. A "Accept assignment on GitHub Classroom" button will appear on the assignment page.

## 5. Content uploads (week-by-week)

These go in the **content repo** (`content-f{YYYY}`), not here:

- [ ] Upload the course syllabus (PDF) to the content repo root
- [ ] Upload lecture slides to `lectures/`
- [ ] Upload required readings to `readings/required/session-NN/`
- [ ] Upload optional readings to `readings/optional/session-NN/`

You can do this via drag-and-drop in the GitHub web UI, or push via git. Upload
progressively as the semester unfolds — the website links will start working as
soon as files are committed.

## 6. Student roster (5 min)

When you have your class list with GitHub usernames, edit:

- [ ] `semesters/f{YYYY}/hertie-semester.yml`
- [ ] Add each student under `students:` as `- github_username`
- [ ] Add instructors and TAs under `instructors:` (if not already handled by the setup workflow)

Push — the sync workflow runs automatically and creates/updates the `students-f{YYYY}` team in the satellite org.

## 7. Delete this file

When steps 1-6 are complete:

- [ ] Delete this `SETUP-CHECKLIST.md` file. It's a setup aid, not production content.

---

## Reference

- Faculty workflow overview: [../gh-org-strategy/docs/for-faculty/semester-workflow.md](https://github.com/hertie-data-science-lab/gh-org-strategy/blob/main/docs/for-faculty/semester-workflow.md)
- Roster file format: [../gh-org-strategy/docs/for-faculty/roster.md](https://github.com/hertie-data-science-lab/gh-org-strategy/blob/main/docs/for-faculty/roster.md)
- Assignment workflow: [../gh-org-strategy/docs/for-faculty/assignment.md](https://github.com/hertie-data-science-lab/gh-org-strategy/blob/main/docs/for-faculty/assignment.md)

Stuck? Contact Henry Baker (@henrycgbaker, h.baker@hertie-school.org) or open an issue in [hertie-data-science-lab/.github](https://github.com/hertie-data-science-lab/.github).
