# Sergioloman.13
E-commerce back-end

Hello everyone, and welcome to the back-end of our E-commerca bank application. Here we test out the communication in between Database and Server thanks to the power of "Sequelize". Keep reading to learn everything works.

## Contents

* [Installation](#Installation)
* [Features](#Features)
    * [Server](#Configuration)
    * [Models](#Models)
    * [Seeds](#Seeds)
    * [Routes](#Routes) 
* [Test](#Test)
* [Bonus](#Bonus)

## Installation

Clone the app repository into your local files. Find it on Github ***[HERE](https://github.com/Sergioloman/Sergioloman.13)***

You will need to write ***npm install*** to enable modules such as ***express***, ***sequelize*** both of them will handle the server and the connection to our mysql database.Additionally, it will install vital packages such as ***dotenv*** and ***mysql2***.

Once you do so you will need to create a ***.env*** file in your root directory. Once you have done so, write the following inside of it:

    DB_NAME= ecommerce_db
    DB_PW= ***your mysql password***
    DB_USER= root

This will enable our application to use your mysql password securely.

Finally, be sure to create a ***.gitignore*** file. there write:

    node_modules
    .env
    .DS_Store

Now you are set and can push your directory to github while safely securing your password.

## Features

Our application, features a number of standard features. Its file structure allows us to easily pinpoint the main components of it.

### Server

Our Server.js file runs the show. Not only contains our dependencies such as our npm modules but also runs our connection to our database and our middleware.

Be sure to write the following command in your command line prior to running the application: ***npm run seeds*** this will load the seeds necessary to visualize our data.

#### Configuration and Databases
You will see that our file structure has a ***db*** and a ***config*** files. The DB folder contains our mysql schema wich will be populated in our server using the models.

Our config folder contains the middleware for the connection to sequelize, wich will allow us to use the package and interact with the mysql database.

### Models

Our Models are how we create our tables, and populate our schema. Each model correspond to a particular set of data.

Notice that our ***index.js*** file will handle the interactions and associations in between each of the models.

Thanks to the power of ***sequelize*** we are able to write tables and schema using javascript rather than cumbersome mysql commands.

### Seeds

Our seeds contain the hard data for our database. Rather than be written on a ***sql*** file. Our seeds are written in javascript and can be read using sequelize, which is handled by the **index.js** file inside the seeds folder.

We are going to be able to display, add, update, delete all of the paratemeres and values inside of it with our API requests.

### Routes

Now that we have our data and our connection to the server all set up. We now need to be able to make calls to the server and receive their information for further display in our application.

Our Routes handle our CRUD operations ( Create, Read, Update, and Delete) allowing us to perform changes to the value in our tables. Each api route handles a set of data correspondant to the modules we describe earlier.

All of the routes will look like ***http://localhost:3001/api/***  + your choice of *categories*, *tags*, or *products*, followed by the following characters depending on the CRUD action of your choice:

**Get**
 * / 
Returns all of the data in the table plus any associated data. Check out **index.js** insode of **models** to see the associations.
 
 * /:id 
Returns a particular set of data with index equal to the id. writing "/4" will return the data at index 4 of the table.

**Post (create)**
 * / 
Enables the creation of a new set of data in the body of the request. Be sure to write it in JSON format!

**Put (update)**
 * /:id 
Updates data at a particular index with the JSON inside the body of our request. 

**Delete** 
 * /:id
Deletes the data at the chosen id.

## Test
Our CRUD is all set. What now? Withouth a front end it makes it a bit difficult to see if our API calls are working; Thankfully, we have ***[Insomnia](https://insomnia.rest/)*** to help us out here. 

Once you have open Insomnia, make sure that your server is on by running ***npm run seed*** and ***node server.js*** in the command line. Then you will be able to try out the proper URLS with the right API request using insomnia. 

## Bonus

Once running the application should look like the following ***[demo](https://drive.google.com/file/d/1hCEKdVZpRpLFNhILrwhsUlkqJbmlDvVF/view)***  :

"https://drive.google.com/file/d/1hCEKdVZpRpLFNhILrwhsUlkqJbmlDvVF/preview"

As always. Thank you for stopping by and *happy coding*

[Sergioloman](https://github.com/Sergioloman)




