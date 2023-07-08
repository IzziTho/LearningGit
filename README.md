# Learning Git

## Creating a local Git repository 

1. using GitBash, navigate to your local folder
2. Initialise the folder with `git init`

3. using the URL to your GitHub repo, link your local repo with GitHub: `git remote add origin {remote URL}`

## Making a commit and pushing

1. Make the change locally. Save.
2. Get the status of local branch `git status`
3. Identify which file to commit `git add {file name}` 
4. add a description `git commit -m "description"`
5. push the commit to the remote (github) `git push origin main`

The change will now be in your history on Github


## Feature Branching

1. Pull the main branch, make sure it's the most up to date `git pull`
2. To check which branch you're on: `git branch`
3. to create a new branch (check the standard naming process for your company): `git checkout -b {branch name}`
4. Make your changes, commit and push. Then make some more changes and don't push.
5. Create a pull request(PR) on GitHub, assign a reviewer.
6. Reviewer will review the PR and make comments. 
7. Resolve comments and re-commit and push.
8. Reviewer will approve and merge the pull request. 

9. Make sure you're back onto the main branch `git checkout main`
10. and it's up to date with `git pull`

## Resolving conflicts

1. While working on a feature branch, which has been created from main, main has been updated because another developer has pushed commits to main in the meantime.
1. When i create a pull request, it can not automatically be merged because there are conflicts. 
1. I need to bring my feature branch inline with main. 
1. Checkout back to main branch `git checkout main`
1. Bring main up-to-date: `git pull`
1. Checkout back to your feature branch `git checkout {branchname}`
1. Merge main into your feature branch `git merge main`
1. Conflicts will show in your code. Review these, confer with the other developer to resolve these. 
1. Commit the changes made in your branch. `git add .`, then `git commit` which will open editor, `esc`, `:wq`
1. Push to your branch `git push origin {branchname}`

Pull request can now be merged