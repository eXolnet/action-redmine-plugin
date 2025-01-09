# Redmine Plugin Action

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Build Status](https://img.shields.io/github/actions/workflow/status/eXolnet/action-redmine-plugin/tests.yml?label=tests&style=flat-square)](https://github.com/eXolnet/action-redmine-plugin/actions?query=workflow%3Atests)

GitHub action to test a Redmine plugin using various versions of Redmine.

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
          # Automatically checkout the plugin.
          # If false, the plugin must be manually checkout.
          #
          # Default: true
          checkout: false

          # Folder where the plugin will be installed.
          #
          # Default: null
          plugin_name: redmine_plugin
          
          # Redmine version to use.
          #
          # Default: null
          redmine_version: 5.0
          
          # Ruby version to use.
          #
          # Default: null
          ruby_version: 2.4
          
          # Database driver to use.
          #
          # Default: sqlite
          database: mysql
```

## Security

If you discover any security related issues, please email security@exolnet.com instead of using the issue tracker.

## Credits

- [Alexandre D’Eschambeault](https://github.com/xel1045)
- [All Contributors](../../contributors)

## License

Copyright © [eXolnet](https://www.exolnet.com). All rights reserved.

This code is licensed under the [MIT license](http://choosealicense.com/licenses/mit/).
Please see the [license file](LICENSE) for more information.
