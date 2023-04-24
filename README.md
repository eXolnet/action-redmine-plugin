# Redmine Plugin Action

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Build Status](https://img.shields.io/github/actions/workflow/status/eXolnet/action-redmine-plugin/tests.yml?label=tests&style=flat-square)](https://github.com/eXolnet/action-redmine-plugin/actions?query=workflow%3Atests)

Action to test a Redmine plugin using various versions of Redmine.

## Usage

```yaml
name: Redmin plugin

on: [ push ]

jobs:
  
  test:
    name: Test Redmine Plugin
    runs-on: ubuntu-latest
    
    steps:
      - uses: eXolnet/action-redmine-plugin@v1
        with:
          plugin_name: redmine_plugin
          redmine_version: 5.0
          ruby_version: 2.4
          database: mysql
```

## Security

If you discover any security related issues, please email security@exolnet.com instead of using the issue tracker.

## Credits

- [Alexandre D’Eschambeault](https://github.com/xel1045)
- [All Contributors](../../contributors)
