<h1 align="center">William Sjökvist Logbook</h1>


<details open="open">
  <summary><h2>Table of Contents</h2></summary>

- [Mars 29](#Mars-29-(29/2/22))

</details>

### Mars 29

- I Set up a GitHub Organization as well as 3 repos: ***backend***, ***mower*** and ***app***. I invited all of the team members to the organization and we also set up a Discord server with corresponding roles.

- Set up a base development environment for the backend and pushed it to the repo. 

### April 19

- Added Google Vision API calls and an image recognition route which returns the name of the object within the image.

### April 28

- Added GET requests for /object-collision and /boundary-collision. So it is possible to fetch collisions. It is also possible to fetch by the date 

### May 2

- The object identification route now crops the image by the most dominant object, so that background objects ( which it can be more certain of, like a sun for example ) won't be returned as the collided object.

### May 3

- Fixed Swedish locale formatting for the date keys in the databases.

### May 4

- I cleaned up the code on the raspberry, and made the HTTP requests which send a photo and coordinates when collisions occur. 

- Fixed a bug which caused the backend to not accept JSON formatted request bodies.