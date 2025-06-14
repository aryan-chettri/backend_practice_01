# backend_practice_01

//#1 Step is to create a git repository and initialize the project.

//#2 Step to run a command in terminal to "npm init" and initialize all the variables.

//#3 Step is to create a folder "public" and inside it create a new folder "temp".

//Now inside the "temp" folder, create a new file called ".gitkeep".

//#4 Step: create a new file named ".gitignore" in the global root directory

//#5 Step: go to url "https://mrkandreev.name/snippets/gitignore-generator/" and go to the input field and type Node and click on Create.

//#6 Step: copy the generated code from that url "https://mrkandreev.name/snippets/gitignore-generator/" amd paste it in the ".gitignore" file.

//#7 Step: Create an ".env" file in the root directory.

//#8 Step: Create a new file ".env.sample" in the root directory

//#9 Step: Create a new folder called "src" in the root directory and inside it create three new files called "index.js", "constants.js" and "app.js".

//#10 Step: Now, go into package.json and add this: ("type": "module")

//#11 Step: Now, change this to the file :

 "scripts": {
    "dev": "nodemon src/index.js"
  }

//#12 Step: Now go to the terminal and run the command "npm i -D nodemon" to install nodemon as a dev dependency.


Now just commit all those files and folders and push them all in your git repository

//#13 Step: Now go to your terminal and run this command prompt "npm i -D prettier"

#14 Step: Create a file ".prettierrc" in the root global directory and within it add: "{
    "singleQuote": false,
    "bracketSpacing": true,
    "tabWidth": 2,
    "trailingComma": "es5",
    "semi": true
}"

so that every one comes in the same page regarding the syntax

#15 Step: Create one file nammed ".prettierignore" in the root directory where all those files will be kept in which the prettier settings won't get applied

within ".prettierignore" add: 

/.vscode
/node_modules
./dist

*.env
.env
.env.*


//// End of the first day of setting up the project



///Start of the Second day for setup for backend project.

Step #1: Start with setting up the MongoDB Atlas go to this link "https://www.youtube.com/watch?v=w4z8Py-UoNk&list=PLu71SKxNbfoBGh_8p_NS-ZAh6v7HhYqHW&index=8" and see the first 10 seconds for the step of the MongoDB Atlas.

Step #2: Go to the .env file and add your PORT and MONGODB_URI into that file again if you have any confusion adding the MONGODB_URI just take the reference from the vedio above.

Step #3: Now after these two points have been set run a command in the node terminal "npm i mongoose express dotenv" --> This will add all the dependencies that you have installed.

Step #4: The most important thing after this is to "src/index.js" and configure dotenv package.

Step #5: Go to the "src/constants.js" and add: export const DB_NAME = "vediotube" ---> This is the name of your database.

Step #6: Now after that, go to your "src/db/index.js" file and write the part of code that is responsible for connecting your database and export that function as "connectDB"

Step #7: After Step 6 import the function connnectDB and call that function inside "src/index.js"


Step #8: After all of this go inside "package.json" and add : 

"scripts": {
    "dev": "nodemon -r dotenv/config --experimental-json-modules src/index.js"
  }

to your script tag that will make sure that is experimental feature is obtained.

Step #9: Final step is that to go the terminal and to run this command "npm run dev"