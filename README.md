# template

This is a Carp [template repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).
You should be able to reuse its structure for your projects!

## Overview

This template comes with a simple entrypoint called `main.carp`. This is the
file that people will load when they first load your project. It doesn’t
currently compile—can you find out why?

We also have some tests. They reside in `test/tests.carp`. If we run them using
`carp -x test/tests.carp`, they fail! Please write some useful tests for your
awesome library!

Finally, we can generate documentation. The script `gendocs.carp` (you can
invoke it by calling `carp gendocs.carp`) will generate documentation from the
docstrings of your functions and modules, and put it in the `docs/` directory.
You can style and customize it by editing the CSS or fiddling with the
configuration options in `gendocs.carp`. They should be pretty
self-explanatory.

<hr/>

Have fun!
