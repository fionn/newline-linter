# Newline Linter

> **3.206 Line**<br>
> A sequence of zero or more non-\<newline\> characters plus a terminating \<newline\> character.

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

## Git Subcommand

Install `git-no-newline` in your path and run
```shell
git no-newline
```
in a Git repository to list non-binary files that do not terminate in a newline.
