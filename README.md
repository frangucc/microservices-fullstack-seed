# microservices-fullstack-seed

## project goals

### STEP ONE - ECS CONTAINERS, NO OPS & CONTINUOUS DELIVERY (12Factor stuff)
- Use docker to establish a GO continuous delivery server based on Thoughtworks https://github.com/gocd/gocd-docker or better, decide on whether or not to use CircleCI or Codeship, choose one

- Toss in a two servers and default to GO. Have Node in there just because we may use it later. Be sure they're on socket.io or better if even necessary with GO
- Have one server send some JSON but through the docker container. Make the application server and the database server seperate.


### STEP TWO - CODEBASE via YO, Redux/React
- Implement redux with the following tree structure: actions, components, constants, containers, reducers and store_enhancers (make strong argument for any others (ie. routes)): must use yeoman generators to build project folder structure as my front-end is opinionated. If you prefer another, you may choose from these following options: yo x, yo y, yo z (as long as your starter builds on the containers services, you're good)

-- install redux-scaffold, redux-devtools, redux-log	

``` code comments go here ```

- Use npm start, gulp and/or webpack with support for ES6, lint, babel and hotloader

### STEP THREE - MAKE AN APP
- Recreate and enahnce the http://search.dronestre.am/ search UI by injesting the http://api.dronestre.am/data feed. Use material-ui react components to render my much sexier looking view.

- Reverse engineer the sound-redux app because that's what a real hacker would do

--- Consider https://github.com/ipselon/material-ui-prepack on the UI
--- Use the scaffolding tool 

- Demonstrate a reducer on the http://api.dronestre.am/data service

- Create a custom react component from a random, older javascript library such as numbers.js or tangle.js to crunch the dronestrike data

- Create a three.js or d3.js visualization component to visualize the drone strike data

### STEP FOUR
- Write a mocha/chai test to test the action, reducer and a componenet responsible for the search and it's results

https://github.com/gaearon/redux-devtools - redux logger

- Keep https://github.com/xgrommx/awesome-redux into perspective

- Figure how how https://github.com/andrewngu/sound-redux is serving mobile vs desktop



