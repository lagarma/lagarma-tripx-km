# TripX Individual KM Mini Project
Organization Branch - Created Pages and Components for the users to integrate, manipulate, and explore.

##  Scripts to run
In the project directory, your can run:

`npm run start`

Runs the app in the development mode. <br />
Open http://localhost:3000/ to view it in the browser.

The page will reload if you make changes to the code and save it.

`npm run test`

Launches the test runner in the interactive watch mode.

## How to run the app
1. Clone the repository and open the folder in the CLI
2. Install all dependencies using the `npm i` or `npm ci` command
3. Start the app using the `npm run start` command. The app will be served at http://localhost:3000/

## User Stories
- User will see the list of Organization with initial details
- From the list, User can search any Organization Names using the Organization Code provided
- User can click a link of the Organization Name from the list. It will provide the General info as well as the license information
- User can view and create a license of that particular Organization Code
- User can create an Organization
- User can update details of an Organization

## Features
### Search

![alt text](https://github.com/lagarma/lagarma-tripx-km/blob/main/screenshots/Screen%20Shot%202021-10-12%20at%209.57.39%20AM.png)

 - Search gets sent to backend and provide the data to the user
 - Searching empty data will return all Organizations
 - Reset button for clearing inputs

### Organization List

![alt text](https://github.com/lagarma/lagarma-tripx-km/blob/main/screenshots/Screen%20Shot%202021-10-12%20at%2010.12.19%20AM.png)

 - Query for all Organizations in a List
 - Clicking an Organization Name link will redirect you to that particular Organization
 - Paging feature to limit users scrolling down from the long list of Organizations

### Create Organization

![alt text](https://github.com/lagarma/lagarma-tripx-km/blob/main/screenshots/Screen%20Shot%202021-10-12%20at%2010.12.39%20AM.png)

 - Create Organization with providing details:
    * Organization Code
    * Organization Name
    * Distribution Category
    * Org Level (Default: 1)
    * Organization Name in French
 - Create gets sent to backend and include it to the list of Organizations
 - Empty Organization Code will not be accepted
 - Can cancel Create Organization using the "Cancel" or "X" button

### Organization Details

![alt text](https://github.com/lagarma/lagarma-tripx-km/blob/main/screenshots/Screen%20Shot%202021-10-12%20at%2010.13.01%20AM.png)

 - This page will appear from the Organization Name link
 - Details provided as well as licenses of that particular Organization
 - Expandable panel to choose between General and License section
 - Can edit Organization Details and save it. Get sent to backend to update the data

### Add License

![alt text](https://github.com/lagarma/lagarma-tripx-km/blob/main/screenshots/Screen%20Shot%202021-10-12%20at%2010.13.07%20AM.png)

 - Add license information with providing details:
   * Effective Date
   * Expiry Date
   * License Number
   * License Type
   * Province
   * Status
 - License data gets send to backend to add it to the Organization
 - Can create multiple licenses

## Technologies used and Dependencies

ReactJS and MUX components were used in this project. For Testing, Jest/React testing library/Enzyme

## Troubleshooting Guide
Some dependencies might not work if you're not using updated node and NPM. For testing components, Enzyme is still using React 16 and your React version might be on version 17. You can downgrade your React to 16 by running `npm install --save react@16 react-dom@16`. To revert back to updated React version, you can run `npm install --save react@^17 react-dom@^17`. Make sure when you downgrade/upgrade React, you should also do it in React-dom to make sure there will be no interconnecting package issues.
