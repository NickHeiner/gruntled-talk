##  use valid identifiers for task names

Bad:
```
'deploy-static-assets': 
  'dev-or-qa':
    options:
      bucket: 'dev.opower.com'

'verify-static-assets': 
  'dev-or-qa':
    options:
      bucket: '<%= grunt.config(["deploy-static-assets", "dev-or-qa"]).options.bucket %>'
```

Good:
```
'deploy_static_assets': 
  'dev_or_qa':
    options:
      bucket: 'dev.opower.com'

'verify_static_assets': 
  'dev_or_qa':
    options:
      bucket: '<%= deploy_static_assets.dev_or_qa.options.bucket %>'
```
