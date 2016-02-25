 Git Tutorial (Just the Basics)
Act I: Repo for One
Topics covered

    Creating a new public repository in GitHub
    Cloning a repo locally
    Adding files to the local repo
    Commiting changes to local repo
    Pushing changes to the public repo

Procedure

    students create new public git repository in GitHub
        call repo GitFun
        see clone URL
    Start a terminal shell -- keep it open for a while!
        cd ~/MOUNTED/apcs-locker/workspace3
        git clone <Clone URL>
        cd GitFun
        ls -la (notice the .git folder)
    Start Eclipse, create new Java project in workspace3 called GitFun
    ls -la (notice what Eclipse has added)
    Eclipse: Add HelloGit.java to src
        add a main() that prints out a message
    Back to terminal:
        git add HelloWorld.java
        git status
        git commit -m "Initial Commit"
        ( tip: forget the -m ) switch and the vi editor starts? :q! to get out
        git status (local repo state is ahead of origin , the copy of the repo in GitHub)
        git push
    View changes in GitHub
    In Eclipse: modify class HelloGit and save
    In terminal:
        git status
        git diff HelloGit.java
    Oops, I don't like my changes!
        revert back to prior committed state:
        git reset --hard
        revisit file in Eclipse editor, which has detected a change to the file
    Exercise:
        Add a second class to the project
        git add <FILENAME>
        git commit -m "Initial commit"
        git push
        Check for new file in GitHub
        make changes to file
        git { add, commit, push }
