# Test Repo2

Created Loaclly not Remotely!
So git has no track of this project!

Check git status

## git status
    $ git status
    fatal: not a git repository (or any of the parent directories): .git

## git init
So we would do -  
    git init

This makes it as a git repo! (Beware: This creates a git repo with default branch name as - master and that could cause issues when your remote repo is called 'main' or not 'master').
So in such case, do -
    Delete the existing .git directory in the root directory of your repository.

    git init --initial-branch=<branch name>


## git status, add and commit
We can commit the files in this repo. But remember we are still commiting this repo/project locally.

## To push this to a remote repository, we do -
    $ git push origin main
    error: src refspec main does not match any
    error: failed to push some refs to 'origin'

We get an error as we had not checked-out this from any remote repository, so github does not know where to push it!

### The easiest way to fix this, is-

Create a new repo on Github, copy its clone link, then do-
    git remote add origin <cloning link of that repo>

This will add a remote repo (which is not on this machine but remotely somewhere else) as an origin to our local repo.
Also avoid extra characters at end of repo URL like '~'.

Once that is done, we can check the remote repos by typing-
    $ git remote -v

Now we can do   'git push' and that will work.
    git push origin main
             OR
We can do -
    git push -u origin main
This '-u' command sets an upstream and git knows where to push the nest time onwards.
So next time onwards, we only need to do-
    git push

## Local changes

for testing branch changes

## Use git diff
To compare what changes have been made between branches
    git diff <branch-name>

    
## Use git branch -d 
to delete the branch
    git branch -d <branch name>

## testing for merge conflict resolution

## Lets create conflict
Hello there!
have fun!

To undo staging- 
    use git reset

To undo commit-
    git reset HEAD~1
It tells git to go back to one commit earlier!