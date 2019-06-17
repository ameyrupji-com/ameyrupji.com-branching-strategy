| [Home](README.md) ▸ **Anti-Patterns** |
|-----|

# Anti-Patterns

This page lists some anti-patterns that i avoid development my development.

- [Don't develop a feature in `develop` or `master`](#dont-develop-a-feature-in-develop-or-master)
- [Don't fix a bug in `master`](#dont-fix-a-bug-in-master)
- [Don't merge your pull requests without a +1](#dont-merge-your-pull-requests-without-a-1)

## Don't develop a feature in `develop` or `master`

**Instead**: Create a feature branch off of `develop` or `master`. When the feature is developed and tested, create a pull request.

**Why?**: All code changes require a code review and verification. By opening a pull request,  I am review the code again and go through a round of testing.

## Don't fix bugs in `master`

**Instead**: Create a hotfix branch off of `master`. Write a test case, fix the bug and create a pull request.

**Why?**: Production bug fixes are super critical and it's especially important to properly review them.

## Don't merge your pull requests without a +1

I would live to have someone review my code for the following reasons.

**Why?**: _Nobody is perfect._ Having said that, we always want to make sure at least one other team member reviews our code. Performance, readability, bugs, memory leaks, etc can all be impacted by code changes and sharing the responsibility to think about all that with a team member takes pressure off your shoulders.
