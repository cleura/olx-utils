This repository was previously hosted under the `hastexo` GitHub organization, and moved to `cleura` in December 2025 as part of a routine repository consolidation.

# OLX Utilities

A set of tools to facilitate courseware development using the [Open Learning XML](http://edx.readthedocs.io/projects/edx-open-learning-xml/en/latest/) (OLX) format.

OLX is sometimes tediously repetitive, and this package enables courseware authors to apply the [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) principle when writing OLX content.
It allows you to create templates (using [Mako](http://www.makotemplates.org/)), which in turn enable you to

- define OLX fragments only once, to reuse them as often as you want (this comes in very handy in using the [stackamole XBlock](https://github.com/cleura/stackamole-xblock)),
- write courseware content in [Markdown](https://en.wikipedia.org/wiki/Markdown),
- do anything else you would like to do using your own plugins.

## Install

Install the `olx-utils` package from PyPI:

```bash
pip install olx-utils
```

## Apply templates to a course

In order to create a new course run named `newrun`, starting on May 1, 2026 and ending on October 31, 2027, change into your courseware checkout and run:

```bash
olx new-run -b newrun 2026-05-01 2027-10-31
```

The `-b` option causes your rendered OLX to be added to a new Git branch named `run/newrun`, which you can then import into your Open edX content store.

You can also invoke `olx new-run` as `new_run.py`.
However, this is deprecated and its use is discouraged.
`new_run.py` will go away in a future release.

## License

This package is licensed under the [GNU Affero GPL](https://tldrlegal.com/l/agpl3); see [LICENSE](https://www.gnu.org/licenses/agpl-3.0.txt) for details.
