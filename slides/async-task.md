##  async tasks

```
var s3 = require('s3');
var util = require('util');

grunt.registerMultiTask('deploy_static_assets', function() {

    // tell grunt this may take a while
    var done = grunt.task.current.async();

    s3.push('dev.opower.com').then(function success() {
        // To indicate success, call done() with no arguments.
        done();
    }, function err(reason) {
        // To indicate failure, pass an Error to done.
        var reasonAsErr = util.isError(reason) ? reason : new Error(reason);
        done(reasonAsErr);
    });
});
```
