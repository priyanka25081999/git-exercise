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

    // rebase with feature branch
    git pull origin <feature-branch-name> --rebase=true
    git pull origin <your-branch-to-be-rebased-with-feature-branch>  --rebase=true

    // Revert an author of pushed commit
    // First set the git config with the author name and email that you want to commit
    git commit --amend --reset-author

