##  configuring from the CLI

```
grunt.registerMultiTask('deploy_static_assets', function() {

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

    'deploy_static_assets': {
        dev: {
            options: {
                bucket: grunt.option('bucket')
            }
        }
    }

});
```

```
$ grunt deploy_static_assets:dev --bucket "qa.opower.com"
```
