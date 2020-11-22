
About gemfile dependencies:

Sometimes github bot complains that certain dependencies in the gem of my blog are outdated and should be upgraded. Usually the bot would automatically generate upgrading pulls (it would even email me!) and all I need to do is go to look at those pulls and click "merge" (or some button like that at the bottom of the page). Then, I'd need to update my local repository as well. This webpage shows how: https://stackoverflow.com/questions/4843881/updating-branches-using-git-pull

Basically, after the bot finishes upgrading the remote repository, I need to use the "git remote show origin" and "git status" commands to double-check the discrepancy between my remote and local repositories. Then I use "git remote update origin" to prepare for the next step (aka the pulling), after which "git status" will say "...can be fast-forwarded" -- now I can simply use "git pull" to update my local repository! After all this is done, use "git remote show origin" and "git status" again and it should detect no more discrepancy between the local and the remote repositories. :D
