##  register a task

```
grunt.registerTask(

    'verify-file-exists',                    // task title

    'Verify that a file still exists',       // optional task description

    function() {                             // the task itself

        var file = grunt.config('verify-file-exists');

        if (!grunt.file.exists(file)) {
            grunt.fail.fatal('Could not find ' + file);
            return;
        }

        grunt.log.ok(file + ' exists ;)')
    }

);
```
