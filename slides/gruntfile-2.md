##  gruntfile.js

```
$ npm install --save-dev grunt-contrib-jshint
```

```coffee
module.exports = (grunt) ->

    grunt.loadNpmTasks('grunt-contrib-jshint');

    grunt.initConfig
        jshint:
            scripts:
                options:
                    angular: true
                files: ['js/**/*.js']
```

```
$ grunt jshint
Running "jshint:scripts" (jshint) task
>> 10 files lint free.

Done, without errors.
```
