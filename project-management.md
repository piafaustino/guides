# SVI's Project Management Workflow

This is how we interface with clients, run sprints, and track the progress
of our projects.

This guide is just a start, and it's meant to change as we grow and learn. **If you disagree with anything, open an issue.** In the meantime, stick to the guide. Please see the [contributing guidelines](/contributing.md) for more info.

## Sprint Timeline

### Pre-Sprint
- The PM of the project should have organized:
 - A long term list of target components, issues, and dates with the client
 - A short term list of target components and issues with the client to aim to be completed at the end of the sprint
- The PM is responsible for making sure that the short term and long term goals are driven by the feasibility assessed by engineering and balance the expecations of the client appropriately

### Day 0: First day of sprint
- All members of the engineering team get together on Skype facilitated by the PM
- PM and tech lead facilitate a the list of issues and assignment over the two weeks among engineering
- The PM should add all of the issues that need to be addressed during the sprint to a sprint milestone
- **Deliverable:** Email update to the client with finalized sprint details

### Day 7: Mid-sprint checkin
- All members of the engineering team get together on Skype facilitated by the PM
- Everybody answers:
 - What are you blocked on?
 - Are you on track to finish everything?
 - What do we expect to be able to accomplish in the next sprint?
- The sprint should be recalibrate depending on how things are going. If we're ahead, we can add some issues. If we are behind, we assess why, and cut from the sprint or deprioritize appropriately
- **Deliverable:** Email update to the client with updated sprint details:
 - What we have accomplished
 - What additional issues have arisen
 - Estimates of components that will be completed by the endo of the sprint

### Day 13: Last day of sprint
- We do a quick final checkup facilitated by the PM.
 - We only need to meet together if things don't look good. If things look good, we can simply discuss the sprint status in Slack.
- We meet with the client to:
 - Review the previous sprint
 - Prioritize, update and clarify user stories for the next sprint

## Creating issues

We use issues to track of bugs, features and everything else. We use labels to keep them organized.

### Add a type label

Add a label for the type of the issue.

#### `type: bug`
- Answer the following questions in the issue description:
 - What are the steps to reproduce the bug?
 - What is the expected behavior?
 - What is the actual behavior?
- For UI bugs, make sure to include a screenshot
- Include a stack trace if one is available

#### `type: feature`
- Features should be described as a user story.
- Break large features into several smaller ones, and keep them as self-contained as possible. Each feature should have the granularity of 1 day max— if it doesn't break it down further.
- The description should include all of the information needed to implement the feature.

#### `type: other`
- Use the other label for UI improvements, performance improvements, refactoring, security improvements, or anything else.
- We can always add new types if `type: other` becomes overused.

#### Add a priority label
- `priority: HIGH`: Critical, needs to be addressed immediately.
- `priority: med`: Important, needs to be handled in this sprint or the next.
- `priority: low`: Can wait until we have spare time.

#### Assign the issue to someone

- Each issue needs to be assigned on creation.
- If you're not sure who to assign the issue to, then assign it to the PM.


## Tracking sprint issues with milestones
* Create a new milestone for each sprint
* All of the issues that are going to be tackled during the sprint should be in the milestone, and nothing more
* The title of the milestone should follow this syntax: `Sprint 4: April 6th - 18th`
* The milestone deadline should be the last day of the sprint







