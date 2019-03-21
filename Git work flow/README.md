# GIT Workflow Commands -

1- please make an account in Github and install git on ur systems , DONOT install the GUI version  . Install the Command Prompt or terminal version for windows or Mac respectively . Please see an Intro video in case you need to refresh then read guide . Intro video was shared on group.

First Use -
 
 1- Check you emails for an Invitation from the organization mind-hack-zombies go to The Autonomous HR repository and Fork it to your personal repo .
 
 2- next step we need to clone it down to your local machines from your personal repo . That click on the clone drop down and copy the link .
 
 3- go over to your cmd or terminal and navigate to your desktop using cd command . type in 
 >>git clone <paste url copied WITHOUT angle brackets>
  

While editing -

1-Always do a pull of the repository before you edit anything . this can be done by doing a
>>git pull

2-when you start working on edit it is best to do a

>>git checkout -b dev  (on the first time only use -b , it creates a new                   branch dev on run time)

from the next time use

>>git checkout dev  (as the branch dev already exists)

3- now you can go over to any file from outside your cmd and code away !!! When your done save the file inside the folder !!!

4- once coding is done and your happy with progress made .
do

>>git add .      ( this will add file to staging area)

then

>>git commit -m "A meaningfull commit message to explain your change"

then

>>git checkout
>>git push origin dev

once this is done go over to your browser you will notice that it has reflected on to your dev branch in your personal repository with the same commit message you had passed .

5- If you feel your code is rdy to be merged with main organization repository just raise a pull request . it will by default pick it as destination just chk your changes and creat request , one of the admis will merge your pull req and merge your changes with the master after review .

6- after acceptance of your code into main organisation repo , dont forget to update your master too to reflect new edits . you can 

go to cmd and 

>>git checkout master

it would show changes with main organization branch and ask you to pull so as to fastforward master .

if this doesnt show just drop down on branches on your personal repo and manually check . if you still see differences raise a pull req from your dev to  master branch and merge .

then repeat the last command .

SOME OTHER IMPORTANT COMMANDS YOU COULD USE 

To see currently checked out branch you are working on
>>git branch  

To check current status of commited , uncommited or staging area files
>>git status 

To synch with upstream Repository

Add the remote, call it “upstream”:

>>git remote add upstream https://github.com/whoever/whatever.git

 Fetch all the branches of that remote into remote-tracking branches,
 such as upstream/master:

>>git fetch upstream

 Make sure that you’re on your master branch:

>>git checkout master

 Rewrite your master branch so that any commits of yours that
aren’t already in upstream/master are replayed on top of that
other branch:

>>git rebase upstream/master

If you don’t want to rewrite the history of your master branch, (for example because other people may have cloned it) then you should replace the last command with 

>>git merge upstream/master








