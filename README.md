# grunt-screeps-customserver

> A Grunt plugin for committing code to your [Screeps](https://screeps.com) account.
>
>
> This is a fork of the original [grunt-screeps](https://github.com/cbgbt/grunt-screeps) in order to provide configuration options for pushing to a private server.
>
> Note: The screeps server must support the [screepsmod-auth](https://github.com/ScreepsMods/screepsmod-auth) mod.

## Getting Started
If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-screeps-customserver
```

### Usage Example

**Gruntfile.js:**
```js
module.exports = function(grunt) {

    grunt.loadNpmTasks('grunt-screeps');

    grunt.initConfig({
        screeps: {
            options: {
                hostname: 'SCREEPS_SERVER_IP_OR_HOSTNAME',
                port: 'SCREEPS_SERVER_PORT',
                'use-https': false,
                username: 'YOUR_USERNAME_OR_EMAIL_IF_ON_SCREEPS_DOT_COM',
                password: 'YOUR_PASSWORD',
                branch: 'default',
                ptr: false
            },
            dist: {
                src: ['dist/*.js']
            }
        }
    });
}
```

Now you can run this command to commit your code from `dist` folder to your Screeps account:
```
grunt screeps
```
