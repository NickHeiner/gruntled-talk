##  config templating

```js
jshint: {
    src: {
        files: ['scripts/**/*.js']
    }
},

concat: {
    src: {
        // DRY out your code with templates!
        files: '<%= jshint.src.files %>'
    }
}
```
