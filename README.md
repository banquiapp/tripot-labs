# Tripot
Web server for project Tripot


## Development

### Branches
It is expected to always keep 2 _static_ branches, staging and prod.
All other branches are development branches.

Main branch is intended to be the *staging* branch. It means, code is expected to be *stable*, runnable, production ready, to be deployed at any time. Yet it will point to a staging environment.

Production branch is going to be *prod*. ONLY code from 'main' can be merged into prod.

Dev branches follow the naming pattern:

* Fort new developments, name starts with 'feature/' + a short branch name, only dashes: eg. 'feature/server-setup' 
* If it is a fix, 'fix/' + short name, only dashes.

### Process
We start by creating new tickets into the [project tracker](https://github.com/orgs/banquiapp/projects/1/views/1) into the 'Backlog column' Tickets can be created into backlog at any time. As time is available we move tickets into the 'Next' column. 

A ticket is marked as in progess by being moved to the 'In progress' column. A new dev branch has to be created for such a ticket, following the branch naming convention. Once local dev has been fully completed (incliding test cases and local integration tests), the ticket wil be moved into 'In review' column, a PR is created and team members notified.

If feedback is received for a ticket, it goes back to 'In progress' and process repeats.

Once PR is approved, it can be merged into 'main', and deployed to stage env.

Once Staging tests are satisfactory, it can be merged and deployed to prod branch.