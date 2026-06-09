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
