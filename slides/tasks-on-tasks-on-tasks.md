##  tasks on tasks on tasks

```
grunt.registerMultiTask('deploy', function() {

    if (!grunt.option('skip-tests')) {
        grunt.task.run('test');
    }

    if (grunt.option('minify')) {
        grunt.task.run('uglify');
    }

    grunt.task.run('deploy-static-assets');

});
```
