##  register a multitask

```
grunt.registerMultiTask(

    'verify-file-exists',                   // task title

    'Verify that specified files exists',   // optional task description

    function() {                            // the task itself

        var file = grunt.task.current.options();

        if (!grunt.file.exists(file)) {
            grunt.fail.fatal('Could not find ' + file);
            return;
        }

        grunt.log.ok(file + ' exists ;)')
    }
);
```
