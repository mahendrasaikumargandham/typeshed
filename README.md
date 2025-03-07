# typeshed

[![Build status](https://github.com/python/typeshed/workflows/Check%20stubs/badge.svg)](https://github.com/python/typeshed/actions?query=workflow%3A%22Check+stubs%22)
[![Chat at https://gitter.im/python/typing](https://badges.gitter.im/python/typing.svg)](https://gitter.im/python/typing?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Pull Requests Welcome](https://img.shields.io/badge/pull%20requests-welcome-brightgreen.svg)](https://github.com/python/typeshed/blob/master/CONTRIBUTING.md)

<h2>About</h2>

Typeshed contains external type annotations for the Python standard library
and Python builtins, as well as third party packages as contributed by
people external to those projects.

This data can e.g. be used for static analysis, type checking or type inference.

For information on how to use `typeshed`, read below.  Information for
contributors can be found in [CONTRIBUTING.md](CONTRIBUTING.md).  **Please read
it before submitting pull requests; do not report issues with annotations to
the project the stubs are for, but instead report them here to typeshed.**

Typeshed supports Python versions 2.7 and 3.6 and up.

## Using

If you're just using mypy (or pytype or PyCharm), as opposed to
developing it, you don't need to interact with the typeshed repo at
all: a copy of standard library part of typeshed is bundled with mypy.
And type stubs for third party packages and modules you are using can
be installed from PyPI. For example, if you are using `six` and `requests`,
you can install the type stubs using

    $ pip install types-six types-requests

These PyPI packages follow [PEP 561](http://www.python.org/dev/peps/pep-0561/)
and are automatically released (multiple times a day, when needed) by
[typeshed internal machinery](https://github.com/typeshed-internal/stub_uploader).

Type checkers should be able to use these stub packages when installed. For more
details, see the documentation for your type checker.

### The `_typeshed` package

typeshed includes a package `_typeshed` as part of the standard library.
This package and its submodules contains utility types, but is not
available at runtime. For more information about how to use this package,
[see the `stdlib/_typeshed` directory](https://github.com/python/typeshed/tree/master/stdlib/_typeshed).

## Discussion

If you've run into behavior in the type checker that suggests the type
stubs for a given library are incorrect or incomplete,
we want to hear from you!

Our main forum for discussion is the project's [GitHub issue
tracker](https://github.com/python/typeshed/issues).  This is the right
place to start a discussion of any of the above or most any other
topic concerning the project.

If you have general questions about typing with Python, or you need
a review of your type annotations or stubs outside of typeshed, head over to
[our discussion forum](https://github.com/python/typing/discussions).
For less formal discussion, try the typing chat room on
[gitter.im](https://gitter.im/python/typing).  Some typeshed maintainers
are almost always present; feel free to find us there and we're happy
to chat.  Substantive technical discussion will be directed to the
issue tracker.
