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

Team members **allot 5-10 minutes before the call** to try to put together their tasks for the week. This involves claiming cards in "Next Up" (putting your face on them). Your cards in "Next Up" reflect your goal tasks for the week. By the call start time, all cards in Next Up should ideally be claimed. Backlog cards should only be moved to Next Up if all Next Up cards are claimed. 

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

*If you're new to Trello, see this: [https://trello.com/guide](https://trello.com/guide)*

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

1. No assigning cards to other people. Only assign cards to yourself. If you want suggest someone claim a card, @-mentioned that person.

2. Only 1 person per card in the **In Progress** list at any time.

3. A team member should have their face on a maximum of 1 card in the **In Progress** list.

4. Use the "Priority" label sparingly. Ideally no more than 1 card per category should be labeled "Priority"

5. Only the board owner should be moving cards to **Next Up** from **Backlog**.

### List descriptions

**Discussion/Ideas**

This list is where new ideas, bugs, and other to-be-defined tickets belong. Each week, this list should be cleared, either defining cards and moving to the Backlog, or to the Icebox. Any task that is not specified to the point that someone else could take your idea and run with it belongs in this list until it has been fully specified. It is your job as the card creator to see a ticket through, otherwise, the card will be added to the **Icebox** or archived after the next weekly team call.

**Backlog**

This is the running list of ready-to-go tasks that are labeled according to their category and project/domain. Cards are moved from **Backlog** to **Next Up** only during the weekly meeting, or by the Trello board owner. Cards are generally in priority order from top-to-bottom.

**Next Up**

This is the priority list of tasks to be accomplished by the team in the **next week**. No new cards should only be added if they are deemed critical to an existing card in **Next Up** or if all existing cards in the **Next Up** list have been set in motion. When you are ready to start a task in the **Next Up** list, you "add your face" to the card by adding yourself as a member.

**In Progress**

This list represents the current task being completed.

**Review**

For code-related tasks, this list is where a card goes when it has been implemented and a pull request (PR) has been made on Github. See "Git Version Control Protocol" for the process on how to do this. The code has been pushed to the code repository for review.

**Acceptance Test on Staging**

Test your feature branch on staging. Once changes are confirmed, merge to master and move the card forward.

**Ready for Production**

Cards should rarely sit here for long. When new changes are merged to `master`, it should be ready to deploy to production. Once deployed to production, move the card to the appropriate **Done** list.

Note: We try to deploy to production during standard business hours to make sure a stakeholder can be around to catch any unforseen issues. 

**Done (Week of <date>)**

When a card is complete, we move it to this list.

### Card Types (labels)

Card types should not be changed by the team. Card types are identified by ALL CAPS. These labels exist to add specification to the type of work contained in a card.

**DEV** — Code-related TODOs for the team.

**OPERATIONS / MGMT** - Dev team tasks that require setup or changes to a non-technical system.

**REVIEW / SPEC / DOCS** — label for any cards not pertaining to code, but related to the production of code.

**SYSOPS** — label for any cards to be completed by the Dev team or by SysAdmin.

### Card decorators (labels)

Card decorators can be added, removed, and changed by the team. These are labels for convenience to add filtering that is relevant to the cards in **Backlog**, **Next Up**, and **In Progress**. 

**bug** — used to identify bugs. Usually accompany the DEV card type.

Other examples of decorators: v1, v2, data migration.
