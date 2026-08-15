# template

This is a Carp [template repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).
You should be able to reuse its structure for your projects!

## Overview

The module lives in `my-mod.carp`, named after the `MyMod` module it holds.
That is the convention the carpentry-org packages follow, so **rename both the
file and the module** for your own library. Four places refer to the name and
need to change with it:

- `test/my-mod.carp`, which loads it
- `gendocs.carp`, which loads it and sets the docs title
- `.github/workflows/ci.yml`, which runs the test file
- the module's own doc string in `my-mod.carp`

`my-mod.carp` also shows the two definition forms you will use most: `defn`
for public functions, each with a `doc` string, and `defn-` for helpers that
should stay inside the module and out of the generated docs.

## Tests

Tests live in `test/my-mod.carp` and run with `carp -x test/my-mod.carp`. The
two that ship here pass, so a red suite means you broke something. Replace
them with tests for your own library.

## Documentation

`carp -x gendocs.carp` generates documentation from the doc strings of your
functions and modules and writes it to `docs/`. Style it by editing the CSS or
the configuration options in `gendocs.carp`, which should be pretty
self-explanatory. Set `docs-url` to your repository, and note that `title`
also names the generated index page. A single-module project does not need
that index at all; uncomment `docs-generate-index` once yours is one.

## CI

The workflow runs the tests, then lints with
[angler](https://github.com/carpentry-org/angler) and checks formatting with
[carp-fmt](https://github.com/carpentry-org/carp-fmt), then generates the
docs. Run `carp-fmt --check` and `angler` locally before pushing to keep it
green.

<hr/>

Have fun!
