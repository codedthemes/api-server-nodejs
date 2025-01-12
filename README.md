
# Nodejs API Server

Express / Nodejs Starter with JWT authentication, MongoDB - Provided by **AppSeed** [App Generator](https://appseed.us/app-generator).
Authentication is based on [json web tokens](https://jwt.io). `passport-jwt` strategy is used to handle the Email/Password authentication. After a successful login the generated token is sent to the requester. 

<br />

> Free Support: 

- Github (issues tracker) 
- Email: **support @ appseed.us** (max 12h response time)
- **Discord**: [LIVE Support](https://discord.gg/fZC6hup) (registered AppSeed Users) 

<br />

![Nodejs API Server - Open-source Nodejs Starter provided by AppSeed.](https://user-images.githubusercontent.com/51070104/124414813-142aa180-dd5c-11eb-9279-6b082dadc51a.png)

<br />

## Requirements

- [Node.js](https://nodejs.org/) >= 10.x
- [MongoDB](https://www.mongodb.com/) server 

<br />

## How to use the code

**Clone the sources**

```bash
$ git clone https://github.com/app-generator/api-server-nodejs.git
$ cd api-server-nodejs
```

**Install dependencies** via NPM or Yarn

```bash
$ npm i
// OR
$ yarn
```

**Start the API server**

```bash
$ npm start
// OR
$ yarn start
```

The API server will start using the `PORT` specified in `.env` file (default 5000)

<br />

## Codebase Structure

```bash
< PROJECT ROOT >
   |
   |-- config/                              
   |    |-- config.js             # Configuration       
   |    |-- passport.js           # Define Passport Strategy             
   | 
   |-- models/                              
   |    |-- activeSession.js      # Sessions Model (Mongo)              
   |    |-- user.js               # User Model (Mongo) 
   | 
   |-- routes/                              
   |    |-- users.js              # Define Users API Routes
   | 
   | 
   |-- api.js                     # API Entry Point
   |-- .env                       # Specify the ENV variables
   |                        
   |-- ************************************************************************
```

<br />

## Mongo Settings

The Mongo URI lives in `config/keys.js`

```javascript
... = 'mongodb://localhost/api_server_nodejs'
```

<br />

## API

For a fast set up, use this POSTMAN file: [api_sample](https://github.com/app-generator/api-server-nodejs/blob/master/media/api.postman_collection.json)

> **Register** - `api/users/signup`

```
POST api/users/signup
Content-Type: application/json

{
    "username":"test",
    "password":"pass", 
    "email":"test@appseed.us"
}
```

<br />

> **Login** - `api/users/login`

```
POST /api/users/login
Content-Type: application/json

{
    "password":"pass", 
    "email":"test@appseed.us"
}
```

<br />

> **Logout** - `api/users/logout`

```
POST api/users/logout
Content-Type: application/json
authorization: JWT_TOKEN (returned by Login request)

{
    "token":"JWT_TOKEN"
}
```

<br />

## License

MIT @ [AppSeed](https://appseed.us)

<br />

## Credits

This software is provided by the core AppSeed team with an inspiration from other great NodeJS starters: 

- Initial verison - coded by [Teo Deleanu](https://www.linkedin.com/in/teodeleanu/)
- [Hackathon Starter](https://github.com/sahat/hackathon-starter) - A truly amazing boilerplate for Node.js apps
- [Node Server Boilerplate](https://github.com/hagopj13/node-express-boilerplate) - just another cool starter
- [React NodeJS Argon](https://github.com/creativetimofficial/argon-dashboard-react-nodejs) - released by **Creative-Tim** and [ProjectData](https://projectdata.dev/)

<br />

---
[Nodejs Starter](https://appseed.us/boilerplate-code/nodejs-starter) - provided by AppSeed [App Generator](https://appseed.us)
