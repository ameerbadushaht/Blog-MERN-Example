## Install dependencies
 Install [ [Node.js] (url).

### cd Desktop
### cd mern-blog
### npx create-react-app client  #react installation

### index.html -> entry point of Application
### manifest.json -> mobile phone uses

### src/App.js -> Root App component

# Tailwind CSS 

	in site framework guide terminal
	cd client
	npm install -D tailwindcss postcss autoprefixer
	npx tailwindcss init -p

## copy below and in tailwind.config.js file clear content and paste it


		    /** @type {import('tailwindcss').Config} */
		module.exports = {
		content: [
		"./src/**/*.{js,jsx,ts,tsx}",
		],
		theme: {
		extend: {},
		},
		plugins: [],
		}


## copy below and in src/index.css file replace with full content

	@tailwind base;
	@tailwind components;
	@tailwind utilities;


### npm install react-router-dom --save

### navigate btw pages ==> npm install --save react-router-dom


## backend dependencies terminal should be outside of client folder
	npm init -y
	npm install express
	npm install -D concurrently nodemon



## in package.json
  
	change - description 
			-  "main": "index.js" to server.js
			- test to server
			- test content to nodemon
			-change author


## create server.js
	type=>

	const express = require('express'); // Express web server framework
	const app = express(); //express app created
	const port = 8080; //set port


## //just for testing purposes

	app.get('/', (req, res) => res.send('Hello World!'));


	app.listen(port, () => console.log('Example app listening on port ${port}'));


# Download and install Postman
	open postman.exe
	select POST and add localhost link then send

	in Body - raw select JSON
	we can add json object like name...

## ////////////////// ------------database creation-----\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

	Download  mongodb.exe and install.
	 Install mongo shell zip file.

	Copy into C drive and rename as mongosh

	in terminal 
	mongod --version to see version of installed mongodb

	then enter mongod
	shows error =>shutting down
	
	so,
	create folder in  C:\data\db
	Again enter mongod it shows waiting for connection.

	Goto mongosh\bin folder open mongosh.exe 
	Now it opens mongo shell.

==============================================================
## if still not open
	download mongodb zip file

	copy mongodb.zip file to desktop
	in terminal desktop\mongodb\bin enter :-

	if opend in cmd mongod.exe --dbpath c:/data/db  or for vscode in windows .\mongod.exe --dbpath c:/users/Username/Desktop/data/db


## now u can see some files in C:/data/db 

	Then enter .\mongod
	open new terminal in bin folder again enter .\mogod 
	it enters into shell 

====================================================================

## Download and install mongo compass

	create new connection by clicking connect  
	in mongoshell => 
		To create DB 
	       		use DBNAME (eg: use mernblog) 
	        To insert in DB
	    		copy server.js content like
			db.articles.insert([{name:'learn-react',comments:[]},{name:'learn-node',comments:[]},{name:'my-thoughts-on-learning-react',comments:[]}])
		To see DB data
		       db.articles.find({})



## =============  Adding MongoDB to Express ===========================

	Install mongodb in our project 

	npm install --save mongodb

	run server

	open postman 

	select GET and send http://localhost:8080/api/articles/learn-node 


=============================================
### Install fetch 
	npm install --save whatwg-fetch

==============================
## Run application 
	npm run dev	
