# Setup for Episode 10:  Pull Requests
This episode has been re-written at the start of 2025. It was based on https://carpentries-incubator.github.io/git-novice-branch-pr/10-pull-requests/ 
This episode still relies on learning in Episode 5: Remotes in GitHub https://nclrse-training.github.io/git-ultra-novice/05-github/index.html.  
### Summary:
Using web interface only, create a branch, copy a file and update (for chosen country), commit and pull request
update the file (add largest city) and commit, observe pull request is updated
instructor accept pull request
### Extension 1 (offline) - in person if the first part is completed quickly, or as 'homework'
clone the same repo locally
switch to your branch
update the file (add national dish)
commit and push your branch
go online to do pull request


## Before the workshop
* check the 'countries' repo https://github.com/NclRSE-Training/countries
* Add a field for learners name & GitHub ID in collab doc

## lunchtime
enrol participants as collaborators on 'countries' repo

## After the workshop

### Revert Countries Repository
https://github.com/NclRSE-Training/countries
_(NB this repository will be reset in a few days time so that we can use it for our next course)_

remove outside collaborators https://github.com/NclRSE-Training/countries/settings/access?query=filter%3Aoutside_collaborators

Robin Wardle
5 Feb 2025 4:01 PM
I've reset the countries repo, 
## procedure:
#### Github
- Disable branch protection rules in GitHub Repository Settings

#### In local terminal:

1. cd to local repo (clone if necessary)
2. `git pull`
3. `git reset --hard v1.0.1` (v1.0.1 is the last "stable" tag, if we update the repo we will need a newer tag)
4. `git push origin +main` (forces a HEAD reset)
#### On GitHub
6. Re-enable branch protection rules in GitHub Repository Settings
7. Delete all the student-created branches (this will also delete pending attached pull requests) in GitHub Repository
8. Revoke all the student collaborator permissions in the GitHub Organization

```
I haven't done the last step yet in case any of the students did want to practice on the repo again. Maybe do that next week.
This is why I didn't want to get into resetting a repo in the lesson, it's moderately complex when dealing with GitHub.
`git revert` will reset the HEAD but it does this by undoing each commit in turn, adding each older commit as a new commit which preserves the history. This can cause merge conflicts and be otherwise a headache.
`git reset` removes history but you need to force the change. I can't actually remember what `git rebase` does!
```
