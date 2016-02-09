# JIRA Integration

## Initial setup

This is the [JIRA version](https://confluence.atlassian.com/bitbucket/linking-bitbucket-cloud-and-github-accounts-to-jira-software-300814271.html)
of the process, which is mercifully similar to the [GitHub version](https://help.github.com/articles/integrating-jira-with-your-projects/).
JIRA Version is slightly more up-to-date as regards items in the JIRA UI.

JIRA Config lives at `COG > Applications > DVCS Accounts`

GitHub Config lives at `Profile Picture > Settings > Organization Settings > Applications`

## Other things I did

I think I copied Paul's fields into a new field configuration called __CiCS Modified__ [here](https://cics-jira.atlassian.net/secure/admin/ViewFieldLayouts.jspa)

Then reset __Default Field Configuration__ to defaults.

Then I made the _Affects Version/s_ and _Fix Version/s_ fields
 _optional_ instead of _required_ [here](https://cics-jira.atlassian.net/secure/admin/ViewIssueFields.jspa?atl_token=BWI2-G03T-NMRM-DOV3%7C30b0439a0ffa964fb9f6598f4fc308f8a3bc91c1%7Clin)

This was because it was complaining on the Project Backlog
page when I tried to quickly add stories


## Smart Commits are Good

Read about [the syntax](https://confluence.atlassian.com/jirasoftwareserver070/processing-issues-with-smart-commits-788729590.html)

## Workflow

Early bonus, I was able to move issue [GI-1](https://cics-jira.atlassian.net/browse/GI-1)
from the `To Do` column by using a commit message.

```
git commit -m "GI-1 #in-progress Adding links to setup docs."
```

That's pretty sweet.

## Synchronisation

Looks like JIRA periodically syncs rather than listens for post-commit pushes.
