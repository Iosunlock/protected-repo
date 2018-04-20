# protected-repo
A repo to:
  * reproduce the error that occurs from someone trying to push to a branch to which they dont have acces
  * document the steps required to :point_up:

## steps
_assume steps not listed explicitly are things **not** to do (where it makes sense :man_shrugging:)_

main handle - performed on dotcom
* create a repo
* protect `master`
  * require pr reviews
  * require signed commits
* add a @iamnotwillshepherd as collaborator

evil handle - performed in desktop
* re-sign in as @iamnotwillshepherd
  * update git information (remember to reset to `iAmWillShepherd` and `iamwillshepherd@github.com`)
  
_noticed that git information didn't automatically update as I was documenting :point_up: (is this a bug?)_
* clone the repo
* make some commits to `master`
* push
