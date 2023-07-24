## Git rebase:

    // add upstream
    git remote -v
    git remote add upstream <url>
    git remote -v

    // main rebase
    git checkout main
    git branch
    git log
    git fetch upstream
    git rebase upstream/main
    git log
    git push -f origin main

    // rebase local branch
    git checkout -b <local_branch>
    git log
    git rebase main
    git log
    git status
    git push -f origin <local_branch>

    // change the base branch to new branch
    git rebase --onto new-base-branch current-base-branch
