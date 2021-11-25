# content-formatting-linting

A series of content formatting and linting tools managed by pre-commit

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

## Installation

To install `pre-commit` hooks locally, execute `pip install -r requirements.txt`
followed by `pre-commit --install`. This only needs to be done once per repo,
and from then on checks are made whenever committing.

## Disable

To bypass the `pre-commit` hook simply pass `--no-verify` when committing. The
CI will simply fail in this case.
