---
layout: page
title: Code review
---

All code should get a review by at least one other developer before being merged.

## Performing a code review

The code review should assume that the code that is being presented for review is correct, has been tested and meets the requirements of the problem.

It is not the reviewer's job to say that the code is: correct, bug-free or appropriate.

The code reviewer is primarily responsible for deciding whether the code makes sense to them and judging whether the code will be easy to maintain in the future. The code reviewer is not responsible for the outcome of the PR being merged, only the submitter.

Examples of reasonable requests during code review:

* Asking for documentation
* Asking for unit or other tests to demonstrate functionality works as expected
* Asking for explanation of an approach in the PR
* Asking for a large PR to be broken up into smaller parts
* Asking for clarification on how a change meets the requirements

## Minimum pull request requirements

A PR should have a description that summarises the change, why it is being made and any issues or decisions that came up in the implementation but might not be obvious in the code.

A PR should have a good title that will be easy to find in a search.

If the change is primarily for user interface or styling changes, include a screenshot illustrating what the changes look like. This helps contextualise your changes.

## Large pull requests

If a change consists of more than 20 file changes then the PR should be considered as unreviewable. Sometimes changes on this scale are inevitable but always try to find ways to create smaller sequences of changes.

## Finding a reviewer

If your PR is urgent ping the #dev channel asking for a review.

If after a day your change has not been reviewed then try:

1. assigning a reviewer to the PR on Github
1. asking for a review on Slack

## For code reviewers

### Dos

* Be in favour of releasing unless you have major reservations
* Do separate whitespace changes from functional changes

### Don'ts

* Where a stylistic or convention has not been followed you only have to point out one example and not all of them
* Assume you know what the code should be doing, ask if you are not sure
* Don't get into a big comment thread with another reviewer on someone else's pull request, take the conversation onto Slack or the real-world
* Be pedantic

## For reviewees

### Dos

* When a reviewer points out a category of problem (for example using `dict` instead of the dictionary literal), check all of your pull request for the problem not just the example given
* Don't try and just address points in the review, where feedback is given consider how you might change your whole approach or change

### Don'ts

* Github will notify reviewers of changes and collapse comments on code that has changed since the comment so you don't need to confirm that each individual change has been made