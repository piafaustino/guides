# GitHub Flavored Development Workflow

This is how we use Github to effectively collaborate and build complex projects.

This guide is just a start, and it's meant to change as we grow and learn. **If you disagree with anything, open an issue.** In the meantime, stick to the guide. Please see the [contributing guidelines](/contributing.md) for more info.

## Creating a new task, or filing a bug
- Create an issue on GithHub
- Write a description that is clear. Someone else should be able to get started on the task without needing to ask you any further questions.
- If you know who to assign the issue to, then assign it to them. Otherwise, assign it to the PM.

## You get assigned a new issue
- Make sure the task is clear enough. Run through the description and see if there are missing details.

## An issue you were assigned isn’t clear enough
- Assign the issue to someone that can clarify the task (usually the tech lead or the PM)
- Ask the questions you have about the issue as a comment in the GitHub issue page, and reference the person who can answer it (like @benigeri)
- The issue should be reassigned appropriately once it has been sufficiently clarified

## You begin work on a new GitHub issue
- Create a new feature branch: `git checkout -b new-search-page`
- Make the smallest change possible to get started with the feature and commit
- Create a pull request (*you can use [Hub](https://github.com/github/hub#git-pull-request) to do this from your terminal*!)
- Once the feature is complete and you can merge the PR

## Code reviews
- **Code reviews are highly encouraged. Never hesitate to ask for a code one. It's always beneficial.**
 - They improve our code quality and can catch our oversights.
 - We learn from the reviewer's comments, and they'll keep us accountable by pointing out when we're lazy
 - The reviewer will also learn by reading and understanding your code.
- You can ask for a code review in Slack or by tagging another team member on the PR

## Merging your PR
- Before merging, you PR must meet two requirements:
 - Your branch passes the CircleCI build
 - You have tested your code locally, and you are confident that it works without issue
- Click on the 'Merge pull request' bottom on your pull request page
- If there are merge conflicts, you'll need to rebase your branch and push it back up before you can merge it
- PRs should only be merged using GitHub

## You have a PR that will not be merged for some reason
- Type in a comment explaining the reason why
- Hit 'Close and comment' when submitting the comment

## You want feedback on some code or design decision
- Make sure your latest commits are pushed to GitHub and that you have opened a PR
- Add a comment explaining the challenge your are facing, and how someone can help
- Tag the team members that can help you

## You are blocked on a feature
- Make sure your latest commits are pushed to GitHub and that you have opened a PR
- In the description of the PR, explain:
 - What are you trying to do? (link the issue)
 - Why are you blocked?
 - What do you need to get unblocked?
- Add the `blocked` label
