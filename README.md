# Find me

> If you think that these can be improved in anyway, please do suggest. Pull Request are highly appreciated. Find me if you wish [@Saif(https://www.linkedin.com/in/saif-aust-cse/).

1. ### Workflow
 
    <div  style="text-align: center;">
          <img src="https://github.com/saifaustcse/Basic-git-commands/blob/main/images/workflow.png" width="750" height="450">
          <span style="padding-left: 200px;" > Workspace ↔ Staging ↔ Local Repository ↔ Remote Repository  </span>
    <div>


2. ### Configuration
   
   git config that lets you get and set configuration variables that control all aspects of how Git looks and operates.

       # Display the current Git configuration.
       $ git config --list
       
       # Set the user information when submitting code.
       git config --global user.name "Saiful Islam"
       git config --global user.email "saifaustcse26@gmail.com"
       
       # Check
       git config --global user.name
       git config --global user.email

3. ### Create a Repository in git hub/git lab

       # [How to create git hub repository.](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/create-a-repo)
       
3. ### Clone a Repository

       # Download an existing git repository to your local computer with its entire code history.
       $ git clone [url]

4. ### Add/Delete Files

       # Add the specified file to the Index.
       $ git add [file1] [file2] ...

       # Add the specified directory to the Index, including subdirectories.
       $ git add [dir]

       # Add all the files in the current directory to the Index.
       $ git add .

       # Delete the files in the Workspace and put this deletion into the Index.
       $ git rm [file1] [file2] ...

       # Stop tracking the specified file, but the file will be remained in the Workspace.
       $ git rm --cached [file]

       # Rename the file and put the renamed name into the Index.
       $ git mv [file-original] [file-renamed]


5. ### Code Submission

       # Submit the code from the Index to the Repository.
       $ git commit -m [message]

       # Submit the specified file from the Index to the Repository.
       $ git commit [file1] [file2] ... -m [message]

       # Submit the changes in the Workspace since the last commit, to the Repository directly.
       $ git commit -a

       # Display all diff information when submitting.
       $ git commit -v

       # Use a new commit to take the place of the last commit.
       # If the code doesn't have any new changes, it will be used to rewrite the commit information of the last commit.
       $ git commit --amend -m [message]

       # Redo the last commit, including the new changes to the specified file.
       $ git commit --amend [file1] [file2] ...

6. ### Branching

       # List all local branches. (the asterisk denotes the current branch)
       $ git branch

       # List all remote branches.
       $ git branch -r

       # List all local branches and remote branches.
       $ git branch -a

       # Create a new branch, but still stay in the current branch.
       $ git branch [branch-name]

       # Create a new branch and switch to the branch.
       $ git checkout -b [branch]

       # Switch to the specified branch and update the workspace.
       $ git checkout [branch-name]

       # Switch to the previous branch.
       $ git checkout -

       # Delete the branch.
       $ git branch -d [branch-name]
       
       # Delete the remote branch.
       $ git push origin --delete [branch-name]
       $ git branch -dr [remote/branch]

       
6. ### Merging

       # merge the specified branch to the current branch.
       $ git merge [branch]

       # merge a branch into a target branch
       $ git merge [source branch] [target branch]

       # Select a commit to be merged into the current branch.
       $ git cherry-pick [commit]

6. ### Tag

       # List all tags.
       $ git tag

       # Create a new tag in the current commit.
       $ git tag [tag]

       # Create a new tag in the specified commit.
       $ git tag [tag] [commit]

       # Delete the local tag.
       $ git tag -d [tag]

       # Delete the remote tag.
       $ git push origin :refs/tags/[tagName]

       # View the tag information.
       $ git show [tag]

       # Commit the specified tag.
       $ git push [remote] [tag]

       # Commit all tags.
       $ git push [remote] --tags

       # Create a new branch pointing to a certain tag
       $ git checkout -b [branch] [tag]

6. ### View Information

       # Display the changed files.
       $ git status

       # Display the version history of the current branch.
       $ git log

       # Display the commit history, and the changed files for each commit.
       $ git log --stat

       # Search commit history, according the keyword.
       $ git log -S [keyword]

       # Display all changes since a certain commit, occupying one line for one commit.
       $ git log [tag] HEAD --pretty=format:%s

       # Display all changes since a certain commit, and its "commit description" must meet the search criteria.
       $ git log [tag] HEAD --grep feature

       # Display the version history of a certain file.
       $ git log --follow [file]
       $ git whatchanged [file]

       # Display each diff related to the specified file.
       $ git log -p [file]

       # Display the past 5 commits.
       $ git log -5 --pretty --oneline

       # Display all the users who have committed, sorted by number of commits.
       $ git shortlog -sn

       # Display when and by whom the specified file was modified.
       $ git blame [file]

       # Display the difference between the Index and the Workspace.
       $ git diff

       # Display the difference between the Index and the previous commit.
       $ git diff --cached [file]

       # Display the difference between the Workspace and the latest commit of the current branch.
       $ git diff HEAD

       # Display the difference between two commits.
       $ git diff [first-branch]...[second-branch]

       # Display how many lines of code you have written today.
       $ git diff --shortstat "@{0 day ago}"

       # Show the metadata and the changed content for a certain commit.
       $ git show [commit]

       # Show the changed file for a certain commit.
       $ git show --name-only [commit]

       # Show the contents of a certain file for a certain commit.
       $ git show [commit]:[filename]

       # Show the latest commits of the current branch.
       $ git reflog


6. ### Remote Synchronization

       # Download all changes from the Remote Repository.
       $ git fetch [remote]

       # Display all the Remote Repositories.
       $ git remote -v

       # Display the information about a certain Remote Repository.
       $ git remote show [remote]

       # Add a new Remote Repository and name it.
       $ git remote add [shortname] [url]

       # Retrieve the changes to the Remote Repository and merge with the local branch.
       $ git pull [remote] [branch]

       # Push the local specified branch to the Remote Repository.
       $ git push [remote] [branch]

       # Force to push the current branch to the Remote Repository, even if there is a conflict
       $ git push [remote] --force

       # Push all the branches to the Remote Repository.
       $ git push [remote] --all

6. ### Remote Synchronization

       # Restore the specified file of the Index to the Workspace.
       $ git checkout [file]

       # Restore the specified file of a certain commit to the Index and Workspace.
       $ git checkout [commit] [file]

       # Restore all the files in the Index to the Workspace.
       $ git checkout .

       # Reset the specified file in the Index, keeping consistent with the previous commit, but remaining the workspace unchanged.
       $ git reset [file]

       # Reset the Index and workspace, keeping consistent with the last commit.
       $ git reset --hard

       # Reset the pointer of the current branch to pointing the specified commit while resetting the Index, but the workspace remains unchanged.
       $ git reset [commit]

       # Reset the HEAD of the current branch to the specified commit while resetting the Index and Workspace, keeping consistent with the specified commit.
       $ git reset --hard [commit]

       # Reset the current HEAD to the specified commit, remaining the Index and Workspace unchanged.
       $ git reset --keep [commit]

       # Create a new commit to undo the specified commit.
       # All changes of the latter will be offset by the former and applied to the current branch.
       $ git revert [commit]

       # Remove the uncommitted changes temporarily and move them in later.
       $ git stash
       $ git stash pop


6. ### Others

       # Generate a archive for releasing.
       $ git archive

9. ### References

    I have followed many articles but among them, the following articles are really helpful. Those articles helped me a lot and also encourage me to write this article according to my understanding.
 
     * [git-most-frequently-used-commands](https://medium.com/analytics-vidhya/git-most-frequently-used-commands-9df9f200c235)
     * [atlassian](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html)
     * [ercankaracelik](https://ercankaracelik.wordpress.com/2018/12/08/basic-git-commands/)
     * [tutorialdocs](hhttps://www.tutorialdocs.com/article/git-basic-command-list.html)
