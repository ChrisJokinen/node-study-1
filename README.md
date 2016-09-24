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


# Requirements:

You will need:
* a github account.
** to make using github easy, setup a private key and add it to github (github - generatingan ssh key)
* node.js installed


I am working on a windows 10 system. To make use of github I have installed the GitHub Desktop



# Sources:

* [GitHub Desktop](https://desktop.github.com/)
* [Github - Generating a ssh key](https://help.github.com/articles/generating-an-ssh-key/)
* [Heroku - Node Best Practices](https://devcenter.heroku.com/articles/node-best-practices)

