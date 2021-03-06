# Table of contents

* [About UH Manoa Club Hub](#About-UH-Manoa-Club-Hub)
* [Installation](#installation)
* [Application design](#application-design)
  * [Directory structure](#directory-structure)
* [Development History](#development-history)
  * [Milestone 1](#milestone-1)
  * [Milestone 2](#milestone-2)
  * [Milestone 3](#milestone-3)
  * [Initial User Testing](#initial-user-testing)
* [Galaxy Deployment](#galaxy-deployment)

# About UH Manoa Club Hub

UH Manoa Club Hub is a Meteor application Organizing Clubs for University of Hawaii at Manoa. When you come to the site, you'll come to a landing page:

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png "Landing Page")

From the landing page, you can easily access the login page, shown below, by clicking on the login button. Everyone with a UH account can login. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/login-page.png "Login Page")

This web application is featured with three different users, the students, the club administrator and the website administrator. And different authorization goes to different users. When you log in as a student, you will go to your student homepage (shown below). On top of the page, it will list all the clubs, which you are in. It's then followed by the comming events of your clubs. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/home-page.png "Home Page")

By clicking the "Browse Clubs" tab on the Menu of student homepage, you will go to club List page (shown below), which will contain all clubs available in University of Hawaii at Manoa. And this page is feaured with a interest search at the top of the page.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-listing-page.png "Browse Clubs Page")

If you login with a club administrator's account, you will go to the founder's admin page, shown below. This page is a channel where you can access all the clubs you created. And it will also allow you to create a new club by clicking on the card, with "+" sign in it.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-founder-admin.png "founder admin Page")
 
The following is the create club page. To create a club, you simply need to fill in all the required information and then click submit. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/add-club-page.png "Create Club Page")

To modify the information of an existing club, you can click on the edit button on the bottom of the club card.And it will look like this: 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-club.png "Edit Club Page")

This page will show the events you've created, followed by your club info. To modify the events, you can simply click on the event card, then it will lead you modify event page. To create a event, you click at the card with "+" in it, and it will take you to a separate page which allow you to add more events.

The create event page and edit event page are both shown below:

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/create-event.png "Create Event Page")
  
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-event.png "Edit Event Page")

To have a better control of the website, someone can log in with a site administrator login. this type of user can go the site admin page, shown below. And they will have the authority to hide or delete a club.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/site-admin.png "Site Admin Page")

# Installation

1. [Install Meteor](https://www.meteor.com/install).

1. clone [UH Manoa Club Hub](https://github.com/ics-software-engineering/meteor-application-template/archive/master.zip) project using git.
  
3. cd into the app/ directory and install libraries with:

```
> meteor npm install
```

4.  run the system with:

```
> meteor npm run start
```
If you successfully run it, you will see the following in your prompt.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/success.png "success screenshots")

And the application will appear at [http://localhost:3000](http://localhost:3000). 
# Application Design

## Directory structure

This App is designed with [meteor 1.4](https://guide.meteor.com/1.4-migration.html). And we also follow the Meteor 1.4 [Application Structure](https://guide.meteor.com/structure.html) guideline, for which we used an import/ directory in the app/ directory to hold our code. The structure of the app/ directory are shown below. 

```
client/
  lib/           # holds Semantic UI files.
  head.html      # the <head>
  main.js        # import all the client-side html and js files. 

imports/
  api/           # Define collection processing code (client + server side)
    club/
    event/
  startup/       # Define code to run when system starts up (client-only, server-only)
    client/        
    server/ 
    both/
  ui/
    layouts/     # Layouts contain common elements to all pages (i.e. menubar and footer)
    pages/       # Pages are navigated to by FlowRouter routes.
    stylesheets/ # CSS customizations, if any.

node_modules/    # managed by Meteor

private/
  database/      # holds the JSON file used to initialize the database on startup.

public/          
  images/        # holds static images for landing page and predefined sample users.
  
server/
   main.js       # import all the server-side js files.
```
 
# Development History

## Milestone 1

The goal of Milestone 1 was to create mockup HTML pages for the various pages that will be a part of UH Club Hub.

Milestone 1 consisted of 10 issues, and was managed via the [uhclubhub GitHub Project M1.](https://github.com/uhclubhub/uhclubhub/projects/1). 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/issue-page.png "issue Page")

And we also use [projects](https://github.com/uhclubhub/uhclubhub/projects/1) feature on github to do the progress management.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/project-page.png "Project Page")

So when ever we have an added issue, we will add it in the "Backlog" column, when we are working on a issue, we add it to the "In Progress" column, and when we are done, we close it and add it to the "Done" column. This keep our progress organized. By knowing what is done and who is working on what, it will be easier for the members to decide what to do first. 

The pages we created for this milestone includes:

* Landing Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png"/>
  
* Login Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png"/>

* Home Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/home-page.png"/>

* Create Club Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/add-club-page.png"/>

* Edit Club Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-club.png"/> 

* Create Event Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/create-event.png"/>
  
* Edit Event Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-event.png"/>

## Milestone 2

Milestone 2 was started on April 13, 2017 and ends on April 25, 2017. The goal of Milestone 2 is to finish unfinished mockup pages and improve already existing ones, implement UH CAS authentication, and create the Collection for the Clubs. The Gitbub issue page of this mile stone is shown [here](https://github.com/uhclubhub/uhclubhub/issues?utf8=%E2%9C%93&q=milestone%3A%22M2%22). And it's progress is  being managed [here.](https://github.com/uhclubhub/uhclubhub/projects/2)

The mockup pages created includes:

* List Club Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-listing-page.png"/>

* Site admin Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-founder-admin.png"/>
  
* Club Admin Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/site-admin.png"/>  

* UH CAS Test Authentication

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/uh-cas-authentication.png"/>
  
* Creation of Club collection
  
  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/browse-club-updated.png"/>
 
 In this issue, we 
  1. created the club collection in /imports/api/. 
  2. create an initialization file, club.js in /imports/startup/server/
  3. modified the browse-club-page.html and browse-club-page.js to link the content from collection, and allow the club in the database to show up iteratively.
  
## Milestone 3

Milestone 3 was started on April 27, 2017 and ends on May 9, 2017. And at the end of this mileston, we've accomplished the following:
* create the database for user profiles.
* create interest collection to implement sorting based on interest

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/browse-club-updated.png"/>
 
  I updated the broseclub page so that it allows the user to filter out the clubs based on interest. The filter works when the user choose an interest in the interest list. And it will filter automatically when user release the mouse.

* implement the add/edit fuctionality to allow us to database with a form, and the edit an existing document in database.
  
  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/add-club-page.png"/>
  
  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-club.png"/>
  
  In this task, I updated both add-club-page and edit-club-page. I involked forms control from [meteor-exaple-form](https://ics-software-engineering.github.io/meteor-example-form/). That has made create-club-page.html a lot cleaner. This create club page also chesk the content of the input to make sure they are right type, and to make sure that all the required fields are filled. With a submission, the site will switch to the brose club page automatically. And I also make sure that whenever a usre added a club, the content will showup in a ui card in the browse club page. Edit club page is similar to create club page, except that the club information was filled. At the top of the edit club page, there's an additional event section. It contain all the events of this club. That means edit club also includes edit events. User can manage their events on Edit club page. 

Milestone 3's issues are assigned  [here](https://github.com/uhclubhub/uhclubhub/issues?utf8=%E2%9C%93&q=milestone%3A%22M3%22). 
And the project progress is being managed [here](https://github.com/uhclubhub/uhclubhub/projects/3). At the end of the milston we've closed all of the previously designed issues, except issue 20, create/edit event. The following are the screenshots of the milestone 3 issues and project progress.

<img width="800px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/M3-issue.png"/>

<img width="800px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/M3-project.png"/>



## Initial User Testing
In order to do an initial user testing, I asked 5 students to test out my project. I didn't tell them much about this website is about, since being self-explanatory should also be part of the testing. I told them to goto [my host](http://uhclubhub.meteorapp.com/) to check out the site and tell me about what they like or what could be improved. And the following are the responds from them.

Yunping (senior, major in Business): 

"The layouts are nice, but I'm so consuded with what this site is about. I think you should have an About page, which can tell the user what this site provide us, and what we can do about it. "

Jinping (senior, major in Business): 

" Join Club is not doing anything. More information about the club would be expected. "

Jipeng Huang (senior, major in computer Science): 

"This app doesn't seem to be well designed for mobile devices. I tried you link and image of the landing page was not well proportioned, and I can only see part of the menu. The homepage looks weird as well, and I cannot logout "

Lookuang (Senior, major in Art): 

"I don't exactly know what what this site provide me. You probably need a user guide. "

Haihong (Senior, major in Japanese): 

"I wasn't sure where the homepage was initialy. When I click on UH Manoa ClubHub in the menu, it was not found. I'm pretty sure it showed up when I've just login.  "

In conclusion, user responds told us that we should complete the functionalities, and make sure every link works; we should improve our UI design to make sure they work well more mobile devices as well; and we need an userguide page at least for the first time users. 

# Galaxy Deployment

The link to our galaxy deployment is [http://uhclubhub.meteorapp.com/](http://uhclubhub.meteorapp.com/)
