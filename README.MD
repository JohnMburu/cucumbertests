## CUCUMBER e2e Web Browser Automation #
This tutorial describes the basic process of web automation using Cucumber

# Step 1#
- Install Nodejs
- Install npm (Usually comed bundled up with Nodejs)

To Confirm that installation is done, run the following commands in your favourite terminal
```
node -v
npm -v
```
# Step 2#
Create an empty cucumber project
```
mkdir hellocucumber
cd hellocucumber
npm init --yes
```
locate the *package.json* file, update the line

```
"test": "echo \"Error: no test specified\" && exit 1"
```
with 

```
 "test": "cucumber-js"
```

# Step 3#
Add cucumber Development dependency

Run 
```
npm install cucumber --save-dev
```

# Step 4#
Prepare the file structure:

```
mkdir features
mkdir features/step_definitions
```

# Step 5#
Create a file called *cucumber.js* at the root of your project and add the following content:
```
module.exports = {
  default: `--format-options '{"snippetInterface": "synchronous"}'`
}
```

Also, create a file called features/step_definitions/stepdefs.js with the following content:

```
const assert = require('assert');
const { Given, When, Then } = require('cucumber');
```

You now have a cucumber project set up.

to confirm your set up, run

```
# Run via NPM
npm test

# Run standalone
./node_modules/.bin/cucumber-js
```
You should see the following

```
0 Scenarios
0 steps
0m00.000s
```
# Step 6 (optional) Git set up#
you might want to start saving your code to git at this point
I have Created a *.gitignore* file at the root of the project folder and added
```
node_modules
```
This will make sure that node_modules are not pushed to the repo

Once that is done run
```
git init
git add .
git commit -m "Your Commit Message goes here"
git remote add origin <giturl>
git push -u origin master
```
