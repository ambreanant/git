1) What is Git?
Ans: Git is a distributed version control system (VCS).
Git is a tool that helps multiple people work on the same code project or documents by 
tracking and managing changes of the files.

2) What is VCS?
Ans: Every time you make a change, whether it's adding a sentence to a document or altering 
a line of code, the VCS records and saves the outcome.

3) Why VCS?
• Backup and Restore: Files are safe against accidental losses or mistakes.
• Collaboration: Multiple people can work on the same project simultaneously.
• Branching and Merging: Users can diverge from the main base of code,experiment, and then bring changes back in line without losing work.
• Tracking Changes: You can see specific changes made and by whom.

4) check git version?
Ans: git --version

5) Configure git with username & Email
Ans: git config --global user.name 'username'
git config --global user.email test@gmail.com

6) git config --list
Ans: to check config username & email.

7) Initialized git repo
Ans: git init

8) Create and check out a new branch named <branch>. Drop the -b flag to checkout an existing branch.
Ans: git checkout -b <branch>

9) show modified files in working directory
Ans: git status

10) add a file as it looks now to your next commit (stage).
Ans: for single: git add fileName
for all changes files: git add .

11) Commit the staged snapshot, but instead of launchingva text editor, use <message> as the commit message.
Ans: git commit -m "<message>"

12) Push the branch to <remote>, along with necessary commits and objects. Creates named branch in the remote repo if it doesn’t exist.
Ans: git push <remote> <branch>

13) check out a new branch named <branch>
Ans: git checkout <branch>

14) Fetch the specified remote’s copy of current branch and immediately merge it into the local copy
Ans: git pull <remote>

15) Clone repo located at <repo> onto local machine. Original repo can be located on the local filesystem or on a remote machine via HTTP or SSH.
Ans: git clone <repo>

16) Fetches a specific <branch>, from the repo. Leave off <branch> to fetch all remote refs.
Ans: git fetch <remote> <branch>

17) Create new commit that undoes all of the changes made in <commit>, then apply it to the current branch.
Ans: git revert <commit>

18) Remove <file> from the staging area, but leave the working directory unchanged. This unstages a file without overwriting any changes.
Ans: git reset <file>

19)Reset staging area to match most recent commit, but leave the working directory unchanged.
Ans: git reset

20) Reset staging area and working directory to match most recent commit and overwrites all changes in the working directory.
Ans: git reset --hard

21) Move the current branch tip backward to <commit>, reset the staging area to match, but leave the working directory alone.
Ans:git reset <commit>

22) Same as previous, but resets both the staging area & working directory to match. Deletes uncommitted changes, and all commits after <commit>.
Ans: git reset --hard <commit>
and  git reset --hard HEAD~2   (Delete Last two commits from remove directory also on local and it not store history)

23) Merge <branch> into the current branch.
Ans: git merge --no-f --no-commit <branch>

24) restore file to last commit, it will remove all changes from files that not commited.
Ans: git restore .

25) restore back from staged to working (back from git add to working)
Ans: git restore --staged .

26) after git add if bymistake added some changes in file, to remove that. (added changes to stagging area(did't commit) after this added more changes to file)
Ans: git restore --worktree .

27) How about if we did commit also wrong files.
Ans: git reset --soft Head^ (uncommit and keep the changes)
git reset --hard Head^ (uncommit and discard the changes)


28) untracted - new files that gir doesn't yet track
modified - changed
stagged - file is ready to be committed
unmodified - unchanged.
push - upload local repo content to remote repo

29) TO delete branch
Ans: git branch -d <branch>

30) 
------------------------------------------
Going forward we need to follow the below steps when working with GIT branches.

When creating new branches :
(Always check with the person who is assigning you the task on which branch to use when creating a ticket branch.)

git checkout master ( or the branch shared above )
git pull --rebase
git checkout -b <ID Branch>
git add .
git commit -m "commit message."
git push

Before merging a branch in any environment :
******** VIMP ********
git checkout master
git pull --rebase
git checkout <ID Branch>
git pull --rebase
git merge master
<Resolve conflicts if any.
git add .
git commit -m "commit message.">
git push
******** VIMP ********

(Always check with the person who is assigning you the task if you should go ahead and merge your changes.)

git checkout ncqa(2,3,4)
git pull --rebase
git merge --no-commit <ID Branch>
git status
<Resolve conflicts if any.
git add .>
git commit -m "merge <id branc> in ncqa(2,3,4)">
git push

