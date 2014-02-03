##  npm test = grunt test

Gruntfile.js
```
grunt.registerTask('test', ['lint', 'unit', 'e2e']);
```

package.json
```
"scripts": {
    "test": "grunt test"
}
```

```
$ npm test

> gruntled@0.1.0 test /Users/nick.heiner/public-projects/gruntled-talk
> grunt test

Running "coffeelint:all" (coffeelint) task
>> 1 file lint free.

Running "jshint:all" (jshint) task
>> 1 file lint free.

Done, without errors.
```

