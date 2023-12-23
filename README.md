# Commits

A commit should be a wrapper for related changes. Don’t mix concerns, keep your commits “atomic”. For example, creating two different components should produce two separate commits. Producing small commits makes it easier for other developers to understand the changes and what context/concern the commit is related to.

Commits should **never crash** the application. For example, you did a refactor that changed the payload. You need to apply this to all codes. This approach is related to having atomic commits. It's the same for tests. You shouldn't create a new commit to adding tests for something you are adding.


## Challenge

Currently, our application has one endpoint and its tests. Your challenge is to create two new endpoints for our application. You need to append two new endpoints to the existing open api file and their tests.

## Answer

[Click to see the answers.](ANSWERS.md)