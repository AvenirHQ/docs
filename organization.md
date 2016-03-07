# Team organization

## 📄 This document

Everything here is always open for discussion. Open a PR or issue to kick off a discussion.

## 👥 Communication: Slack vs Trello

When you're reaching out to a specific individual...

### For urgent matters: Prefer Slack

You need an answer soon because you're blocked on something important, a substantial bug has been discovered, etc.

If it is urgent, use Slack.

### For everything else: Prefer Trello

Otherwise, if the team member is not online, you should just @-mention them on Trello.

If they are online you should feel OK with using Slack. But be mindful that you might be interrupting their flow.

On the flip side, if a team member pings you over Slack about a non-urgent issue, you should feel OK holding off a response to their inquiry if you're in the midst of deep focus.

## 🚨 Emergencies

In the event of an emergency, use text or phone to reach team members who are needed.

Jason will be providing on-call service for the ISR app during business hours. He will be in charge of routing requests to the appropriate team members.

## 👀 Code Reviews

**If you're requesting the CR, you're responsible for getting the review**. It's still your task to move the card across the finish line.

You might need to ping around on Slack or Trello to determine who will be available to perform the review.

## 🌲 Git

In general, use rebases and squashes to keep the Git history clean. Avoid merge commits and extraneous progress commits.

We subscribe to the overall flow outlined here: [https://github.com/thoughtbot/guides/tree/master/protocol/git](https://github.com/thoughtbot/guides/tree/master/protocol/git).

## 👷 CI & tests

TBD

## 📞 Weekly call

Every week we hold a team-wide meeting for about an hour on Google Hangouts.

Find the agenda for the weekly call [here](https://docs.google.com/document/d/1oeM1sDIcoUU-1SHuxmGdPJIH-TTbteFH4dyVZFEKF-4/edit).

### Before the call

Any notes, questions, or feedback **can be added to the agenda** in advance of the call for the team to discuss.

Team members **allot 5-10 minutes before the call** to try to put together their tasks for the week. This involves moving cards from "Backlog" to "Next Up" and putting your face on them. Your cards in "Next Up" reflect your goal tasks for the week.

> No worries if your tasks for the week are not clear. They can be compiled during the call.

## 💻 Code

###  Linters

We will use ESLint for all JS code.

> `.eslintrc` to be constructed.

## 🚢 Deploys

### Staging

We deploy branches to staging.

1.  It's wise to **rebase your branch on top of `master`** before deploying to staging.

2. Check Slack to see if anyone else has a "mutex" on staging. If not, announce that you're taking staging and then kick off the deploy.

3. When you're done using staging, deploy `master` to staging.

4. Announce to Slack that you are releasing your mutex.

> No need to use `@here` or `@channel` as folks interested in using staging will always check Slack first.

### Production

* If it's on `master`, **it should be on production**. The `HEAD` of `master` should match production.
* Announce deploys to Slack.

> Coming soon: Deploy hooks that post to Slack.

## 🔮 Trello

### Usage tenants

1. It is the source of truth

    If anybody wants to know the state of any project, they should be able to find out in a glance on Trello.

2. Developers start their shifts in Trello

    When beginning a block of Avenir time, a team member always opens Trello and makes sure their cards are current.

    In addition, everyone **clears out their Trello notifications at this time**. This means responding to all @-mentions.

3. Developers end their shifts in Trello

    Even if the session was unproductive, developers should be in the habit of making their closing ritual adding any updates to Trello. It can be as simple as: "Looked at this bug — hit a wall with X, will revisit tomorrow."

    These little updates keeps Trello relevant as the source of truth.

4. @-mention if you want attention.

    If you don't @-mention someone, assume they won't see it. In a discussion on a Trello card, all relevant parties should be @-mentioned.

### Board rules

1. No assigning cards to other people. Only assign cards to yourself. If you want someone to assign themselves to a card, mention that person.

2. Only 1 person per card in the **In Progress** list at any time.

3. A team member should have their face on a maximum of 1 card in the **In Progress** list.

4. Use the "Priority" label sparingly. Ideally no more than 1 card per category should be labeled "Priority"

### List descriptions

**Discussion/Ideas**

This list is where new ideas, bugs, and other to-be-defined tickets belong. Each day, this list should be cleared, either defining cards and moving to the Backlog, or to the Icebox. Any task that is not specified to the point that someone else could take your idea and run with it belongs in this list until it has been fully specified. It is your job as the card creator to see a ticket through, otherwise, the card will be added to the **Icebox** or archived.

**Backlog**

This is the running list of ready-to-go tasks that are labeled according to their category. At our weekly meeting, we will select what cards from this list are added to the **Next Up** list to be completed in the next week.

**Next Up**

This is the priority list of tasks to be accomplished by the Lussier team in the **upcoming week**. No new cards can be added unless they are deemed *Critical* or if all existing cards in the **Next Up** list have been set in motion. When you are ready to start a task in the **Next Up** list, you "add your face" to the card by adding yourself as a member.

**In Progress**

This list represents the current task being completed.

**Review**

For code-related tasks, this list is where a card goes when it has been implemented and a pull request (PR) has been made on Github. See "Git Version Control Protocol" for the process on how to do this. The code has been pushed to the code repository for review.

**Acceptance Test on Staging**

When a pull request has been approved and merged into master, we deploy the code to staging, and notify the project stakeholders to review and approve.

**Ready for Production**

When a project stakeholder has approved the changes on staging, they move the card to **Ready for Production** and notify the developer who "owns" the card. The card is ready to deploy to production, and the card can be moved to **Done (Week of <date>)**

**Done (Week of <date>)**

When a card is complete, we move it to this list.

### Label descriptions

**DEV** — label for any cards to be completed by the Dev team pertaining to development.

**DESIGN** — label for any cards to completed by the Dev team pertaining to design.

**ADMIN** — label for any cards not pertaining to code, but related to the production of code.

**SYSOPS** — label for any cards to be completed by the Dev team or by SysAdmin.

**Priority** — can be considered a decorator label that should only exist with an ALLCAPS category label.
