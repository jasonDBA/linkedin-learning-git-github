# linkedin-learning-git-github

## What have you learned from the course?

### Resource
* http://themasterworld.com/git-three-tree-architecture-key-concepts/
* https://www.linkedin.com/learning/git-essential-training-the-basics/

### Three trees architecture in Git
* Working Directory - Staging Index - Repository

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

### Git Commands
* __$git status__ displays the state of the working directory and the staging area.
* __$git diff__ to view changes you added to your worktree and staging area from the last commit.
* __$git diff --staged__ only shows changes to the files in __"staging"__ area.
* __$git diff --color-words__ used to highlight the changed parts only (NOT entire paragraphs but more specific parts).
* __$git rm__ used to remove a file from a Git repository.
* __$git mv__ this often is used to __rename__ files.
