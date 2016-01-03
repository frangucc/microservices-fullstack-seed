# microservices-fullstack-seed

Complete (work in progress) E2E stack based on Docker+Git and the Microservices architecture. Begins with a fool-proof Docker install and NPM install to a full deployment with Empire. Code architecture is done with Redux, React with Go and Node for workers. Using Material-ui react components for the front end with some opinionated mircoframeworks and code patterns such as Immutable.js. All front-end JS written in ES6/Babel. 

> [Demo App](http://3db5fb2b.ngrok.com) 
> Grokking from my machine Demo App TTFB super slow :p

### STEP ONE - ECS CONTAINERS, NO OPS & CONTINUOUS DELIVERY (12Factor stuff)
- Use docker to establish a GO continuous delivery server based on Thoughtworks https://github.com/gocd/gocd-docker or better, decide on whether or not to use CircleCI or Codeship, choose one (but describe why we want this).

> After some research and careful consideration I am going with Empire. Empire is a control layer on top of Amazon EC2 Container Service (ECS) that provides a Heroku like workflow. It conforms to a subset of the Heroku Platform API, which means you can use the same tools and processes that you use with Heroku, but with all the power of EC2 and Docker.

No Ops Library | Links | Github | Status
--- | --- | --- | ---
Empire | [Empire Quickstart](http://empire.readthedocs.org/en/latest/) | [Empire Github](https://github.com/remind101/empire) | Implementing
12 Factor Theory | [12 Factor Theory](http://12factor.net/) | Irrelevant | Evaluating

###### Franchino screencast explaining how to use Empire

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/pFC5Tp-QYjk/0.jpg)](http://www.youtube.com/watch?v=pFC5Tp-QYjk)

Dependencies for Empire | Links |
--- | --- | ---
Amazon EC2 Container Service | [Amazon Explainer on ECS](http://aws.amazon.com/ecs/) |
A PostgreSQL database. We use Amazon RDS | [RDS](http://aws.amazon.com/rds/postgresql/) |


``` ACTIONS: Run Empire and let it set everything up using Docker and ECS. Be live in the cloud and deploying like a boss. Establish key commands for destorying, booting and hosting and restarting. ```


> In terms of application servers and general workers, do the following:

- Toss in two servers and default one to GO for our web-app. Have Node in there just because we may use it later, there's good stuff ready to go for Node we may use later. Be sure they're on socket.io or better (if even necessary with GOLANG)
- Have one server send some JSON through the docker container, the other right off the app server. Make the application server and the JSON server seperate. Put a store on both servers, whichever you choose.


``` ACTION: fire up the servers and test them, be sure they're running, open them in the browser with bash ```


### STEP TWO - IMPLEMENT A CODE ARCHITECTURE via YO
- I like Redux/React right now. But maybe you're still on FLUX or even Angular or Backbone. Use YO to pick your poison.
- Implement redux with the following tree structure: actions, components, constants, containers, reducers and store_enhancers (make strong argument for any others (ie. routes, assets)): must use yeoman generators to build project folder structure as my front-end is opinionated. If you prefer another, you may choose from these following options: yo x, yo y, yo z (as long as your starter builds on the containers services, you're good)

-- install redux-scaffold, redux-devtools, redux-log and id any others

``` scaffolding commands go here ```

> GETTING STARTED

``` git clone git@github.com:frangucc/microservices-fullstack-seed.git ```

``` npm install ```
``` yo redux-react // scaffold out sound-redux ```
``` bower install // install any js dependencies ```
``` npm start // fire up localservers ```

> If someone maintains a better yo scaffold for getting started us it not mine.

[Yo generator-react-webpack-redux](https://github.com/stylesuxx/generator-react-webpack-redux)

``` npm install yo ```
``` npm install -g generator-react-webpack-redux ```

> See generator commands [Yo generator-react-webpack-redux](https://github.com/stylesuxx/generator-react-webpack-redux)

- Use npm start, gulp and/or webpack with support for ES6, lint, babel and hotloader

### STEP THREE - MAKE AN APP (OR STEAL ONE MUAHAHAHAHAAHAHA)
- Recreate and enahnce the http://search.dronestre.am/ search UI by injesting the http://api.dronestre.am/data feed. Use material-ui react components to render my much sexier looking view.

- Reverse engineer the sound-redux app because that's what a real hacker would do

--- Consider https://github.com/ipselon/material-ui-prepack on the UI
--- Use the scaffolding tool

- Demonstrate a reducer on the http://api.dronestre.am/data service

- Create a custom react component from hardly even bowered javascript library such as numbers.js or tangle.js. Use it to crunch the terrifying dronestrike data

- Create a three.js or d3.js visualization component to visualize the drone strike data

``` Run the app in the browser ```

### STEP FOUR
- Write a mocha/chai test to test the action, reducer and a componenet responsible for the search and it's results

https://github.com/gaearon/redux-devtools - redux logger

- Keep https://github.com/xgrommx/awesome-redux into perspective

- Figure how how https://github.com/andrewngu/sound-redux is serving mobile vs desktop

``` Run the dev tools ```

### STEP FIVE
- Bring in Phant and AWS IoT because the fuck I said so


