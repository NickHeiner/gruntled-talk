##  non-task config

Config doesn't need to be task-specific

```
directories: {
    demo: 'dist'
},

// some made-up build task
build: {
    local: {
        src: 'scripts/**/*.js',
        dest: '<%= directories.demo %>'
    }
}
```
