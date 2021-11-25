# content-formatting-linting

A series of content formatting and linting tools managed by pre-commit

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

## How to install?

To install `pre-commit` hooks locally, execute `pip install -r requirements.txt`
followed by `pre-commit --install`. This only needs to be done once per repo,
and from then on checks are made whenever committing.

## How to temporarily disable?

To bypass the `pre-commit` hook simply pass `--no-verify` when committing. The
CI will simply fail in this case.

## How to customise a linter or formatter?

Depending on the hook sometimes you need to pass in `args` into the relevant
hook in `.pre-commit-config.yaml` i.e. for [isort](https://pycqa.github.io/isort/)
to be compatible with [black](https://black.readthedocs.io) a suitable profile
must be passed in. Other hooks such as [flake8](https://flake8.pycqa.org) require
a config file i.e. `.flake8` which must be added to the repo. It would be good
if the group had an agreed standard for various different languages.

## How to extend to the checks?

To extend simply add to `.pre-commit-config.yaml` where you will need the URL
of the hook you want and a version to pin. The hook is specified with the `id`
tag and sometimes optional `args` may be passed. For more detail see the
[pre-commit](https://pre-commit.com/) documentation.
