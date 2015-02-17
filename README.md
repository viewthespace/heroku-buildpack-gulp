Heroku Buildpack for gulp.js
========================================

Usage
-----

- Set your Heroku app's buildpack URL to heroku-buildpack-multi
`heroku config:add BUILDPACK_URL=https://github.com/heroku/heroku-buildpack-multi.git`
- Create a .buildpacks file
`
https://github.com/heroku/heroku-buildpack-nodejs
https://github.com/rjmackay/heroku-buildpack-gulp
`
- Run `heroku labs:enable buildpack-env-arg` to enable environment variable support
- Run `heroku config:set NODE_ENV=production` to set your environment to `production` (or any other name)
- Add a Gulp task called `heroku:production` that builds your app
- Serve your app as usual

Credits
-------
Forked from [heroku-buildpack-nodejs-gulp](https://github.com/heroku/heroku-buildpack-nodejs-gulp).
