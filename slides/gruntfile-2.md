##  gruntfile.js

```
$ npm install --save-dev grunt-contrib-jshint
```

```coffee
module.exports = (grunt) ->

    grunt.loadNpmTasks 'grunt-contrib-jshint'

    grunt.initConfig
        jshint:
            options:
                globals:
                    angular: true
            files: ['scripts/**/*.js']
```

```sh
$ grunt jshint
Running "jshint:files" (jshint) task
>> 10 files lint free.

Done, without errors.
```
