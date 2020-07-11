# SmartBrain
## Overview
SmartBrain is a project for a course I took designed to cover all aspects of modern web development.
It covers 3 main areas
  1. Front end using React.js
  2. Back end using Node.js
  3. Postgres Databse to hold user data

## Front End
The front end project can be found in the **facereconitionbrain** folder.
The front end was created using React.js and has each component organized and seperated for easy reusability.
The application uses the Clarifai API to detect faces in images

## Back End
The back end project can be found in the **facereconitionapi** folder.
The back end RESTapi was created using Node.js

## Database
SmartBrain uses the **Postgres Relational Database**
The database contains 2 tables, a users table and a login table

### Users table
The users table can be created with the folling SQL command:
```
CREATE TABLE users(
  id serial PRIMARY,
  name VARCHAR(100),
  email text UNIQUE NOT NULL,
  entries BIGINT DEFAULT 0,
  joined TIMESTAMP NOT NULL
  );
```
### Login table
The Login table can be created using the following SQL command:
```
CREATE TABLE login(
  id serial PRIMARY KEY,
  hash VARCHAR(100) NOT NULL,
  email text UNIQUE NOT NULL
  );
```





