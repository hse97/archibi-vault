create new file with 
	`touch hello_world.txt`
check status of files in the git repo 
	`git status`
	will output files not yet tracked which means the file is not staged by git 
add files to be tracked
	`git add hello_world.txt`
	adds file to the staging area in Git
	staging area is part of a two-step process for committing changes
	staging area is the waiting room for changes
	retype `git status` to show `hello_world.txt` was added \
commit with 
	`git commit -m "Add hello_world.txt` 
								this commits changes to the Git repo but does not push them 
push commits
	`git push origin main` since we are dealing with the main directory 