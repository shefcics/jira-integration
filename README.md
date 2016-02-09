# JIRA Integration

## Initial setup

This is the [JIRA version](https://confluence.atlassian.com/bitbucket/linking-bitbucket-cloud-and-github-accounts-to-jira-software-300814271.html)
of the process, which is mercifully similar to the [GitHub version](https://help.github.com/articles/integrating-jira-with-your-projects/).
JIRA Version is slightly more up-to-date as regards items in the JIRA UI.

## Workflow

Early bonus, I was able to move issue [GI-1](https://cics-jira.atlassian.net/browse/GI-1)
from the `To Do` column by using a commit message.

```
git commit -m "GI-1 #in-progress Adding links to setup docs."
```

That's pretty sweet.

## Synchronisation

Looks like JIRA periodically syncs rather than listens for post-commit pushes.
