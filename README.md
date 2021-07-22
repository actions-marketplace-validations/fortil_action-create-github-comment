# Create a github comment
Create a github comment

example:
```yml
name: Testing PR

on:
  pull_request:
    types: [opened, synchronize]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: fortil/action-create-github-comment@v1
        with:
          TOKEN_GITHUB: ${{secrets.TOKEN}}
          TENOR_TOKEN: ${{secrets.TENOR}}
          COMMENT: 'Is a test comment'
```
