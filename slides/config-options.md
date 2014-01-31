##  config options

```
jshint:
    options:               # default options for all targets
        node: true

    grunt: 'Gruntfile.js', # accept the defaults as-is

    test:
        options:           # extend the defaults
            force: true
        files: 'test/**/*.js',

    src:
        options:           # override and extend the defaults
            node: false,
            reporter: 'checkstyle'
        files: 'scripts/**/*.js'
```
