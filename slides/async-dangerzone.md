##  async dangerzone

```
grunt.registerMultiTask('deploy-static-assets', function() {

    var done = grunt.task.current.async();

    s3.push('dev.opower.com');

    // oops - forgot to ever call done()
});
```

```
$ g exp
Running "exp" task
$
```


