# ameyrupji.com-branching-strategy

This document is the current branching and release strategy for websites developed for ameyrupji.com. It provides a guideline of the two release models that I am using: [release deployment](RELEASE-DEPLOYMENT.md) and [continuous deployment](CONTINUOUS-DEPLOYMENT.md).

These workflow tries to streamline the development process to build my website.

List of common scenarios encountered during development and how I apply these branching strategies is listed below.


## Purpose

As my website is growing and expanding, I would like to maintain consistency across repositories showcasing experience in branching strategy. Alignment across the various repositories increases productivity.

This repository and its documentation outline the process for:
* Developing features
* Creating a release
* Performing hot fixes when required and
* Anything else related to branching strategy


## Project Types

Depending on the type of project, I am using one of two branching strategies:

### Release Deployment

I have used this strategy for projects where features get bundled into a release and then deployed together.

[Learn more](./RELEASE-DEPLOYMENT.md)

### Continuous Deployment

I have used this strategy for projects where features get deployed as soon as they're ready.

[Learn more](./CONTINUOUS-DEPLOYMENT.md)

Though I have mostly used the release deployment strategy I am trying to move to a continuous deployment Strategy.


### Protected Branches

GitHub supports [Protected branches](https://github.com/blog/2051-protected-branches-and-required-status-checks). Protected branches:
- Can't be force pushed
- Can't be deleted
- Can't have changes merged into them until required status checks pass

`master` and `develop` branches are protected. These protected branches should never be directly committed to. They should only be updated through PR merges.

Projects that have continuous integration with a service such as CircleCI should have their `master` and `develop` (if applicable) branches protected by a status check requiring CircleCI builds to pass before changes can be merged.


## Branch Naming

`master` and `develop` are always named exactly that. For a feature, bugfix or hotfix with a is related to a ticket I prefer that the branch name start with the keyword `feature/`, `bugfix/` or `hotfix/` followed by ticket number and a small description (eg. `GH-7-add-header-bar`). Branch names should use dashes to separate words of the name and should not contain any `.` (dots) as this is used to generate the urls for feature branch testing.

Other than that, choose names that are descriptive and concise. You don't need a branch name that is a novel because most branches should be relatively short-lived (hours to days, not weeks).


## Anti-Patterns

Some of the [Anti-Patterns](ANTI-PATTERNS.md) that I try to avoid in my development processes.
