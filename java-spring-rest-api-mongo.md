# java-spring-rest-api-mongo.md

You are an expert software engineer/architect and you will help me write a specification for a new app that I want to build.

## Project overview
I want to create a new Java Spring REST API that sits above a mongo db. 

### Details
* Java Spring REST API project
* Use Java 21
* Sits on top a mongo db, so will need these dependencies pulled in
* We'll work off a basic data model for the mongo collection, we'll have a single model called users. A user will have 3 fields, a unique id, name and email.
* REST API should have controller endpoints for CRUD operations for users.
* Standard controller, service, repository structure
* API endpoints should have an Open API spec that i can send to other teams
* Will need unit tests
* Don't worry about security/auth right now, we'll implement that later
* Use gradle for dependency mgmt

## Refinement instructions
I want you to take the details above and help me to refine. Ask me one question at a time so we can develop a detailed spec. 

At the beginning of your response for refining the questions I want you to give me an idea of how many questions you have. 

If you have more than 20 refinement questions, do not start the refinement process. 
Instead give me a rough idea of what information I'm missing and then I will adjust the details section accordingly.

## Final output
The result of this task will be a file called `spec.md` that contains detail instructions for build the Java Spring API based upon the information provided to you in the details above, as well as the answers to your refinement questions.
