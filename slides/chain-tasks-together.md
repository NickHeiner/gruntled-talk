##  chain tasks together

```js
grunt.registerTask('test', 'verify that the code is sound', [
    'jshint',                   // static analysis
    'karma:unit',               // run unit tests via karma
    'launch-protractor-server', // launch a server for ptor tests to hit
    'protractor'                // run protractor tests
]);

grunt.registerTask('publish', 'test and publish to npm', [
    'test',         // be sure that we only publish good code
    'build',        // uglify, concat, whatever you need to do
    'shell:publish' // run `npm publish`
]);
```

