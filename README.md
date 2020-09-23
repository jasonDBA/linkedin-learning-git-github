# linkedin-learning-git-github

## What have you learned from the course?

### Resource
* http://themasterworld.com/git-three-tree-architecture-key-concepts/
* https://www.linkedin.com/learning/git-essential-training-the-basics/

### Three trees architecture in Git
* Working Directory - Staging Index - Repository
* NOTE: Once you add the files to staging area, you can keep track of all changes in the file.

### Git Workflow
1. __$git init__ Create a working directory (.git)
2. Make the changes
3. __$git add .__ Add the changed file in the staging index
4. __$git commit -m "Initial Commit"__ Commit the changed file to the repository
* NOTE: You can see all history of the changes by checking out the commits

### Head Values (SHA-1)
* A specific ID the file gain when we commit it in the Git three trees architecture.
* We can track our values by the help of this specific ID
* __HOW?__ When the file is added to our repo, Git generates __the checksum__ for each change and the checksum algo __converts data into a simple number.__ If we change something, the data changes, meaning the checksum changes as well.


### Setting up Git Online Repository
1. Sign up for an account either at Bitbucket (https://bitbucket.org) or GitHub (https://github.com).
2. Set the local Git repository to set its remote origin:
```
$git remote add origin <repository URL>
```
3. Pushing your commits to the online repository
```
$git push -u origin master
```
4. Cloning an online repository
```
$git clone <repository URL>
```

### Git Commands
* __$git status__ displays the state of the working directory and the staging area.
* __$git diff__ to view changes you added to your worktree and staging area from the last commit.
* __$git diff --staged__ only shows changes to the files in __"staging"__ area.
* __$git diff --color-words__ used to highlight the changed parts only (NOT entire paragraphs but more specific parts).
* __$git rm__ used to remove a file from a Git repository.
* __$git mv__ this often is used to __rename__ files.

### Git Stage and Commit Shortcut
* Typically, you can go through two phases to commit the files as follows:
1. __$git add .__ Add all the files from your working dir to the staging area
2. __$git commit -m "Your Message"__ Commit the files to your repo
* Alternatively, there is a shortcut instead -> __$git commit -am "Your Message"__

### How to see the difference of the previous commit?
1. Type __$git log__. It will show all logs of your commit with reference ID
2. Type __$git show [reference ID] --color-words__. Can see the difference of the specified commit. --color-words will allow you to see only specific changed parts.

### How to write multi lines of commit?
1. Type __$git commit -a__ or __$git commit -all__
2. Will move to VI mode
3. Enter __i__ to insert your commit lines
4. Once completed, press __esc__ to escape
5. Type __:wq__. __w__ used to save the commit and __q__ used to quit the vi mode
6. Type __$git log__ to verify the multi lines of your commit

### How to undo working directory changes?
* If you change something in the file by accident or on purpose, you can always __retore back__ by using:
* $git checkout -- <file name>
* This is used to discard changes in working directory.

### How to unstage files?
* $git reset HEAD <file name>
  
### How to modify the most recent commit?
* $git commit -amend -m "Your Modified Message"
* It lets you combine staged changes with the previous commit instead of creating an entirely new commit.
* It can also be used to simply edit the previous commit message without changing its snapshot.

### About .gitignore
* List of rules to determine which files to ignore
* The purpose of using this is to ensure that certain files not tracked by Git remain untracked
* It follows a pattern format - meaning a __regular expression__
* Examples & More Details: https://git-scm.com/docs/gitignore

### How to ignore tracked files?
* If you have already completed to add the file and commit the change, the file is being tracked.
* In this case, even though putting the name of the file into .gitignore, all changes of the file is being tracked as it is already in a staging area.
* To ignore this tracked file, you can use the following command:
* $git rm --cached <file name>
  
