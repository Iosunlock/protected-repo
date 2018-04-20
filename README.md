# protected-repo
A repo to: 
  * reproduce the error that occurs from someone trying to push to a branch to which they dont have acces
  * document the steps required to :point_up:

## steps
* create a repo
* protect `master`
  * require pr reviews
  * require signed commits
* add a collaborator
* clone the repo (as collab)
* make some commits to `master`
* push
