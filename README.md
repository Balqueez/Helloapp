HelloApp
========
A simple Node.js application containerized with Docker, versioned with Git, and
integrated using Jenkins.

## Project Setup
-------------

Step 1: Repository Initialization
---------------------------------
Created a new local project and initialized a Git repository.
      git init

Step 2: Project Files
---------------------
- Created a simple index.js file that runs a basic "Hello World" Node.js app.
- Created a Dockerfile 
- Created a Jenkinsfile

Step 3: Connect to Remote Repository
------------------------------------
Created a repository on GitHub named HelloApp.
      git remote add origin https://github.com/Balqueez/HelloApp.git

Step 4: First Commit & Push
---------------------------
       git add .
       git commit -m "Initial commit"
       git push -u origin master
At this point, neither .gitignore nor README.md was created.

Step 5: Create Branches
------------------------
       git checkout -b dev
       git checkout -b feature
       git branch [to check the branches]

Pushed both to remote:

       git push origin dev
       git push origin feature

Step 6: Pull Requests & Merge
-----------------------------
- Opened Pull Requests on GitHub to merge changes from dev and feature into master.
- Merged successfully using the GitHub interface.

Step 7: Add .gitignore and README.md
-------------------------------------
Created .gitignore and README.md locally:

        touch .gitignore
        touch README.md

Added basic content to .gitignore.

        git add .gitignore README.md
        git commit -m "gitignore added"
        git push origin master

Step 8: Tagging Versions
------------------------
Created a Git tag v1 on the latest commit (commit message:"gitignore added" with hash df9330):

        git tag v1 
        git push origin v1

 Checked the hashes of all commits to get the hash value of desired commit;

        git log --oneline

Later, changed the v1 tag to point to the initial commit (commit message"initial commit" with hash d363e72);

        git tag -f v1 d363e72
        git push origin v1

Step 9:README updated 
-----------------------

README.md updated and pushed to remote

       git add README.md
       git commit -m "README updated"
       git push

## END