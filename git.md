# GIT

> ### Initialize local git repository, push to the remote repository
> [article](https://jinnabalu.medium.com/initialize-local-git-repository-push-to-the-remote-repository-787f83ff999)
> - git init
> - git status
> - git add --all   # Add all files in entire repository
> - git commit -am "MY FIRST COMMIT"


> ### CUSTOM BRANCH MERGE TO MASTER BRANCH
> [article](https://stackoverflow.com/questions/9069061/what-is-the-difference-between-git-merge-and-git-merge-no-ff)
> 
> (on branch_development)
> - git merge master
> - (resolve any merge conflicts if there are any)
>
> (on master branch)
> - git checkout master
> - git merge --no-ff branch_development

> ### DICARD ALL LOCAL COMMITS ON THIS BRANCH
> In order to discard all local commits on this branch, to make the local branch identical to the "upstream" of this branch, simply run 
> - git reset --hard origin/<branch_name>

> ### DELETE LOCAL BRANCH
> - git branch -d "branch_name"

> ### DELETE REMOTE BRANCH
> - git push origin --delete "branch_name"

> ### CREATE LOCAL BRANCH
> - git checkout -b "branch_name"

> ### CREATE REMOTE BRANCH
> - git push -u origin "branch_name"


### GIT STASH ([source](https://www.atlassian.com/git/tutorials/saving-changes/git-stash))

Git stash takes your uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from your working copy
> ### VIEW
> - git stash list
> - git stash show

> ### STASHING UNTRACKED or IGNORED FILES
> Adding the -u option (or --include-untracked) tells git stash to also stash your untracked files
> - git stash -u
> 
> include changes to ignored files as well
> - git stash -a

> ### SAVE
> it's good practice to annotate your stashes with a description
> - git stash save "your message"

> ### RE-APPLYING OUR CHANGES
> reapply previously stashed changes
> - git stash pop