---
layout: page
title: Code review
---

All code should get a review by at least one other developer before being merged.

## Performing a code review

The code review should assume that the code that is being presented for review is correct, has been tested and meets the requirements of the problem.

It is not the reviewer's job to say that the code is: correct, bug-free or appropriate.

The code reviewer is primarily responsible for deciding whether the code makes sense to them and judging whether the code will be easy to maintain in the future.

Examples of reasonable requests during code review:

* Asking for documentation
* Asking for unit tests to demonstrate functionality works as expected
* Asking for explanation of an approach in the PR
* Asking for a large PR to be broken up into smaller parts

## Minimum pull request requirements

A PR should have a description that summarises the change, why it is being made and any issues or decisions that came up in the implementation but might not be obvious in the code.

A PR should have a good title that will be easy to find in a search.

## Large pull requests

If a change consists of more than 20 file changes then the PR should be considered as unreviewable. Sometimes changes on this scale are inevitable but the code reviewer is not responsible for the outcome of the PR being merged, only the submitter.

## Dos

* Do separate whitespace changes from functional changes