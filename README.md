# jr-rauxa-gh
### Github Username Search by Jeff Roth
See [Heroku App](https://jr-rauxa-gh.herokuapp.com/).

## Briefing

Project created with vue-cli

Github API requests made with Axios

Tested with Mocha + Chai + Sinon

Hosted on Heroku + Express server

Heroko Pipeline: Local Branch > Master Branch > Github Notification & Approval > Heroku deployment to Staging App.


## Frontend

As per request, the chosen Frontend framework was Vue.js. I had no previous experience with Vue.js but I studied the documentation and used my experience with other frameworks to complete the requested project.

App was generated from the vue-cli command.

Home.vue adapted to be the Home page for the challenge with a functional answer for the challenge.

Router created for About Page.

Home page renders an input field to enter the username to be requested by Github API. 

If no username is given, a message saying the field id required will appear below the field.

If a username is given, Axios will request it on the API. 

If is there a match, the app will render the user's avatar image, the number of followers and their avatar images. In case the number of followers is higher than 100, a button to load more results will show.

If the username has no followers, it won't render the followers list.

Any empty, zero or null field won't be shown (Bio, Location, Number of Followers, Number of Following).



## Backend

In order to host the app to Heroku, a Express server was created.



## Tests

Mocha + Chai + Sinon

See [Unit Tests](https://github.com/jeffersonroth/jr-rauxa-gh/tree/master/tests/unit).



## Problem

### Description

Create a service that allows for a user to search for a GitHub username. On a successful search return, display the user's GitHub handle, follower count, and a list of the user's followers (just the avatar is fine). Since some users (e.g. mrdoob, holman, etc.) have many thousands of followers, GitHub only returns a portion of the followers with each request. Create a "load more" button that, when clicked, fetches the next payload of followers. This button should persist until there are no more pages of followers to fetch.

### Challenges

Calling the Github API to retrieve username info was no challenge. The point here was to adapt how to render it to the browser. Vue.js documentation is clear and the generated example by vue-cli gave a clear path to follow. The next step was to adapt the Vue components to work with the data and Vuetify to give it order and design.

### Solution

I'm really used to use Axios for API calls. Happily, it integrates well with Vue.js. All scenarios were taken into account (no username is given, matching and non-existing usernames) so the template could work with the data. v-if's and v-for's were enough to present all the data I wanted to present in the browser.


## Future - If I were to continue with the project, I would:

- Present similar results for non-matching usernames;
- A way to export the followers' list (it seems to be important here) and their information (bio, username, id, login, followers, etc);
- No only present the avatar images, but the images would redirect to the user's profile;
- For a match, show the followers in common with me;
- More actions: follow, see repos, etc.


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Run your unit tests
```
npm run test:unit
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
