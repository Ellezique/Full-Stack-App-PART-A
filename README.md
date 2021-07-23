# T3A2-A  Full Stack App (PART A)
## AfterCredits
#### By: Chris Gibson & Gizelle van Zyl
GitHub repository: https://github.com/Ellezique/Full-Stack-App-PART-A
___

### R1: DESCRIPTION OF WEBSITE

#### PURPOSE 
AfterCredits is a movie discussion app (ideally for people aged 18 and older). There are two proposed versions of the app:

**A. Early Beginnings version:** The initial core app version is designed to build user community. There will be one movie or series for the month, similar to a book club. Community users can see what the select movie/series is so that they can have a chance to watch it if they haven't seen it yet. When they are ready, they can join the chatroom to discuss the movie/series with other users.

**B. Expansion version:** The expanded app will have multiple movies/series, each with their own chatroom. Users can join a chatroom to discuss any listed movie or series of their liking whenever they wish, rather than waiting for a single monthly selection. 

The development plan is to build the Early Beginnings version first (core app) and to then commence incorporating features from the Expansion version. It is fairly unlikely that the entire Expansion version will be completed within the relevant development timeframe. It is anticipated that the final product will be an Early Beginnings version incorporating some additional features that have been proposed for the Expansion version. 

From a real life marketing perspective, the plan would be to achieve continued member and participation growth by commencing with a small and intimate community and gradually expanding the collection of movie/series chatrooms as the community grows (and becomes, perhaps, less intimate due to the increased number of users), thereby allowing for the users to be spread out across multiple chatrooms. 

---
#### FUNCTIONALITY/ FEATURES

**A. Early Beginnings version:**

###### Sitemap: Early Beginnings version

![Core App Sitemap](docs/core_app.PNG)

###### Log in/Sign up: Early Beginnings version
Users can sign up and then log in to access the chatroom to discuss the movie/series of the month. They will need the following to sign up:
- username
- email
- password

###### Authentication and Authorisation: Early Beginnings version
Authentication and Authorisation will be handled using:
- Knock
- JWT

There will be two user roles: 
- Admin
- User

###### Movie/Series Cards: Early Beginnings version
The home page includes one movie/series card for the month. 
The movie/series card will contain the:
- title
- poster (image) 

The initial title and image can be saved in the source code as a placeholder. Thereafter, the movie data can be accessed from an API such as the Movie Database (IMDB Alternative). The RAPID API version currently has a basic price plan of $0.00 per month that inludes 1,000 requests per day and is available at: https://rapidapi.com/rapidapi/api/movie-database-imdb-alternative/
Once the API is implemented, the imdb_id can be stored in the database when the card is created. That imdb_id can then be used to fetch the title and poster(an image url) from the API. 

A "Show more" button can then toggle additional data from the API e.g. a movie or series description.

###### Chatroom
Each movie/series card contains its own chatroom relevant to that movie/series.

Messages will have full CRUD functionality. Users can post, edit and delete their own messages. Admin role users can additionally delete anyone's message to ensure a means for removing inappropriate content.  

Each message will include:
- username
- message
- posting time and date

###### Contact Page: Early Beginnings version
All website visitors can access the contact page.

An Admin email address will be included to allow users to contact an admin directly.

The AfterCredits head office address will be listed and accompanied by a static location map. 

###### Styling, design and aesthetics: Early Beginnings version
Styling will include the following:
1.	Icons: https://fontawesome.com
2.	Google fonts: https://fonts.google.com/
3.  Background image/s from unsplash: https://unsplash.com/

Each JavaScript component will have its own css stylesheet e.g. Navbar.js and Navbar.css

###### Database 
![Database](docs/erd.PNG)

---

#### FUNCTIONALITY/ FEATURES

**B. Expansion version:**

###### Sitemap: Expansion version

![Expanded App Sitemap](docs/expanded_app.PNG)

###### Log in/Sign up: Expansion version
As above. An expansion feature could enable users to select an avatar image (a limited number of images posing no storage issues) or upload their own image (requiring a storage solution such as Cloudinary).

###### Authentication and Authorisation: Expansion version
As above.

###### Movie/Series Cards: Expansion version
The Cards feature should have full CRUD functionality so that an Admin user can change the monthly movie/series card and add additional cards as the site grows towards the Expansion version. 

The home page includes multiple movie/series cards.
Each home page movie/series card will contain the:
- title
- image 

Users may click on a card to view additional movie information, which may include any of the following: Year, Metascore Rating, IMDB rating, Release date, Runtime, Genre, Directors, Writers, Actors, Plot, Awards etc.

###### Chatroom: Expansion version
As above. 

Additionally user messages can display with the user's chosen avatar or image. Users can click on a username to see all of their messages.

Each movie/series can have two chatrooms:
- with spoilers
- without spoilers
A spoilers boolean could be added to the Cards table to distinguish spoiler and no-spoiler messages. An additional button will be needed to allow users to select whether they want to view the spoiler or no-spoiler chatroom.

Chatrooms can contain many messages. There could be a scroll bar or a hide/show more button so that only the most recent messages are visible but that the user may still look at older messages should they choose to do so.

###### Contact: Expansion version
As above but instead of including an admin email address, users can submit a contact form. 
- The contact form could be handled using Netlify forms.

The interactive map of the business address will have a marker showing the location. Users can interact with the map.
The map data can be provided by an API such as Bing Maps API, available at https://www.bingmapsportal.com/ or alternatively, the Google Maps API.

This page will also include links to the developers' GitHub accounts.

###### Styling, design and aesthetics: Expansion version
Styling could include the following:
1.	Icons: https://fontawesome.com
2.	Google fonts: https://fonts.google.com/
3.  Background image/s from unsplash: https://unsplash.com/
4.  Animated background: https://greensock.com/

###### Additional features for future development (the nice-to-have-but-not-included list)
- A search feature so that users can search for a particular movie or series by genre, actor, rating etc. This feature will not be pursued in the current project. It would require database design changes and features that are beyond the scope of the current project.
- Full CRUD functionality over users so that users may edit their own details (and so that Admin can delete users). 
- Thorough solutions to moderating and handling user input and dealing with inappropriate content.

---

#### TARGET AUDIENCE

Broadly, the target audience inludes anyone that enjoys watching movies/series and would like to read other users' comments and engage in discussions about movies/series. The app is a community for watchers, bingers, enthusiasts, the curious and critics alike.

**A. Early Beginnings version:**
The target audience includes users who:
- want to join a monthly movie/series club
- want to discuss or read comments about a movie/series
- are, ideally, at least 18 years old (movies and series have classifications and age restrictions which vary between jurisdictions, therefore it is preferable that users are at least 18 years old when entering chatrooms).

**B. Expansion version:**
The target audience includes users who:
- want to discuss or read comments about a number of different listed movies/series 
- get more information about listed movies/series

#### TECH STACK 

- **HTML**: HyperText Markup Language is the standard markup language for documents to display in web browsers. 
- **CSS**: Cascading Style Sheets describe the presentation and styling of markup language documents.

##### Front-end/client side
- **React.js**: [React](https://reactjs.org/) is a front-end (client side) **JavaScript** library used to build user interfaces and components.
- **Yarn**: [Yarn](https://yarnpkg.com/) is a [package manager](https://engineering.fb.com/2016/10/11/web/yarn-a-new-package-manager-for-javascript/) for JavaScript (client side) that will be used for this project. It is prefereable to use yarn with React apps. The most stable version currently is 1.22.5, which will be used for this project. To add and remove packages, `yarn add [package]` and `yarn remove [package]`. Install all project dependencies using `yarn install`. Dependencies can be upgraded to the current stable versions by running `yarn upgrade`. All dependencies and configuration for the React side of AfterCredits will be specified in the package.json file.
- **Jest**: [Jest](https://jestjs.io/) is a testing framework that works with React projects (testing front-end).
- **Netlify**: [Netlify](https://www.netlify.com/) will be used to deploy the front-end React repository. The service used for this project is free of charge.

##### Back-end/client side
- **Ruby on Rails**: [Ruby on Rails](https://rubyonrails.org/) is a back-end/ server side application framework written in Ruby. It has a model-view-controller framework.
- **RubyGems**: [Ruby Gems](https://rubygems.org/) is a package management framework for Ruby and is used to distribute Ruby programs and libraries. RubyGems is a tool used to install gems.
- **Rspec**: [Rspec](https://rspec.info/) is a meta-gem used for testing in Ruby on Rails.
- **Heroku**: [Heroku](https://www.heroku.com/) is a cloud platform that supports Ruby on Rails. It will be used to deploy the Ruby on Rails repository (back-end/ server-side). The service used for this project is free of charge.

##### User Testing (Development and Production)
- Consider either manual testing (video recording or excel spreadsheet); or
- Cypress

##### Database
- **PostgreSQL**: [PostgreSQL](https://www.postgresql.org/) is a free relational database management system.

##### Repositories
- **Github**: [Github](https://github.com/) is a development platform and service hosting Git version control. The service used for this project is free of charge.

##### Source Control 
- **Git**: [Git](https://git-scm.com/) is a version control system for tracking changes across a set of files and to coordinate work between programmers working collaboratively on developing source code.

###### PROPOSED BASIC SHARED REPOSITORY WORKFLOW

A. SETUP

1.    **Create app in central repository on GitHub.** Both developers will have access to push and pull- Developers must do all their work on a different branch to master and must not commit to the master branch directly.

2.    **Each developer clones the main GitHub repository to their local.** Developers are working in VS Code.

3.    In local, developers create and checkout their own branch:  `$git checkout -b Developername`. 

B. DEVELOPMENT

4. Developers should do all their work on their own branch and not commit to the central repositry (GitHub) master branch directly. Developers should work only on their `Developername` branch. `$ git branch` to see what branch you are on. If you are not on your branch `$ git checkout Developername`

5.  **Code in your Developername branch** and then stage changes in local `$ git add .` and commit changes with `$ git commit -m "meaningful commit description"`.

6. The developer can incorporate changes from the GitHub repo into the branch that they are on by making sure they are on their `Developername` banch and then:  `$ git merge master`. They can pull using `$ git pull origin master `. **Resolve conflicts locally in VS Code** before pushing to GitHub.

7. Developers can **push their changes to GitHub** from their developer branch `$ git push origin Developername`. Developers can then follow the prompts in the GitHub repository "Pull requests tab" to merge their Developername branch with the Github master branch (green buttons) and delete their branch after it has been merged with the Github central master branch (purple button).   

### R2: DATAFLOW DIAGRAM
![Dataflow Diagram](docs/DataflowDiagramT3A2-A.png)

### R3: APPLICATION ARCHITECTURE DIAGRAM
![Application Architecture Diagram](docs/ApplicationArchitectureDiagramT3A2-A.png)

### R4: USER STORIES

### PERSONAS
|         | Who are they? | What is their main goal? | What is their main barrier to achieving this goal? |
|---------|---------------|--------------------------|----------------------------------------------------|
| Binge Watcher | A person that uses streaming services such as netflix to binge watch shows and movies | To discuss in real time what is happening in their favourite shows while they are watching them | Finding a chat application that supports live message updates without having to refresh the page/app |

|         | Who are they? | What is their main goal? | What is their main barrier to achieving this goal? |
|---------|---------------|--------------------------|----------------------------------------------------|
| Movie Enthusiast | A person that regularly goes to the cinema to watch the latest movies | To find a place where others that share their interest can gather to discuss the latest movies | Finding a website that facilitates discussion around this mutual interest |

|         | Who are they? | What is their main goal? | What is their main barrier to achieving this goal? |
|---------|---------------|--------------------------|----------------------------------------------------|
| AfterCredits Administrator | Users with admin privileges on the AfterCredits web app | General admin duties around card creation and chatroom monitoring | The functionality present in the app and the authentication mechanism present to limit who can access that functionality |

### STORIES
As a Binge Watcher of TV shows and movies, I want to feel like the discussion I have in the chatroom is happening in real time so we can react/discuss things that are happening as it unfolds.

As a Binge Watcher, I want to be able to use the site on my phone and for it to be a smooth experience so I can stay in the conversation while I am on the move.

As a Binge Watcher, I dont want other users to be able to change my posts, so I know what I post is safeguarded and is my own content.

As a Binge Watcher, I want to be able to contact an Admin so that I can send them feedback about the site or to inform them about issues I have with either the site or other users.

As a Movie Enthusiast, I want to go into chatrooms based around my favourite films/shows with others, so I can share my opinions and gain insight from our discussions.

As a Movie Enthusiast, I want to be able to view the initial content of the site without registering so I can see what it is all about before I go through a potentially annoying and lengthy process of creating an account and giving away my personal details.

As a Movie Enthusiast, I want my posts to be there when I return to the chatroom so I can continue the conversation later.

As a AfterCredits Administrator, I want to have the ability to remove certain user messages from the chatroom if they are deemed to break the terms of service for the web app, so I can ensure the chatroom stays civil even during heated discussions.

As a AfterCredits Administrator, I want to be able to manage movie/series cards for Users to view and interact with, so I can enable users to have their conversations on that particular movie/series.

As a AfterCredits Administrator, I want to be able to join the conversation alongside other users, so I can share my views on my favourite hobby with them.


### R5: WIREFRAMES
Wireframes were prepared using Balsamiq Wireframes. 

**A. Early Beginnings version**
![Core app wireframes: Early Beginnings version](docs/core_app_wireframes.png)
<br>

**B. Expansion version**

![Expanded app wireframes: Expansion version](docs/expanded_app_wireframes.png)

### R6: TRELLO

Planning commenced with a discussion and presentation of various concept ideas. One concept idea was selected and developed into a project idea.

The aim of this project is to build the core app (Early Beginnings) first and then incorporate features from the Expansion version. The aim is not to deliver the full expansion version, but rather to deliver extra features on the core app.   

An Agile methodology will be used in this project. This methodology allows for changing the requirements at any time to adapt to challenges encountered and to incorporate additional features as time permits. The team will manage the project jointly rather than appointing a single project manager. Testing will be performed concurrently with development. 

Trello is a Kanban-style web application used for organizing collaborative projects. Columns represent stages of the process (to do, working on, blocked, finished). Cards represent tasks. These task cards are moved between the column stages as work on the task progresses. The board, as a whole, provides a visual depiction of the project progress. 

The Trello board used for this project is online at: https://trello.com/b/VLtFLtdT/aftercredits

###### Trello Board and Cards Overview

Cards are arranged by 4 main categories:
- To Do - Part A (pink)
- To Do - Back End (cyan)
- To Do - Front End (yellow)
- Other Criteria Part B (orange)

Cards contain information about the relevant task or criteria, a color cover corresponding to the column category (for ease of progress tracking), difficulty level, deadlines and task allocation.

![Trello Board and Cards](docs/trello1.PNG)

###### PART A: Task Allocation

The Trello Board, columns and preliminary cards for the overall project are created. All tasks for Part A are allocated. 

![Part A Task Allocation](docs/trello2.PNG)

###### PART A: Task Progression

Developers work on multiple tasks concurrently. 
![PART A progression](docs/trello3.PNG)
![PART A progression](docs/trello5.PNG)
![PART A progression](docs/trello6.PNG)
![PART A progression](docs/trello7.PNG)

Developers agreed to take a break from the project over the weekend. Card deadline updated from aspirational early-finish deadline to actual deadline:
![PART A progression](docs/trello11.PNG)

Added more Part B card details and checklist items:
![PART A progression](docs/trello12.PNG)

Part A progress continues;
![PART A progression](docs/trello13.PNG)
![PART A progression](docs/trello14.PNG)
![PART A progression](docs/trello17.PNG)
![PART A progression](docs/trello18.PNG)
###### PART A: Completed Tasks

Please visit the Trello board to see expanded details for card activity as recorded over time: https://trello.com/b/VLtFLtdT/aftercredits
![PART A completed dataflow diagram](docs/trello4.PNG)
![PART A completed application architecture diagram](docs/trello8.PNG)
![PART A completed description of website](docs/trello9.PNG)
![PART A completed wireframes](docs/trello10.PNG)
![PART A completed user stories](docs/trello15.PNG)
![PART A completed presentation](docs/trello16.PNG)
![PART A completed trello part A](docs/trello19.PNG)