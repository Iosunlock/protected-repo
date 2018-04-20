# protected-repo
A repo to: 
  * reproduce the error that occurs from someone trying to push to a branch to which they dont have acces
  * document the steps required to :point_up:

## steps
1. create a repo
1. protect `master`
  1. require pr reviews
  1. require signed commits
1. add a collaborator
1. clone the repo (as collab)
1. make some commits to `master`
1. push
