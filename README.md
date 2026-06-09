# DKU UCC Event Workflow Demo

This repository demonstrates a folder-based event publicity workflow for DKU UCC.

## Website

Live demo: https://dku-ucc.github.io/demo-event-workflow/

## How to add a new event

1. Go to the `events/` folder.
2. Duplicate the `_template-event` folder, or create a new folder named:

   `YYYY-MM-DD-short-event-title`

   Example:

   `2026-06-15-ai-education-panel`

3. Inside the folder, create or edit `index.md`.
4. Add event metadata at the top:

```md
---
type: event
title: "Event Title"
date: 2026-06-15
time: "4:00 PM - 5:30 PM"
location: "AB 3107"
speaker: "Speaker Name"
poster: poster.jpg
---

5. Put poster images or other media files in the same folder.
6. Reference images with relative paths:

```md
---
![Event Poster](poster.jpg)
---

7. Commit changes to the main branch.
8. GitHub Actions will automatically rebuild and deploy the website.

```text
events/_template-event/index.md

---
type: event
title: "Event Title"
date: 2026-06-15
time: "4:00 PM - 5:30 PM"
location: "Room"
speaker: "Speaker Name"
poster: poster.jpg
---

## Abstract

Write the event abstract here.

## Event Details

| Item | Information |
|------|-------------|
| 📅 Date | Month DD, YYYY |
| ⏰ Time | Time |
| 📍 Location | Room |

![Event Poster](poster.jpg)
