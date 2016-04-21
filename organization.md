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

For most projects, an emergency is handled by the Avenir HQ team, and should not require immediate development changes/fixes. 

In the event that there is a critical bug that blocks normal use of the application, we will establish a protocol with the client as to how to handle the situation from a customer management standpoint. Normal hours and availability are all that are required of the dev team at this time.

## 👀 Code Reviews

**If you're requesting the CR, you're responsible for getting the review**. It's still your task to move the card across the finish line.

You might need to ping around on Slack or Trello to determine who will be available to perform the review.

## 🌲 Git

In general, use rebases and squashes to keep the Git history clean. Avoid merge commits and extraneous progress commits.

We subscribe to the overall flow outlined here: [https://github.com/AvenirHQ/guides/tree/master/protocol/git](https://github.com/AvenirHQ/guides/tree/master/protocol/git).

## 👷 CI & tests

TBD

## 📞 Weekly call

Every week we hold a team-wide meeting for about an hour on Google Hangouts.

In the team Trello board, there is a card titled "Weekly Call" with a link to the relevant agenda document.

### Before the call

Any notes, questions, or feedback **can be added to the agenda** in advance of the call for the team to discuss.

Team members **allot 5-10 minutes before the call** to try to put together their tasks for the week. This involves claiming cards in "Next Up" (putting your face on them). Your cards in "Next Up" reflect your goal tasks for the week. By the call start time, all cards in Next Up should ideally be claimed. Backlog cards should only be moved to Next Up if all Next Up cards are claimed. 

> No worries if your tasks for the week are not clear. They can be compiled during the call.

## 💻 Code

###  Linters

We will use ESLint for all JS code.

> `.eslintrc` to be constructed.

## 🚢 Deploys

### DeployBot

For projects using DeployBot, we utilize a `staging` branch in git that is watched by DeployBot.

Staging deploy:

1. Rebase and squash changes onto `staging` branch
2. Access Avenir Deploybot: [https://avenirhq.deploybot.com/](https://avenirhq.deploybot.com/)
3. Navigate to correct Repository > Environment (in this case environment is `staging`)
4. Click "Deploy"
5. Because of the way DeployBot works, after staging environment has been used for QA, be sure to use the "Rollback to ..." button to "reset to `master`".
6. After DeployBot Rollback has finished, reset git branch `staging` to `master`. **Warning: Be sure to roll back in Deploybot BEFORE you reset branch `staging` to `master` as Deploybot will break trying to track changes on a branch that has been pushed with `--force`. **


Production deploy: 

1. Follow github protocol here for merging reviewed code changes: [https://github.com/AvenirHQ/guides/tree/master/protocol/git](https://github.com/AvenirHQ/guides/tree/master/protocol/git).
2. Access Avenir Deploybot: [https://avenirhq.deploybot.com/](https://avenirhq.deploybot.com/)
3. Navigate to Repository > Environment (in this case environment is `production`)
4. Click "Deploy"
5. After successful deploy to production, follow "Staging deploy" instructions to match staging environment to production environment. 


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

## Authorize.Net

If you're going to be doing a lot of Authorize.net work, it's recommended that you make your own sandbox account.  You can register for one [here](https://developer.authorize.net/hello_world/sandbox/).  Then you can log in at [sandbox.authorize.net](https://sandbox.authorize.net).

**NOTE:** Right when you make your account, the response page will have your API Login ID and API Transaction Key.  Save these values, because they are hard to get back if you don't save them the first time around.

Other things to know:

- DPM = Direct Post Method, this is using an html form to submit directly from the client to AuthorizeNet
- SIM = Server Integration Method, this is basically just a server sending CC info to their API directly
- CIM = Customer Information Manager, this isn't even an integration method.  This just refers to saving customer payment info on AuthorizeNet servers.
- Our v2 RRG API is going to use SIM and CIM.
- You can whitelist URLs for DPM in the AuthorizeNet settings.  Under **Transaction Format Settings**, click **Response/Receipt URLs**.
- It seems that most of the settings around DPM exist in the **Transaction Format Settings** and generally don't apply to us.
- In the AuthorizeNet settings, **MD5-Hash** is actually just a secret string that gets appended to transaction information before it gets hashed.  That hash can then be used to verify the authenticity of the AuthorizeNet server.
- There are also **Address Verification** and **Card Code Verification** in the **Security Settings** that will probably be helpful.

