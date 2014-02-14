##  pulling in package.json

```
  pkg: require('./package'), // read package.json

  uglify: {
    options: {
      banner: '/* <%= pkg.name %> <%= grunt.template.today("yyyy-mm-dd") %> */\n'
    },
    // ... etc
  }
```