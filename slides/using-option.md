##  configuring from the CLI

```
grunt.registerMultiTask('deploy-static-assets', function() {

    var done = grunt.task.current.async();
    var opts = grunt.task.current.options({
        bucket: 'dev.opower.com'
    });

    s3.push(opts.bucket).then(done, function err(reason) {
        done(util.isError(reason) ? reason : new Error(reason));
    });
});
```

```
grunt.initConfig({

    'deploy-static-assets': {
        dev: {
            bucket: grunt.option('bucket')
        }
    }

});
```

```
$ grunt deploy-static-assets:dev --bucket "qa.opower.com"
```
