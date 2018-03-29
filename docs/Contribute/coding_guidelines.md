---
id: coding_guidelines
title: Coding Guidelines
---

## Code of Conduct
> in discussion

## Issue and Pull Request Templates
> in discussion

## Style Guides
> in discussion

## Translation Strategy
> in discussion

Currently, translation is done for OCP (ValueNetwork) using transifex.  (Find the instructions.)

## Testing Guidelines
> in discussion

(Notes: Currently, there are test suites for django OCP/valuenetwork for valueaccounting and api.  These should be run when making any changes that can affect this code.  Also, the travisci testing should be kept up to date.)

## Git Flow
We use a branch and pull-request flow within the team. All changes should be made in a branch, usually created from master. A pull request should be made from the branch to master.  This gives everyone a change to see and possibly discuss each pull request. 

https://guides.github.com/introduction/flow/

Additional specifics for OCP/ValueNetwork django code: The branch called "testing" is always in testocp.  To test, merge your branch to testing and deploy that on testocp.  Once tested there, follow the above process.

## Maintenance
> in discussion
