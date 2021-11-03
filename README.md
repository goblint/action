# Goblint for GitHub Actions

GitHub action for analyzing C code using [Goblint](https://github.com/goblint/analyzer).
Directly based on its [Docker image](https://github.com/goblint/analyzer/pkgs/container/analyzer).

## Usage

```yml
jobs:
  goblint:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - uses: goblint/action@master
        with:
          file: 01-simple_rc.c
      - uses: github/codeql-action/upload-sarif@v1
        with:
          sarif_file: goblint.sarif
```
