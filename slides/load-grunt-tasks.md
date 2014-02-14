##  load-grunt-tasks

Use [@sindresorhus](https://github.com/sindresorhus)'s excellent [load-grunt-tasks](https://github.com/sindresorhus/load-grunt-tasks) library.

Before:

```
grunt.loadNpmTasks('grunt-contrib-jshint');
grunt.loadNpmTasks('grunt-mochatest');
grunt.loadNpmTasks('grunt-doge-script');
grunt.loadNpmTasks('grunt-s3');
grunt.loadNpmTasks('grunt-contrib-copy');
grunt.loadNpmTasks('grunt-coffeelint');
grunt.loadNpmTasks('grunt-my-task');
grunt.loadNpmTasks('grunt-bitcoin-miner');
grunt.loadNpmTasks('grunt-dogecoin-miner');
grunt.loadNpmTasks('grunt-available-tasks');
```

After:

```
require('load-grunt-tasks')(grunt)
```


