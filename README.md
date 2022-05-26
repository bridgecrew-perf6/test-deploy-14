
This is the README file for testing changes to the repository.I'm deploying to staging
=======
Another change
Another change
Testing the CircleCI Install
Checking on the local remote
Another new line for testing
One final github test
Adding a line for heroku push test
Another new line for testing

Deploying via git
** Create a local repository to work with **

* Initialize a git repository in the current directory
$ git init
* Tell git to add all files in the directory
$ git add -A
* Commit files
$ git commit -a -m "Initial node-deploy commit"
 
** Setup a target repository **

* Move to a different directory
* Clone the node-deploy repo
$ cd ../
$ git clone node-deploy/ local_clone

* Checkout to a temporary directory
* Change the checked out branch in the local clone because git does not 
  like to do pushes to repositories with the target branch checked out already.
$ cd /local_clone
$ git checkout -b tmp 

* Go back to previous repository
$ cd ../node-deploy

* Remote command
$ git remote add second ../local_clone/
* The remote is going to be named second. And we can find it at local clone. 
  Now if we were creating from a remote system, then the URL would go here 
  instead of the file path
* What the remote does is it links different repositories together so that
  you can push commits from one to the other.

* Make changes to previous directory 
* git commit
* Then push to second repo as master
$ git commit -a -m "Pushing line to local clone"
* -a: commit all changes
$ git push second master

* Checkout the local_clone to master
$cd ../local_clone
$ git checkout master

* Check for changes












