## Configure your task

```
grunt.initConfig

    'verify-package-json-exists':
        pkg:
            options:
               file: 'package.json'

        bower:
           options:
               file: 'bower.json'

        travis:
            options:
               file: '.travis.yml'
```