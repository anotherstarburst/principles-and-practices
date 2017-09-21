---
layout: page
title: Documentation
---

## Creating documentation

Creating documentation is your responsibility not other people's. If you know something and you don't want people to constantly ask you about it: document it. If it took you a long time to figure out how something works: create the documentation you wished you had been able to read.

You can ask for someone to supply documentation during [code review](code-reviews.md) but don't make a general request, be specific about what information would be useful to understand the change.

## Where should documentation live?

If it would be helpful to find documentation where you are doing a search in the code base then that documentation should live in the project's `doc` folder.

So for example a description of a collection of classes that ties together how they work together and what their heirarchy is would be most useful if you could find it when search for one of the class names.

Documentation that you use mostly outside of the code base should be in the project wiki.

So for example: the release procedure, setting up client data or the history of decisions made in the codebase all belong in the project's Github wiki.

## Information security

Finally if some information is sensitive, for example passwords, disclosure of vulnerabilities or information relating to specific client needs or business practices, then it should be put in either a Google doc with appropriate access controls and then linked to from the project or 1Password with a description of the entry name and the vault that contains it.

This way we can have external collaborators on a project or allow access to a repo's source code without having an information security discussion.