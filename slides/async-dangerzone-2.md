##  async dangerzone

```
grunt.registerMultiTask('deploy-static-assets', function() {
    var done = grunt.task.current.async();
    s3.push('dev.opower.com')
        .then(done, function onErr(reason) {
            // oops - calling done() with a value that is not an Error or false
            done('task failed');
        });
});
```

```
$ g exp
Running "exp" task

Done, without errors
```

![lies](images/lies.png)


