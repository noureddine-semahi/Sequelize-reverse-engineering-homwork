Reverse engineering homework by Noureddine Semahi

This app uses the Passport package and allows users to sign up for an account, log into an existing account and logout securely. All user data is stored in a mysql database.
When someone wants to safely sign up or log in to "an account", It’s crucial that the login info remains safely stored.

In this work we have utilized some technologies including:
EXPRESS -EXPRESS-SESSION -MYSQL2 -PASSPORT -PASSPORT-LOCAL -SEQUELIZE- BCRYPT JS

To get started with this app, you need to clone the repository into your local storage. Once this is complete, please follow these steps: 

Create a mysql db called "passport_demo" 
Inside the config folder, open config.js and insert your personal data username, password.
Open the integrated terminal in your repo and run "npm i" to install all node packages.
To start the app you need to run "node server.js" and you will successfully connect to the server.
Open browser and put "http://localhost:8080" in the search bar.

FOLDERS AND FILES:

CONFIG (folder)
	-config.json 
{ connection configuration to connect to server };
-passport.js
 { contains javascript logic that tells passport we want to log in with an email address and password };

MIDDLEWARE (subfolder)

-isAuthenticated.js 
{ restricts routes that a user is not allowed to visit if not logged in. if user is logged in, it continues with request };

MODELS (folder)

-index.js
 { connects to database and imports users log in data };

-user.js 
{ requires "bcrypt" for password hashing. this makes our database secure even if compromised. Here we have JS that defines what is stored on our database };

PUBLIC (folder)
	
	-login.html { Boilerplate html static page which is rendered when }
	-members.html {}
	-signup.html {}
	
	JS (subfolder)
		-login.js {}
		-members.js{}
		-signup.js{}
	
	STYLESHEETS (subfolder)
		-style.css{}



ROUTES (folder)

-api-routes.js 
{ contains routes for signing in, logging out and getting users specific data to be displayed client side };

-html-routes.js
{ routes that check whether user is signed in, whether user already has account etc and sends them to the correct html page };

-package.json 
{ contains all package info, node modules used, version info etc
This file contains all the packages and dependencies information as well as the scripts, versions of each dependency and their licence and the version number };

-server.js
 { requires packages, sets up PORT, creates express and middleware, creates routes and syncs database / logs message in terminal on successful connection to server
The express variable is requiring express package
The session variable is requiring the server session
The passport variable is being used to configure the password information
The port variable is the server whe are running 
The db variable is requiring our Database which is in MODELS(folder)

Then on line 12 it is a Boilerplate code saying that we are using express
On line 15 is telling us that our static directory is located in PUBLIC(folder) 
From line 17 to 19 this is being used to keep track of our users login status.

On line 22 and 23 this is requiring the routes for API and HTML.

From line 26 to 30 we are syncing the database with sequelize. and then console logging in the terminal that we are listening to the localhost 8080 };
