# famn

famn is an Angular2 application framework with both client side and server side integrated. 
I have been exploring for such an Angular2 [MEAN](http://mean.io) for a while but w/o an ideal solution, so I write it.

famn stands for [Feathers](http://feathersjs.com/), [Angular2](https://angular.io), [MongoDB](https://www.mongodb.com/), and [Node.js](https://nodejs.org/en/)

famn borrowed much from [angular2-webpack-starter](https://github.com/AngularClass/angular2-webpack-starter), [@angular/material](https://github.com/angular/material2), [ng2-material](https://github.com/justindujardin/ng2-material)

*IMPORTANT* This project has no commercial level of support and it's suggested to use in development for quick prototype. PR is welcome to make it go further.


### Features

- Angular 2 + typescript
- Webpack for both client and server side
- Feathers is to provide realtime service
- All websocket based communications
- MongoDB and mongoose model
- Ngrx for state management
- HMR in development
- Material design
- Docker based

### Development

#### local

```sh
# prepare environment
npm i -g nodemon ts-node typescript@2.0

# or use yarn
yarn add global nodemon ts-node typescript@2.0

# build client code
yarn run build:client:dev

# start server with webpack hmr
yarn run start:hmr
```

#### docker (recommended)

```sh
# docker way which is recommended
docker-compose -f ./docker/docker-compose.dev.yml up --build

# real time service, check the new message in message module after running below command
curl 'http://localhost:3030/messages/' -H 'Content-Type: application/json' --data-binary '{ "email": "yourname@yourdomain.com", "message": "Hello Implus" }'
```

- Go to `http://localhost:3030` for web

### Deploy

```sh
docker-compose -f ./docker/docker-compose.prod.yml up --build -d
```

### To do

- ( ) CLI for project initialization
- ( ) user authorization
- ( ) robust material design data-table
- ( ) charts
- ( ) using npm package of ng2-material instead of local build
- ( ) unit test