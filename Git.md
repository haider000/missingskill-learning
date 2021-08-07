# Git
  * Git is a free open source distributed version control system. 
  * It gives facility to manage code base and versions.
  * It tracks changes in files and take a look at code history.
  * It allows to have your own working copy of code in local system.

# Distributed Version Control System

It is a kind of version control system where in a single code base multiple developers can work together in same repository i.e. collaboration and Every user has its own copy of code base in local system.
They can update a file same time and both can merge them together.

eg : Git , Mercurial

# Centralised Version Control System

It is also a kind of version control system where in a single code base multiple developers can work together in same repository but there is only one central server to get the latest copy of the code and to share changes with other
Atleast one Developer can work at a time unless he pushes the code .
eg : Subversion , Microsoft team foundation server

<br/>
<br />
<br/>

# Git Commands

<br/>
<br/>

## 1. SETUP Configuring user information
<br/>

``` git config --global user.name “[firstname lastname]” ```
set a name that is identifiable for credit when review version history

``` git config --global user.email “[valid-email]” ```
set an email address that will be associated with each history marker

``` git config --global color.ui auto ```
set automatic command line coloring for Git for easy reviewing

``` git init ```
initialize an existing directory as a Git repository

``` git clone [url] ```
retrieve an entire repository from a hosted location via URL

<br/>
<br/ >

## 2. STAGE & SNAPSHOT Working with snapshots and the Git staging area
<br/> 

``` git status ```
show modified files in working directory, staged for your next commit

``` git add [file] ```
add a file as it looks now to your next commit (stage)

``` git reset [file] ```
unstage a file while retaining the changes in working directory

``` git diff ```
diff of what is changed but not staged

``` git diff --staged ```
diff of what is staged but not yet commited

``` git commit -m “[descriptive message]” ```
commit your staged content as a new commit snapshot

<br/>
<br/>

## 3. BRANCH & MERGE Isolating work in branches, changing context, and integrating changes
<br/>

``` git branch ```
list your branches. a * will appear next to the currently active branch

```git branch [branch-name] ```
create a new branch at the current commit

``` git checkout ```
switch to another branch and check it out into your working directory

``` git merge [branch] ```
merge the specified branch’s history into the current one

``` git log ```
show all commits in the current branch’s histor

<br/>
<br/>

## 4. SHARE & UPDATE  Retrieving updates from another repository and updating local repos
<br/>

```git remote add [alias] [url]```
add a git URL as an alias

```git fetch [alias]```
fetch down all the branches from that Git remote

```git merge [alias]/[branch]```
merge a remote branch into your current branch to bring it up to date

```git push [alias] [branch]```
Transmit local branch commits to the remote repository branch

```git pull```
fetch and merge any commits from the tracking remote branch


<br/><br/>

## 5. INSPECT & COMPARE  Examining logs, diffs and object informatio
<br/>
 
 ``` git log ```
  show the commit history for the currently active branch
  
  
  ```git log branchB..branchA```
  show the commits on branchA that are not on branchB
  
  
  ```git log --follow [file]```
  show the commits that changed file, even across renames
  
  
  ```git diff branchB...branchA```
  show the diff of what is in branchA that is not in branchB
  
  ```git show [SHA]```
  show any object in Git in human-readable format
  
  
  <br/><br/>
## 6. REWRITE HISTORY Rewriting branches, updating commits and clearing history
<br/>

  ``` git rebase [branch] ```
  apply any commits of current branch ahead of specified one

  ```git reset --hard [commit]```
  clear staging area, rewrite working tree from specified commit
<br/><br/>

## TRACKING PATH CHANGES Versioning file removes and path changes
<br/>

``` git rm [file] ```
delete the file from project and stage the removal for commit

``` git mv [existing-path] [new-path] ```
change an existing file path and stage the move

```git log --stat -M```
show all commit logs with indication of any paths that move 
  
 <br/>
 <br/>
  
  
  
