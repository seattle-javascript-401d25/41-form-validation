![cf](https://i.imgur.com/7v5ASc8.png) 
# 401 JS --  Lab 41 -Form Validation

## Submission Instructions
  * Continue working from previous labs 36-40
  * Work in a branch on your fork
  * Submit a pull request to your forked repository
  * Submit a link to your pull request on canvas
  * Submit the following two links
     * Your deployed Heroku frontend **that reflects the new changes for form validation** 
     * Your deployed Heroku backend
  * Submit a question, observation, and how long you spent on canvas  
  * Submit the Github URL to the backend repo you selected
  * Submit any necessary `.env` variables for BOTH your backend and front end projects so that TA's can have an easier time configuring their environments
 
## Feature Tasks 
* Run `npm i validator` and use the `validator` module demonstrated in lecture today to add validation to your `AuthForm` component
* Add error handling for a 409 conflict error if a user submits a username or email that is already in the database
* Deploy your frontend app with these new changes and submit the Heroku URL
* **Your deployed app must be at an MVP working state to get full credit. The MVP deployed requirements are:**
    * You must be able to sign up or login and see your `/dashboard` page
    * You must be able to create AND edit a new profile, and upon logging out and logging in, see that same profile
    * You must be able to upload photos successfully, and see those photos displayed on the page upon each login session
    * Remember, cookies are NOT cached on the Heroku free tier, so don't worry about persisting login sessions for now.
* Because of the cookie restrictions on deployment, Google OAuth will **not work completely**. *However*, you must still have deployed OAuth working at these MVP steps:
    * User clicks "Sign up with Google"
    * User sees the Google consent screen
    * User returns back to the signup/login homepage (because we are unable to store cookies on deployment on the free Heroku tier at this time, so we are unable to go the `/dashboard` page as we properly should)
  
### backend
* Ensure your `Config Vars` on your deployed Heroku backend contain all the necessary `.env` variables in order to work. Make the necessary changes, i.e. anything referencing `localhost` should now point to your deployed URLs instead

### frontend
* Amazon Cloudfront NOT required going forward, so please do not put a `CDN_URL` in your Heroku Config vars
* Ensure your front end has an `index.js` and you have installed Express via `npm i express` so you can serve your front end code through Heroku
* Ensure your front end `package.json` has the following scripts in order to work properly:
```
"start": "npm run build && node index.js",
"heroku-prebuild": "npm uninstall cypress",
"heroku-postbuild": "webpack --progress --config webpack.prod.js"
```
* Disable automatic Travis integration by renaming your `travis.yml` file to something such as `X-travis.yml`. This makes it so that your Github pushes will not automatically run through Travis

 
## Stretch Goals
* Write Cypress tests for your validation
* Add server-side validation for your username/password/email properties on your Mongoose schema
* Add server and client side validation to your profile or asset upload properties 
  

##  Documentation  
Write a description of the project in your README.md. 
