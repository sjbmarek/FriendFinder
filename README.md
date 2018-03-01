

# Friend Finder - Node and Express Servers

### Overview

This is "FriendFinder"-- basically a dating app. This full-stack site will takes in results from users' surveys, then compares their answers with those from other users. The app will then display the name and picture of the user with the best overall match. 

Npm modules:  Express, Body-parser and Path.
Deployed to Heroku.


### App Basics

1. A survey of 10 questions with answers on a scale of 1 to 5 based on how much the user agrees or disagrees with a question.

2.  `htmlRoutes.js` file contains two routes:

   * A GET Route to `/survey` displays the survey page.
   * A default, catch-all route that leads to `home.html` which displays the home page. 

3.  `apiRoutes.js` contains two routes:

   * A GET route with the url `/api/friends` used to display a JSON of all possible friends.
   * A POST route `/api/friends` which handles incoming survey results. This route handles the compatibility logic. 

4. Compatibility logic:

   * Compare the users survey to each possible friend in the library.  
   * The match score will be sum of the absolute values of the differences of values for each survey question.
   * Find the lowest match score
5. The result is displayed as a modal pop-up with the name and picture of the closest match.

### App Additions

Future work on this project: 
  * Form validation for name and photo link
  * Friend object shuffle (current logic selects the first lowest match score when looping through the friend object).  A Fisher-Yates Shuffle could be added to accomplish this.

- - -

### Added To My Portfolio

