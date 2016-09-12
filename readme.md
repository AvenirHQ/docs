# About this document

Avenir has grown significantly in the first year of our existence. This document is where we document our process and protocol for how we work and why. While this document might contain references to a process that exists for a certain project or team at Avenir, please defer to any instructions or process found in the documentation for a particular project.

The format, the content, and the organization are all subject to change. Everything here is always open for discussion. Open a PR or issue to kick off a discussion.

---------

# The tools we use

### generally:

- Slack
- Trello
- Google Drive
- Google Calendar
- Google Hangouts
- Toggl (for time tracking and reporting)
- Lastpass (for shared team passwords and credentials)
- Helpscout

### for code-related tasks:

- Github
- Heroku
- AWS
- Mailchimp + Mandrill
- 3rd party APIs (see specific projects for details)
- Programming language agnostic (see specific projects for details)

### for design-related tasks:

- Sketch
- Adobe Creative Suite (Photoshop, InDesign, Illustrator)
- Balsamiq
- Gliffy (or other diagramming tool of choice)

### sparingly:

- Doodles (for scheduling team meetings/calls)

---------

# Communication

## Team Communication

We use a few tools for regular team communication and have some general rules for determining when to use one tool over the other. 

### For urgent matters: Prefer Slack

You need an answer soon because you're blocked on something important, a substantial bug has been discovered, etc.

If it is urgent, use Slack.

_Note: Slack should be used for ephemeral messages between teams, groups, and individuals. We currently have the free tier for Slack as it suits our operational needs. This means that only the 10k most recent messages are searchable/visible in Slack._

### For everything else: Prefer Trello

Otherwise, if the team member is not online, you should just @-mention them on Trello.

If they are online you should feel OK with using Slack. But be mindful that you might be interrupting their flow.

On the flip side, if a team member pings you over Slack about a non-urgent issue, you should feel OK holding off a response to their inquiry if you're in the midst of deep focus.

### Outliers to the rule

- We use the conversation and inline comments in Github Pull Requests to provide specific feedback during code review, but always give high level feedback and the final word to the contributor in a Trello ticket so other team members can easily follow along as needed.
- In spec documents (these will be Google Docs), we use the Comments feature to directly mention team members or clients for feedback. High level changes and directions that the team should be aware of belong in a Trello comment as well.
- We use email sparingly, but when we do, it's primarily for:
  - sending contracts or paperwork between Avenir and a team member
  - non-product related, asynchronous communication 

## Client communication

We value effective communication and believe that a healthy separation between client stakeholders and the general team leads to better productivity and efficiency.

- The only dedicated channel of communication we have with client stakeholders is via email or scheduled Hangout or phone call.
- Client stakeholders have access to view all Trello boards and team work product at any time, and can add comments to docs or Trello cards when requested as part of review and feedback.
- Team members and contractors responsible for regularly communicating with client stakeholders should their @avenirhq.com email address for regular communication. 

## Emergencies

Any emergency is handled by the Avenir HQ team, and should not require immediate development changes/fixes. 

In the event that there is a critical bug that blocks normal use of the application, we will establish a protocol with the client as to how to handle the situation from a customer management standpoint.

> Unless explicitly stated otherwise in a contractor agreement, normal hours and availability are all that are required of any team member.

---------

# Meetings

Our process is oriented around the basis of our team being completely distributed. We try to organize our process in such a way that we require as few meetings as possible while maintaining a high level of productivity.

- Every week we hold a team-wide meeting for about an hour on Google Hangouts.
- Every other week, all team members have an individual 1:1 with a Partner at Avenir.
- Meetings outside of these required meetings can be scheduled as needed.

> Note: if a team member is client facing, there is also 1 stakeholder call per client per week that is held that they will often be responsible for leading or attending.

## Weekly Call Format

In every Trello board, there is a card titled "Avenir Team — Weekly Call Notes" with a link to the agenda document. This document follows the general format for the call:

### Before the call

Team members should **allot 5-10 minutes before the call** to review their assigned cards in the "Next Up" list.

Your cards in "Next Up" reflect your goal tasks for the week. By the call start time, all cards in Next Up should ideally be claimed. Backlog cards should only be moved to Next Up if all Next Up cards are claimed. 

Any notes, questions, or feedback should be added to appropriate cards in the Trello board. If there is a point for discussion that falls outside the focus of a card that exists, a new card should be added the "Ideas and Discussion" list. The creator of the discussion card should be the "member" on the card to ensure it gets addressed during their turn in the retrospective.

### 1. Nags and Brags

We start every call with every team member sharing some personal updates. A "nag" is something negative that a person wants to share, and a "brag" is something positive that a person wants to share. Updates should not be work related, but otherwise, anything is fare game!

### 2. Housekeeping and availability

Updates to the team process are shared here and any feedback on how we can improve our process for the week can be addressed at this time. Team members will add any noted changes to availability in the next week to this section as well as to the Team Google Calendar.

### 3. Retrospective

The team lead will start the retrospective process. Using Trello, we filter the cards for the individual doing their retrospective, and from right to left (completed to next up) the team member will review where their tasks stand for the week and raise any blocking issues or questions.

### 4. Quick review of remaining Next Up tickets

If there are any tickets in Next Up that are not assigned by the end of the retrospective process, we take a moment to address that before we start the week.

## 1:1s

One-on-ones are a chance for team members and partners to get regular facetime to address big-picture goals, issues, and updates. There is not a set format for this call, but this is a time to address non-product thoughts that should be addressed.

The format is a regular bi-weekly 20 min call that is required for all active contractors and team members.

---------

# Trello

*If you're new to Trello, see this: [https://trello.com/guide](https://trello.com/guide)*.

## Usage tenants

1. It is the source of truth

    If anybody wants to know the state of any project, they should be able to find out in a glance on Trello.

2. All team members start their shifts in Trello

    When beginning a block of Avenir time, a team member always opens Trello and makes sure their cards are current.

    In addition, everyone **clears out their Trello notifications at this time**. This means responding to all @-mentions.

3. Developers end their shifts in Trello

    Even if the session was unproductive, team members should be in the habit of making their closing ritual adding any updates to Trello. It can be as simple as: "Looked at this bug — hit a wall with X, will revisit tomorrow."

    These little updates keeps Trello relevant as the source of truth.

4. @-mention if you want attention.

    If you don't @-mention someone, assume they won't see it. In a discussion on a Trello card, all relevant parties should be @-mentioned.

## Board rules

1. No assigning cards to other people. Only the team leads should assign cards to other members. If you want suggest someone claim a card, @-mention that person.

2. Only 1 person per card in the **In Progress** list at any time.

3. A team member should have their face on a maximum of 1 card in the **In Progress** list.

4. Use the "priority" label sparingly. Ideally no more than 1 card per member should be labeled "priority"

5. Only the board owner should be moving cards to **Next Up** from **Backlog**.

## List descriptions

### Reference

Most Trello boards will have a reference list as the first list. These are cards with discussions or links to spec documents that are notable for all project team members to be aware of.

### Discussion/Ideas

This list is where new ideas, bugs, and other to-be-defined tickets belong. Each week, this list should be cleared, either defining cards and moving to the Backlog, or to the Icebox. Any task that is not specified to the point that someone else could take your idea and run with it belongs in this list until it has been fully specified. It is your job as the card creator to see a ticket through, otherwise, the card will be added to the **Icebox** or archived after the next weekly team call.

### Backlog

This is the running list of ready-to-go tasks that are labeled according to their category and project/domain. Cards are moved from **Backlog** to **Next Up** only during the weekly meeting, or by the Trello board owner. Cards are generally in priority order from top-to-bottom.

### Next Up

This is the priority list of tasks to be accomplished by the team in the **next week**. No new cards should only be added if they are deemed critical to an existing card in **Next Up** or if all existing cards in the **Next Up** list have been set in motion. When you are ready to start a task in the **Next Up** list, you "add your face" to the card by adding yourself as a member.

### This Week

Sometimes, as a deadline approaches, the team may use this list to help prioritize upcoming tasks for the next week. In this case, This Week takes over for Next Up, and Next Up becomes a more high priority backlog. This list is also useful in weekly calls, where the team can see what was actually done vs. what was planned for the previous week.

### In Progress

This list represents the current task being completed.

### Review

When a task has been completed in part or in full, the card should be moved by the card owner to the "Review" list and a reviewer directly notified that a review is needed with an @-mention. 

For code-related tasks a pull request (PR) in Github will accompany the move to the "Review" list.

### QA on Staging — _For code-related Trello boards only._

When a code-related change is ready for QA review, move the card to "QA on staging" and notify a member responsible for QA with an @-mention. By default team leads are responsible for QA unless there is a dedicated QA resource for the project. 

Once changes are confirmed, merge to master and move the card forward.

### Ready for Production — _For code-related Trello boards only._

Cards should rarely sit here for long. When new changes are merged to `master`, it should be ready to deploy to production. Once deployed to production, move the card to the appropriate **Done** list.

> Note: We try to deploy to production during standard business hours (Pacific Time) to make sure a stakeholder can be around to catch any unforeseen issues.

### Done (Week of ...)

When a card is complete, we move it to the appropriate "Done" list.

### Icebox

When a card is been deemed out of scope for the project, it is preserved in the "Icebox" for later reference. This is a list used mostly be the board master. 

## Card Types (Trello labels)

Card types should not be changed very often to avoid confusing the team. Board masters will occasionally update labels for card types when project requirements dictate. 

Card types Trello labels written in ALL CAPS. These labels exist to add specification to the type of work contained in a card.

**DEV:API** — Code TODO that includes backend code requirements.

**DEV:CLIENT** — Code TODO that includes frontend/client code requirements.

**REVIEW/SPEC/DOCS** — label for any cards not pertaining to code, but related to the production of code.

**SYSOPS** — label for any cards to be completed by the Dev team or by SysAdmin.

## Card decorators (labels)

Card labels might change frequently. These are labels for convenience to add filtering that is relevant to the cards in **Backlog**, **Next Up**, and **In Progress**. 

### Rules for decorators (labels)

- Card decorators should always accompany a "card type" 
- decorators should not use the same color as a card type if possible
  - ask the board master if there is more specificity needed or reorganization of labels.

> A label that is common to most boards will be the **priority** label. This is usually RED, and should be the only label that uses the RED color. 

---------

# Designer best practices

## File directory structure for design work

Because wireframes, assets, designs and other docs can change so frequently, we want to ensure we're doing things in a way that allows for others to see the most up-to-date changes. We do this a few ways:

- When sharing versions of a design or asset, we have a directory structure that allows the most recent version to be linked to at all times. Something like this:

```
"Login Wireframes"
 |- file_design_v3.png <-- current draft
 |- archive/
    |- file_design_v2.png
    |- file_design_v1.png
 |- source/
    |- assets/
       |- file_design_source_file_v1
       |- file_design_source_file_v2
```

Note: `file_design_v3.png` is the file we want our team to see, but as versions change, that single file will be archived, and v4, v5, etc. will replace it.

> Link to the Google Drive **folder** when sharing or attaching to a Trello card, not the file.

--------

# Developer best practices

## General rules

- Process described in a project repo takes precedence over the parent/general docs.

## Code Reviews

- If you're requesting a code review (CR), you're responsible for getting the review. It's also your task to move the card across the finish line.
  - You might need to ping around on Slack or Trello to determine who will be available to perform the review.
- Code contributions should always include:
  - relevant code comments
  - relevant tests
  - updated readme to reflect domain-specific knowledge relevant to the code changes
  - updated db seeds or factories to ensure reviewers and QA folks can efficiently test your code. 

## Tests and CI

- Make sure you've been added to any private deploy or CI Slack channels for a project when starting. These are usually called `clientname-bots`
- tests and CI will change from project-to-project, so check the project readme for what process we're following.

## Git protocol

In general, use rebases and squashes to keep the Git history clean. Avoid merge commits and extraneous progress commits.

We subscribe to the overall flow outlined here: [https://github.com/AvenirHQ/guides/tree/master/protocol/git](https://github.com/AvenirHQ/guides/tree/master/protocol/git).

> If it's on `master`, it should be on production. The `HEAD` of `master` should match production unless a project-specific workflow says otherwise.
