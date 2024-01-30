# Waldo-backend
This is a repository for the back end of my waldo-phototapping project providing a simple API for  retrieving  and storing the levels and their scores. It was developed using the Express library and MongoDB for the database, using the moongose library.

# Install
Simply clone the project and type in your terminal "npm run serverstart",  you will need to first create a MongoDB database and provide the connection URL to the app.js file. 

# Usage
The models use url to fetch the image,  this why they are specified by a string type. I use an url to images from imgur, but you can use any kind of image provider. 
There is Cors middleware, so if you don't want to use it, feel free to change it.

The next routes have the /api/ prefix and are 100% free, please be kind.

You can retrieve the levels in the /level end route and /level/:levelId/highscores to retrieve the level high scores. 
Also, you can send a POST request to the /level/:levelId with a json object of the kind {positionX:Number, positionY:Number, characterId:String} to check if the character with the correspondent Id is in the position 
(positionX; positionY) of the image.
And last you can send a POST request to the /level/:levelId/Highscores with the object {name:String, score:Number(in ms)} to add a high score to the level.

