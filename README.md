PLUG-Wall
=========

Panther Linux User Group's Summer Open Source Project. 

PLUG-Wall is an embeddable JavaScript based message board that can be included on any of your websites. There is two components, a server side which will store and recieve posts from the user and a client side script which will generate the HTML for the message board and allow users to send and get posts from the server.

Contributing
------------
To contribute to this project, press the fork button above on Github. This will be your own personal git repo to work on. 
Then you will clone your project
```bash
# Clone your own git repo, found on the top of your repo
git clone git@github.com:<username>/PLUG-Wall.git
```
Add the original project repo as a remote upstream, this will allow you to update your copy.
```bash
# Move into the file
cd PLUG-Wall
# Add a new remote which points to this project
git remote add upstream git@github.com:PantherLinuxUserGroup/PLUG-Wall.git
```
To get the latest updates from the main project repo
```bash
# checkout your master branch
git checkout master
# pull from upstream remote into your master branch
git pull upstream master
```
To work on a new feature, create a branch on your repo
```bash
# checkout a new branch
git checkout -b <name-of-branch>
```

The branch you have just created is where you will work on. Working on a branch allows you to keep your master as a mirror of the main project's master. 

To locally merge your branch with the main project's upstream use
```bash
# while in current branch
git pull upstream master
```

Then push your branch to your fork.
```bash
git push origin <name-of-branch>
```

You can now send a Pull Request from Github selecting your branch and to merge with the master. The Pull Request will be reviewed and be merged if accepted.

Running the server
------------------
To run the server you will need to install node.js
```
# Assuming you are using Ubuntu or Debian based distros
sudo apt-get install nodejs

# Arch Linux
sudo pacman -S nodejs
```
You will also need to install the server dependencies
```
cd PLUG-Wall/src/server && npm install
```
Once you installed node.js and you cloned the project to your computer as described in the section about contributing,
you can run the server.
```
# Change your working directory to the root of the project
cd PLUG-Wall
# Running the server
nodejs src/server/index.js

# or sometimes node.js is installed as node
node src/server/index.js
```
Open your favorite browser and navigate to http://0.0.0.0:1337/
