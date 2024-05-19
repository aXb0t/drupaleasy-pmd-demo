# drupaleasy-pmd-demo

## Github Personal Access Token
Rename `github.key.example` to `github.key` and add your Github Personal Access Token information.

## Basic Set Up

1. Install the following modules:
  - DrupalEasy Repositories

2. Create test user account

3. Give the test user account the following permissions:

  - Repository: Create new content
  - Repository: Edit own content
  - Repository: Delete own content

### Custom Module Location

The custom module is located in the project root `modules/` directory. It is symlinked to the `web/modules/custom/` to allow Composer to manage the custom module as a dependency.

## Run code quality checks and tests

Run PHP Code Sniffer, a convenience command is available in DDEV:
```
ddev sniff
```

Run PHPStan with DDEV, passing along a level:
```
ddev stan 3
```

Assume the following tests are run from inside the container (`ddev ssh`):

Run code quality checks:
```
phpstan analyze --level 5 web/modules/custom/drupaleasy_repositories
```

Run all the tests:
```
phpunit web/modules/custom/drupaleasy_repositories/tests/
```

Run a the Unit tests:
```
phpunit web/modules/custom/drupaleasy_repositories/tests/src/Unit/
```

