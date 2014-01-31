##  gruntfile

```coffee
module.exports = (grunt) ->

    grunt.loadNpmTasks('grunt-contrib-jshint');

    grunt.initConfig
        jshint:
            options:
                angular: true

            scripts:
                files: ['js/**/*.js']

            test:
                files: ['test/**/*.js']
```

```
$ grunt jshint:scripts
Running "jshint:scripts" (jshint) task
>> 10 files lint free.

Done, without errors.
```

```
$ grunt jshint:test
Running "jshint:test" (jshint) task
>> 3 files lint free.

Done, without errors.
```