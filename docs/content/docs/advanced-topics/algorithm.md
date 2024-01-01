---
title: Algorithm
weight: 22
---

## How it works

The application a unique algorithm to perform the generation of entries in EXSP

{{% steps %}}

### Impersonation

 the application tries to impersonate your profile to connect to:
    - your Outlook through the Graph API
    - MSX to retrieve opportunities
    - to EXSP to retrieve your ROSS assignments and your existing tracked hours

### Retrieve vacations

 Then it retrieves all your vacations because vacations days should not be tracked.

### Existing hours

 Retrieves all your existing hours in ESXP in case you already tracked hours manually or during a previous run.

### Outlook Calendar events

 Retrieves all your calendar events and parse them to extract relevant meetings (the ones marked with categories, the other ones are ignored).
For each of the categorized event, the app will create a labor entry matching the day, the duration and the category. (It's using the server version of outlook (GraphApi) and thus has no dependency on a specific version of Outlook client)

### 


### Fill up

 Because some managers ask you to track 40 hours of activity per week, the application can automatically create fake entry until you reach 40 hours. There are random labor entry but always matching non-customer events, and in case of customer activity (i.e. opportunity), will use a random Opportunity from your MSX.

{{% /steps %}}
