<h1 align="center">William Sjökvist Logbook</h1>

<details open="open">
  <summary><h2>Table of Contents</h2></summary>

- [Mars 29](#Mars-29)
- [April 19](#April-19)
- [April 28](#April-28)
- [May 2](#May-2)
- [May 3](#May-3)
- [May 4](#May-4)
- [May 5](#May-5)
- [May 12](#May-12)
- [May 16](#May-16)
- [May 20](#May-20)
- [May 21](#May-21)
</details>

### Mars 29

- I Set up a GitHub Organization as well as 3 repos: ***backend***, ***mower*** and ***app***. I invited all of the team members to the organization and we also set up a Discord server with corresponding roles.

- Set up a base development environment for the backend and pushed it to the repo. 

### Mars 30

- Added a style guide to the project, the team agreed to use Google's. 

### April 19

- Added Google Vision API calls and an image recognition route which returns the name of the object within the image.
- Added a .env file which contains all our API keys. This is .gitignored in the project so as to not expose the API keys, and was instead passed around in our private Discord.

### April 28

- Added GET requests for /object-collision and /boundary-collision. So it is possible to fetch collisions. It is also possible to fetch by the date.
- Set up unit testing for boundary collion

### May 2

- The object identification route now crops the image by the most dominant object, so that background objects ( which it can be more certain of, like a sun for example ) won't be returned as the collided object.
- Set up unit testing for image recognition and object-collision route.

### May 3

- Fixed Swedish locale formatting for the date keys in the databases.

### May 4

- I cleaned up the code on the raspberry, and made the HTTP requests which send a photo and coordinates when collisions occur. 

- Fixed a bug which caused the backend to not accept JSON formatted request bodies.

### May 5

- Added the object-collision and boundary-collision API requests on the Raspberry when they should be fired. 

### May 12

- Decoupled business logic from the routes for cleaner code and ability to potentially switch the business logic implementations.

### May 16

- Refactored the error handling. Added a MowerApiError object which has fields for message and HTTP status code. Added many predefined errors, such as GOOGLE_VISION_FAILED_TO_REACH, LOG_OBJECT_COLLISION_FAIL etc.

### May 20

- Added a query parameter to the GET routes for boundary-collision and object-collision, for getting the last collision points within a set time interval. Defaults to getting the collision points from the last 5 minutes.

- Refactored the GET routes for boundary-collision and object-collision which to remove code duplication.

- Fixed bug where object-collision images were not stored on the server. 

### May 21

- Changed some of the API documentation to make it easier to understand
