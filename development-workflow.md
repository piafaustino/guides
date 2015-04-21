# GitHub Flavored Development Workflow

This is how we use Github to effectively collaborate to build complex projects. This guide is just a start, and it's going to evolve with our team. 

**If you disagree with anything, open an issue.** We'll debate it and think of alternatives to improve our workflow. In the meantime, stick to the guide.

## Creating a new task 
- Create an issue on GithHub
- Write a description that is clear. Someone else should be able to get started on the task without needing to ask you any further questions.

## You get assigned a new Github issue
- Make sure the task is clear enough. Run through the description and see if there are missing details.

## An issue you were assigned isn’t clear enough
- Assign the issue to whoever is best suited to clarify the task (usually the tech lead or the PM)
- Write question as a comment in the GitHub issue page, and reference the person who can answer it (like @benigeri)

## You begin work on a new GitHub issue
- Create a new feature branch: `git checkout -b new-search-page`
- Make the smallest change possible to get started with the feature and commit
- Create a pull request 

## You answered someones questions for a task
- Assign the task back to the person who asked you the question

## You need your code to be reviewed
**This means that the code is at a point where it is good to be merged. You just want a sanity check on what you have written.**
- Assign an `PR:awaiting review` label to your PR
- If possible, add a comment on the PR to reference the person on your team who can best review your PR (this could be main author of a file you've edited, the UI expert, the security expert, etc...)

## You have code related questions about your task
- Create a checklist of unanswered question in your PR *at the top of the description*
- If the question requires a long architectural discussion, then create a separate issue and link to the issue in your checklist
- Assign the `PR:question` label to your PR
- If you are blocked assign the `PR:blocked` label. Consider what caused you to get blocked in the first place.

## Code review process
**Should be done 2-3 times per day** (start of day, after lunch, end of day might work for you)
- Go through all `PR:question` PRs 
- Go through all `PR:awaiting review` PRs
- Merge all of your `PR:looks good` PRs and close the related GitHub issue
- Process all of the `PR:answered` PRs 
  - Check off the answered questions
  - If any questions have not been answered move from `PR:answered` to `PR:question` again
  - If all of the questions have been answered, remove the `answered` label
- Process all of the `PR:needs work` labels
  - If the changes take under 15 minutes, make them right away
  - If the changes take longer, use your judgement

### Reviewing an awaiting review PR
- Read through the code and answer any questions
- Write comments on individual lines when giving feedback
- If the code looks good
  - Add `PR:looks good` label to the PR
- If the code needs changes made before merging
  - Add `PR:needs work` label to the PR
  
### Answering questions for a PR
- Reference the person in a GH comment
- Answer any related issues
- Mark the PR as `PR:answered`
- If the answer was sufficient
  - The submitter of the PR should remove the `PR:answered` label
- If the answer wasn't enough
  - The submitter should remove the `PR:answered` label and add the `PR:question` label back

## You have a PR that will not be merged for some reason
- Type in a comment explaining the reason why
- Hit 'Close and comment' when submitting the comment

## Github PR Tags
These are all of the PR tags and what they are used for. 

- **`PR:looks good`**

  The PR has been reviewed and everything looks good.

- **`PR:needs work`**

  This PR needs has some required changes before merging.

- **`PR:awaiting review`**

  The PR needs someone to take a look at it for feedback.

- **`PR:question`**

  The PR has questions that needs to be answered.
  
- **`PR:Answered`**

  The PR had questions which are now answered. This needs to be approved by the one who asked the question.

- **`PR:blocked`**

  This PR is currently blocked. The person working on this needs something before he can continue.