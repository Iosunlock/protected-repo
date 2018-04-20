# protected-repo
A repo to:
  * reproduce the error that occurs from someone trying to push to a branch to which they dont have acces
  * document the steps required to :point_up:
  * list the problems we should fix over in `desktop/desktop` 

## steps
_assume steps not listed explicitly are things **not** to do (where it makes sense :man_shrugging:)_

### main handle - performed on dotcom
* create a repo
* protect `master`
  * require pr reviews
  * require signed commits
* add a @iamnotwillshepherd as collaborator

### evil handle - performed in desktop
* re-sign in as @iamnotwillshepherd
  * update git information from `iAmWillShepherd` and `iamwillshepherd@github.com` :arrow_right:: `iAmNotWillShepherd` and `iAmNotWillShepherd@github.com` (remember to change back)
  
_noticed that git information didn't automatically update as I was documenting :point_up: (is this a bug?)_

* clone the repo
* make some commits to `master`
* push

## problems

### it's possible to push to a protected branch
desktop should preempt this

![2018-04-19_23-42-51 994](https://github.com/iAmWillShepherd/protected-repo/blob/master/2018-04-19_23-42-51.994.png)

The reason why this failed is in the error message, but it's not presented in a user friendly way. In the case of :point_up:, the publish button should have been disabled. We can get these permissions from the [repository endpoint](https://developer.github.com/v3/repos/#response), so it should be possible to prevent this state from occuring. Interestingly, this repo requires signed commits and I did not sign the commits made by my evil-handle, yet that was not the reason why the push failed. Shouldn't unsigned commits take precedence?
