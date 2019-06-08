
<!-- README.md is generated from README.Rmd. Please edit that file -->

# pre-commit-hooks

<!-- badges: start -->

<!-- badges: end -->

A collection of git pre-commit hooks to use with pre-commit.com.
Currently, we have:

  - `styler-style-files`: A hook to style files with
    [styler](https://styler.r-lib.org)
  - `devtools-document`: A hook to run `devtools::document()`.
  - `usethis-use-tidy-description`: A hoock to run
    `usethis::use_tidy_description()` to make sure you only commit key
    values ordered (alphabetically) in your DESCRIPTION file.

To add a pre-commit hook to your project, install pre-commit as
described in the [official documentation](https://pre-commit.com/#intro)
and make sure the executable `pre-commit` is in a place that is on your
`$PATH`.

If you installed pre-commit, you can add it to a specific project by
adding a `.pre-commit-config.yaml` file that has a structure like this:

``` yaml
-   repo: https://github.com/lorenzwalthert/pre-commit-hooks
    rev: latest
    hooks: 
    -   id: devtools-document
    -   id: styler-style-files
    -   id: usethis-use-tidy-description
```

Then, run `pre-commit install` in your repo and you are done. The next
time you run `$ git commit`, the hooks listed in your
`.pre-commit-config.yaml` will get exeuted before the commit. The
revision `latest` refers to HEAD of master.