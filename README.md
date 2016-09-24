# node-study-1

This will be a #1 of a series of repos created as I study and explore node.js, npm and perhaps a little github and AWS (Amazon Web Services) too.


# Purpose:

My experience is that of a PHP programmer and while I have been working to transition to Node and I have found the common wall many find when making this move, callbacks and race conditions. 

So in this series I will do what I can to explain my thoughts as I explore node with a goal of gaining mastery over it.


# Reasoning:

As stated above I come from a background of PHP, I also have experience with the often related languages of HTML, CSS, JavaScript, SQL and others like Delphi. 

When I was making the decision to first study PHP over other competing technologies like; ASP, ColdFusion or JSP. I settled on PHP because of the technology, the community, cost and the abundance of resources aimed at new programers. Looking at all of these points I felt very positive that PHP was going to be the technology that came out on top, and I was right. 

After many years in PHP, I am now seeing a shift in the technology landscape and it is a big one.


# The Future:

Some very smart people took a look at the current web client server design and found an issue. This issue is not specific to any specific technology but seems to be a share issue, blocking code. And so they came out with a solution that would run code but would not block the execution pipe. This non blocking code execution is where the amazing speed of node is realized and is also the source of its headaches.

This shift involves the following technologies:
* Node.JS and its related technologies; Express, Angular and Mongo. (A.K.A the MEAN stack)
* Serverless Amazon – a combination of Amazon Services including; S3 (static document storage/hosting), API Gateway (for REST services), Lambda ( execution service, imagine running server side code without having to worry about managing the server ), Dynamo DB ( Amazons version of Mongo DB ), RDS ( Relational Database Service, here you can host a more traditional DB like MySQL)
* gitHub – I have a limited knowledge of git and so will offer tips as I find them. I do have a working knowledge of a git work flow I have picked up from work and it is what I will present in this series.


# What is missing to date:

* Off the top of my head I know I am missing automated unit testing. I will work to correct this as I make more repos in this series.
* a practical and usable project to work on. I am going to hold off on this until I have a much stronger understanding of node.



# This project:
I will focus on configuration of a basic node project, github configuration and the work flow I will use going forward. I will note my source materials below and reference them below.


You will need:
* I am working on a windows 10 system. To make use of github I have installed the GitHub Desktop also known as GitHub for Windows.
* a github account.
  * to make using github easy, setup a private key and add it to github (github - generating an ssh key)
  * to add an ssh key to your windows system, use the git shell and follow the rules for generating a new sshe key (if you do not have an ssh key)
  * after you make the sshe key follow the instructions for adding you key to you github account.
* node.js and npm (node package manager) installed
  * Team Treehouse - install node and npm

## Steps:
In Github
* make a new repository - you may need to navigate to the repositories section on github. Look for a green button that should read "New" or "New Project", click it and fill out the information.
  * name the repo. If the name already exist you will get a warning.
  * description is optional, but very useful for a project.
  * for study or open source projects, the public repository is fine. Private is a paid feature and what you would use for any projects you want full control over who can see you code.
  * click the "initalize this repository with a README" checkbox.
  * click "Create Repository" button
  
Our your local system
* Clone your new repo
  * open the GitHub Desktop and click on the "+" on the right. select the clone option and you will see your github repositories listed. select the one you created and click the clone button at the bottom. 
  * Select where you want the repo to exist on your local system. Unlike something like PHP, ASP, etc.. node can run in any location provided you have node installed. I setup a "nodejs" folder directly off of my C:\ drive. For cloning you always select the root directory you want your project to reside in. So there is no need to make a project folder as the cloning process will make it for you. My nodejs folder is just where all of my node projects will reside.
* initialize you node project
  * open th Git Shell, navigate to your project folder. For me I use the "cd c:\nodejs\node-study-1" command at the prompt.
  * enter npm init. This will start a series of questions about your node application most of these you can use the default (hit enter) but you can name your application, add a description, enter your name as prompted. Once all the questions are answered you will be presented with the contents for a file called "package.json". If you do not know what a json file is, well in simple terms it is a text file. JSON is used a lot to transport information between systems and it can also be used to store settings like an INI or config file.
  * Modify package.json - I am following the suggestion made here on Heroku (see references) and modifying the package.json file to include the engines setting. The reason stated is sound. Also read the rest of the article as he has some great ideas.
  * Modify README.md - The default readme only has your project name. As you work on your node project you will need to modify from time to time. Use the GitHub - Markdown Cheetsheet to learn about formating options.
  * create index.js - when you ran the "npm init" above, one of the questions asked was concerning the "entry point" of your app and it defaults to "index.js". now we need to make it and add some very simple node js code, see below, enter this and save your new file as "index.js".
```javascript
console.log("Hello");
```
  * test code
    * open the git shell
    * naviagte to the project folder. On my system the command is "cd C:\nodejs\node-study-1"
    * enter the command "node index.js" without the quotes
    * If all goes well you should see "Hello" with out quotes in the console as a response.
    
* commit changes
  * return to the git desktop. in here you will see your project on the left panel. Select it and you will see int the center panel a list of files that have changed (note the circle) or have been added (note the +). If you select a file you will see what changes occured in the right hand panel. hanges that are going to be removed are marked in red and have a "-" in front of the lines. changes that will be added are highlighted green and are marked with a "+" in front of the lines. Use this feature to look over the files and make certain you are ready to commit these changes. Any files you do not want to push you can right click on the file and select "Discard Changes" option to return the file to its original state. With new files this will remove them.
  * after you have reviewed the files and you are happy with them, now we can start to commit them. to the left of the file names you will see a check box. you can select one or more to add these changes to 1 commit. You can select 1 file per commit but it is common to select all files that share a related change. For now select the package.json and then below in the summary field enter "Added Engine setting" and click "commit to master". Now select the index.js and enter "added index.js" in summary and then again click the "commit to master". Repeat for any other files you have added or changed. You can alternatively select all files and just add a summery of "new file and changes to files". While this is doable you are being more vague and you will find it more difficult to track down specific changes to your code base later. NOTE: master is a reference to the default "Master" branch of you code repo. When starting a new code base it is ok to write to it, but later as you add team members, patch code, add new features you will want a different git work flow that will make use of branches. I will cover that later. For now just remember writing to master is only ever done at the start of coding only and while you are build this base code and you are the sole author, it is ok for the short term.
* push to GitHub - now we will push or changes up. In the Git Desktop they have a sync button with a gray bar under it. That bar will show the commits you have done. All we need to do is click the "Sync" button and the desktop wll handle pushing our commits to the master branch on GitHub. Once done you should be able to log into your github account and see the changes you have made.



# Sources:

* [GitHub Desktop](https://desktop.github.com/)
* [Github - Generating a ssh key](https://help.github.com/articles/generating-an-ssh-key/)
* [Heroku - Node Best Practices](https://devcenter.heroku.com/articles/node-best-practices)
* [Team Treehouse - install node and npm](http://blog.teamtreehouse.com/install-node-js-npm-windows)
* [GitHub - Markdown Cheetsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
