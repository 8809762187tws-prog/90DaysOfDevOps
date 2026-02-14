

1. What is the difference between git add and git commit?

   git add - converts untracked files to staged.
   git commit - converts staged files to tracked.

2. What does the staging area do? Why doesn't Git just commit directly?

   staging has files which are selected to commit , files here can be reviewed before commiting.

3. What information does git log show you?

   Git log shows history of commits.

4.What is the .git/ folder and what happens if you delete it?

  It is a git repo. If .git folder is deleted , the files will not get deleted , git will no longer recognize the folder as agit repo.

5.What is the difference between a working directory, staging area, and repository?

  A working directory - It is a place where we create , edit and update files.
  
  Staging area - It is a place where selected files are stagged for commit.

  Repo - Here files are saved permanently.(history is maintained)
