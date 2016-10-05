## Collaborating

We accept collaborations from team members and outside contributors!

We work using a feature based workflow. Understand more about this workflow here: https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow

We suggest we always use rebase when pulling new changes from the master repository. For that, set your git to always use rebase when pulling.

###### Config pull rebase only for the repository
`git config pull.rebase true`

###### Config pull rebase globally (all repositories)
`git config --global pull.rebase true`

## Commiting new code

### TL;DR
```
git checkout master
git pull # Updates master branch
git checkout <branch_name> # Checkout the branch you were working on
git rebase master # Rebase your feature branch with updated master commits
git push
git push -f # If the prior push is not possible after rebasing with master
```
Go to Github, open a Pull Request from your branch to master and wait for code review.

### Start a new feature branch

When starting to work on a new feature, we should create a new branch for it.

First update your master branch

```
git checkout master
git pull
```

Then create your new branch from the master branch

```
git checkout -b feature_title
```

Commit code on your new branch. Keep your commits concise and contextualized.

When your feature is ready, push it to the remote repository.

```
git push origin --set-upstream origin feature_title
```

Then open a pull request of your branch into master.
Access the branch Github page of this application

https://github.com/rails-projects-br/decide/branches

And click on the 'New Pull Request' branch.

Your PR will be reviewed and evaluated. It might need changes before being merged into master.

## Code styling

#### Identation

Use 2 spaces for code identation. No tabs please...

Always ident your code properly
