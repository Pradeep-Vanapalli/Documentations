WHAT IS GIT?
	Free and Open Source version control system.

WHAT IS VERSION CONTROL?
	The Management of changes to documents, computer programs, large websites, and other collection of information.

TERMS:
	=>Directory - Folder
	=>Terminal or Command Line - Interface for Text Commands
	=>CLI - Command Line Interface	
	=>cd - Change Directory
	=>Code Editor - Word Processor for writing code
	=>Repository - Project, or the folder/place where your project is kept
	=>Github - A website to host your repositories online

GIT COMMANDS:
	=>Clone - Bring a repository that is hosted somewhere like Github into a folder on your local machine
	=>add - Track and save your files and changes in Git
	=>commit - Save your files in Git
	=>push - Upload Git commits to a remote repo, like Github
	=>pull - Download changes from remote repo to your local machine, the opposite of push.

HOW TO USE COMMANDS:
	=>git clone "git hub link" - to download the files into local machine
	=>cd "folder name from repo" - to get into that folder to do any changes
	=>ls -la - to see all folders in that particular folder
	=>git init - to initiate the git repo
	=>git add . -  to track all the files in the folder
	=>git status - to track the chnages in the folders
	=>git commit -m "Need to type message about changes"  - to give any explantion about the chnages we made.
	=>git push origin master - To push the changed files to repo

IF WE WANT TO PUSH THE LOCALLY CREATED FILES TO GITHUB:
	=>We need to create one empty repo in Github with same name which is available in local machine.
	=>git remote add origin 'link of that git repo'
	=>git remote -v - To know which are all repos we have connected
	=>git remote set-url --add --push origin "URL" - to change the repo to connect
	=>git push -u origin master - to push the files to repo

GITHUB WORKFLOW:

	WRITE CODE ====>COMMIT CHANGES ====>MAKE A PULL REQUEST

LOCAL GIT WORKFLOW:

	WRITE CODE ====>SAVE CHNAGES (git add) ====> COMMIT CHANGES (git commit) =====> PUSH CHANGES(git push) ====> MAKE A PULL REQUEST

GIT BRANCHING:
	=>git branch - to check the how many branches and present where we are
	=>git checkout -b 'branch_name' - to create branch and enter into that branch
	=>git checkout master - to go to the master branch
	=>git status - to check the status of the file after some chnages in it.
	=>git add 'the_filename_we_made_chnages' - to save chnages we made
	=>git commit -m "message we need to write" - to add message about chnages we made
	=>git diff 'branch name'  - to check the changes in the file we made
	=>git push -u origin 'branch name' - to push the cide to the branch

***So if we want to merge the code from branch to the master we need create the Pull Request***

HOW TO CREATE PULL REQUEST AND MERGING MANUALLY IN GITHUB?
	=>Go to compare&pull request and click on that.
	=>Add description about the chnages we made.
	=>Click on create Pull Request.
	=>Go to 'Files chnage' bar in the pull request - to add comment in the file by clicking on the '+' symbol at the chnage we made.
	=>Go 'Conversation' bar and click on Merge Pull request button.
	=>Merging sucessfull done as we go to master branch and check.
	=>git pull - to pull down the repo to local machine.

HOW TO DELETE BRANCH?
	=>git branch -d 'branch name'
	
HOW TO DO CHNAGES IN BOTH MASTER AND CHILD BRANCH AND MERGING?	
	=>git checkout -b 'branch_name' - to create branch and enter into that branch
	=>git status - to check the status of the file after some chnages in it.
	=>git diff 'branch name'  - to check the changes in the file we made
	=>git commit -am "message we need to write" - to add message and save chnages about chnages we made(basically adds and comits at the same time), It only works for modified files
	
***Along with child branch if we changed anything in the master branch***
	
	=>git checkout master
	=>git branch - should be at master branch
	=>git checkout 'branch name' -  It will throw an error as we have made some changes in master branch so we nee to commit them first
	=>git status - to check the status of the file after some chnages in it.
	=>git commit -am "message we need to write" - to add message and save chnages about chnages we made(basically adds and comits at the same time), It only works for modified files
	=>git checkout 'branch name' - To go to the branch
	=>git diff master - to check the changes in the file we made-when we are in brach 
	=>git merge master - to merge master into the branch
			*If we face any issue saying conflict we need to go to that master file and need to do same chnages then
			*git status
			*git diff
			*git commit -am "message we need to write" 
			
UNDOING IN GIT:
	=>If we made any changes incorrectly, to delete or undo those
		*git add 'file name we made changes'
		*git status
		*git reset
		*git status
	=>If i want to undo commit 
		*git add 'file name we made changes'
		*git commit -m "message about changes"
		*git reset HEAD - to undo the last commit.
		*git reset HEAD~1 - to undo the last but one commit4
		*git status
		*git diff
	=>To undo a specific commits
		*git log - To see all commits
		*git reset 'commit name'
		*git reset --hard 'commit name' - to get rid of all commits before certain point.
		
FORKING:
	=>If we want to push other's repo into our github, we need to do forking manually.
	=>Then we need to create pull request
	=>we can see that repo in our github
