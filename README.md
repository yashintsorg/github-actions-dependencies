## Dependency management in GitHub Actions

You can use the `needs` keyword to make sure a job only starts when another job has completed successfully.

```yaml
jobs:
  setup:
    runs-on: ubuntu-latest
    steps:
      - run: |
        echo 'Setup completed'

  build:
    needs: setup
    runs-on: ubuntu-latest
    steps:
      - run: |
        echo 'Build is now safe to run'
```
