# Newline Linter

> **3.206 Line**<br>
> A sequence of zero or more non-\<newline\> characters plus a terminating \<newline\> character.

## Overview

_No, newline at end of file._

Lint tracked non-binary files that do not end in a newline, either locally with a Git subcommand or in CI with GitHub Actions.

## Git Subcommand

Install `git-no-newlines` in your path and run
```shell
git no-newlines
```
in a Git repository to list non-binary files that do not terminate in a newline.
Setting `EXCLUDE_PATTERN` to an extended-`grep`-compatible pattern will exclude matching files.

## GitHub Action

### Inputs

* `exclusion_pattern`
    * Optional extended-`grep`-compatible pattern of filenames to exclude.

### Example

```yml
- name: Lint newlines
  uses: fionn/newline-linter@master
  with:
    exclusion_pattern: intentionally_unterminated_file
```

See [this repository's workflow](.github/workflows/main.yml) for a more complete example.
