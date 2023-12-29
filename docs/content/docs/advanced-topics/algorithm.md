---
title: Algorithm
weight: 22
---

## How it works

The application a unique algorithm to perform the generation of entries in EXSP

1- the application tries to impersonate your profile to connect to:
    - your Outlook through the Graph API
    - MSX to retrieve opportunities
    - to EXSP to retrieve your ROSS assignments and your existing tracked hours

2- then it retrieves all your vacations to mark days without tracking

3- retrieves all your existing hours in EXP

4- retrieves all your calendar events and parse them to extract relevant meetings (the ones with categories, the other ones are ignored).
For each of the categorized event, create a labor entry matching the day, the duration and the category.

5- 