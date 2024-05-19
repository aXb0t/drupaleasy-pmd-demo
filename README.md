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

## Run code quality checks and tests

Run PHP Code Sniffer, a convenience command is available in DDEV:
```
ddev sniff
```

Assume the following tests are run from inside the container.
```
ddev ssh
```

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

