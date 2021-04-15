# Getting set up

Once the repo is cloned and dependancies are synced up you will need to CD into two different folders and run the following commands.
1. /client/server nodemon .
2. /client npm start

this will allow the app to run as intended.

## Packages used

### Client:
1. Axios - Promise based HTTP client for the browser and node.js. I used this npm package to help interact with mongodb.
2. Scss - This packages was installed as a method for styling the front end.

### Server:
1. Cors/Express    -    Cors and Express are middleware packages used to help push information to the mongodb.
2. Mongoose        -    Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment.
                     Mongoose supports both promises and callbacks.
3. Nodemon         -    Nodemon is a tool that helps develop node.js based applications by automatically restarting 
                     the node application when file changes in the directory are detected.
  

## A Quick runthrough of the App:

The server side:
I used mongoose to help build a schema that could be pushed up to the mongobd colection for quick and easy storage.

`const mongoose = require ('mongoose');

const TyresSchema = new mongoose.Schema({
    Brand :
    {
        type: String,
        required: true,
    },
    Title:
    {
        type: String,
        required: true,
    },
    Size:
    {
        type: Number,
        required: true,
    },
    Price:
    {
        type: Number,
        required: true,
    },
    Image:
    {
        type: String,
        required: true,
    }
});

const Tyres = mongoose.model("tyrecollections", TyresSchema)
module.exports = Tyres;`
