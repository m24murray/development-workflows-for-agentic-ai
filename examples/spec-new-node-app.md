# Specification for Web-Signup Application

## Project Overview
The Web-Signup application is a Node.js front-end web app built using Express.js and TypeScript. It is designed to allow users to register for a new user account by submitting their name and email. This app is part of a demo, so the focus is on getting something functional up and running quickly.

## Technical Details
- **Framework**: Node.js with Express.js
- **Language**: TypeScript
- **Dependency Management**: npm
- **Templating Engine**: Nunjucks
- **Design System**: GOV.UK Design System (installed via `npm install govuk-frontend --save`)
- **Validation Library**: Basic validation with regex for email
- **Common Libraries**: Use libraries like lodash for commonly used functions
- **Build Commands**:
  - `build`: Compile TypeScript using `tsc`
  - `start`: Start the application
  - `test`: Placeholder for future unit tests
  - `dev`: Hot reload for development

## Application Overview
The application consists of four screens:

1. **Start Page**
   - Displays basic text explaining what the service does.

2. **Enter Your Contact Details**
   - A form with the following fields:
     - **Name**: Text input with validation (min length: 0, max length: 20).
     - **Email**: Text input with validation (regex for email format, min length: 0, max length: 20).

3. **Summary Page**
   - Displays a summary of the information entered on the previous screen (name and email).

4. **Submitted Page**
   - Confirms the form has been completed.
   - Includes a button to return to the Start Page.

## Validation Details
- **Name**: Minimum length of 0 and maximum length of 20 characters.
- **Email**: Regex validation for email format, with a minimum length of 0 and maximum length of 20 characters.

## Out of Scope
- Backend API for data persistence (stubbed for now, logs data to the console).
- Authentication (to be implemented later).
- Unit testing (to be implemented later).

## Development Notes
- Follow the GOV.UK Design System strictly for all components and styles.
- Use the console to log submitted data as a stubbed backend.
- Prioritise simplicity and functionality to meet the demo's requirements.
