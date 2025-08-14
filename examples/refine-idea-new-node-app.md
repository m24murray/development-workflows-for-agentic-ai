# Spec prompt

You are an expert software engineer/architect and you will help me write a specification for a new app that I want to build. This app is actually being created as part of a demo, so i favour getting something up-and-running as quickly as possible, over getting things perfect.

## Project overview
I want to create a new Node.js front-end web app. It will comprise of a series of forms to allow a user to submit user information.

### Details
* Node.js express, with typescript
* Use npm for dependency management
* Implement standard build commands for the app in package json. build using tsc, hot reload, run tests
* This is really important, the app must be GDS compliant, so please use the GOV.UK Design System (styles, components, patterns) as much as possible (this is installed with npm install govuk-frontend --save)
* Consider using libraries for commonly used functions, e.g. lodash
* Just use latest stable versions of npm dependencies
* Use nunjucks for templating 

#### Out of scope
* Eventually we'll have a backend api that we can persist some data to. But for now we'll just stub this out and log the data instead.
* Don't worry about auth for now, we'll implement this later. 
* Don't worry about unit testing, will implement this later

### Application overview
* Lets call the app, web-signup
* It allows the user to register for a new user account using their name and email
* 4 screens
  * Start page - some basic text explaining what the service does
  * Enter your contact details - form with name and email fields for the user to input
  * Summary - summary of the information from previous two screens (name and email)
  * Submitted - An screen confirming the form has been complete. It should have a button that brings the user back to the start page
* Just put basic validation on all of the form fields, im not too worried the specifics for now, but maybe something like min length 0, max length 20. I'll extend on this manually.

## Refinement instructions
I want you to take the details above and help me to refine. Ask me one question at a time so we can develop a detailed spec. 

At the beginning of your response for refining the questions I want you to give me an idea of how many questions you have. 

Remember, as this is part of a demo, limit this to 3 questions, keep it simple. 

## Final output
Create a new file in this project directory called `spec.md`. I want you to update that file to include the information provided to you in the details above, as well as the answers to your refinement questions.
