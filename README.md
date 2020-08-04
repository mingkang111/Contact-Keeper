# Contact-Keeper
A web application for users to save their contacts. (Full Stack Development with MERN)

# Demo
view the [demo](https://gentle-bastion-16273.herokuapp.com/).

# Tech stacks
React.JS, MongoDB, Express.js, Node.js, JWT, MERN stack, Java, JavaScript, HTML 5, CSS

# Highlight
Developed an interactive web page for users to add, update, create and view contacts with React.js ( with React Hooks and Context API for state management). <br>
Used Node.js and Express.js for creating contacts and users API for the frontend to interact as well as the user authentication is based on JWT(JSON Web Token). <br>
Built with MongoDB to store the users' data and contacts data.

# RESTful APIs
RESTful API for contacts that uses JWT authentication. <br>
All contact endpoints are protected and each registered user has their own contacts.

## API Usage & Endpoints

### Register a User [POST /api/users]

- Request: Add user and request JSON web token

  - Headers

        Content-type: application/json

  - Body

            {
              "name": "",
              "email": "",
              "password": ""
            }

- Response: 200 (application/json)

  - Body

          {
            "token": ""
          }

### Login with a User [POST /api/auth]

- Request: Login with credentials to recieve a JSON web token

  - Headers

        Content-type: application/json

  - Body

            {
              "email": "",
              "password": ""
            }

- Response: 200 (application/json)

  - Body

          {
            "token": ""
          }

### Get Contacts [GET /api/contacts]

- Request: Get all contacts of a specific user

  - Headers

        x-auth-token: YOURJWT

* Response: 200 (application/json)

  - Body

          {
            "contacts": []
          }

### Add New Contact [POST /api/contacts]

- Request: Add a new contact

  - Headers

        x-auth-token: YOURJWT
        Content-type: application/json

  - Body

            {
              "name": "",
              "email": "",
              "phone": "",
              "type": "" [personal or professional]
            }

- Response: 200 (application/json)

  - Body

          {
            "contact": {}
          }

### Update Contact [PUT /api/contacts/:id]

- Request: Update existing contact

  - Parameters

    - id: 1 (number) - An unique identifier of the contact.

  - Headers

        x-auth-token: YOURJWT
        Content-type: application/json

  - Body

            {
              "name": "",
              "email": "",
              "phone": "",
              "type": "" [personal or professional]
            }

- Response: 200 (application/json)

  - Body

          {
            "contact": {}
          }

### Delete Contact [DELETE /api/contacts/:id]

- Request: Delete existing contact

  - Parameters

    - id: 1 (number) - An unique identifier of the contact.

  - Headers

        x-auth-token: YOURJWT

* Response: 200 (application/json)

  - Body

          {
            "msg": "Contact removed"
          }


## Usage
### Install dependencies <br>
`
npm install 
`
<br>
`
npm client-install
`

### Mongo connection setup
Edit your /config/default.json file to include the correct MongoDB URI <br>

## Run Server
`
npm run dev   
`
<br>
`
npm run server  
`
<br>
`
npm run client 
`
