<h2>Speed IRL</h2>

Game using realtime bus locations for the city of Los Angeles.

The movie Speed <a href="http://www.youtube.com/watch?v=aRmhneo5A48#t=1m10s">explains the concept</a>

Completely harmless web-based experiment ( HTML5, Node.js )

<h3>Install</h3>

Based on AlexeyPro's <a href="https://github.com/alexeypro/crud-bones">crud-bones</a> framework.

Install Node.JS (http://nodejs.org/#download), NPM (http://npmjs.org/) and Foreman (http://ddollar.github.com/foreman/).

Symlinks a package folder into your system, so that changes are automatically reflected, and install the "dependencies" and "devDependencies" from package.json:
$ npm link .

Run:
$ foreman start

or as simple as:
$ node src/server.js

List of all modules/libraries in use is in package.json or below:
https://github.com/LearnBoost/mongoose
https://github.com/felixge/node-mysql
https://github.com/mranney/node_redis
https://github.com/visionmedia/express
https://github.com/visionmedia/ejs
https://github.com/caolan/async
https://github.com/lorenwest/node-config
https://github.com/LearnBoost/cluster
https://github.com/flatiron/winston
https://github.com/broofa/node-uuid
https://github.com/felixge/node-dateformat
https://github.com/visionmedia/expresso
https://github.com/dannycoates/node-inspector
https://github.com/mhevery/jasmine-node

For simplicity sake I'll describe the process of getting it on Heroku:
https://devcenter.heroku.com/articles/nodejs

$ heroku create crud-bones-dev --stack cedar --remote heroku-dev
$ git push heroku-dev master
$ heroku config:add NODE_ENV=staging --app crud-bones-dev

Or if you want to push to existing Heroku instance:

$ git init 
$ git add .
$ git commit -m 'bundle for heroku-dev deploy'
$ git remote add heroku-dev git@heroku.com:crud-bones-dev.git
$ heroku config:add NODE_ENV=staging --app crud-bones-dev
$ git push -f heroku-dev master

* dotCloud:

$ dot create crudbonesdev
$ dot push crudbonesdev .

Unfortunately at this moment it doesn't seem to be supporting newer Node.JS

* Engine Yard 

N/A (in progress :-)
