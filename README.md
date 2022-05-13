[![PyPI status](https://img.shields.io/pypi/status/kiara_plugin.documentation.svg)](https://pypi.python.org/pypi/kiara_plugin.documentation/)
[![PyPI version](https://img.shields.io/pypi/v/kiara_plugin.documentation.svg)](https://pypi.python.org/pypi/kiara_plugin.documentation/)
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/kiara_plugin.documentation.svg)](https://pypi.python.org/pypi/kiara_plugin.documentation/)
[![Build Status](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2FDHARPA-Project%2Fkiara%2Fbadge%3Fref%3Ddevelop&style=flat)](https://actions-badge.atrox.dev/DHARPA-Project/kiara_plugin.documentation/goto?ref=develop)
[![Coverage Status](https://coveralls.io/repos/github/DHARPA-Project/kiara_plugin.documentation/badge.svg?branch=develop)](https://coveralls.io/github/DHARPA-Project/kiara_plugin.documentation?branch=develop)
[![Code style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

# [**kiara**](https://dharpa.org/kiara.documentation) plugin: (documentation)

Kiara user documentation.

 - Documentation: [https://DHARPA-Project.github.io/kiara_plugin.documentation](https://DHARPA-Project.github.io/kiara_plugin.documentation)
 - Code: [https://github.com/DHARPA-Project/kiara_plugin.documentation](https://github.com/DHARPA-Project/kiara_plugin.documentation)
 - `kiara`: [https://dharpa.org/kiara.documentation](https://dharpa.org/kiara.documentation)

## Description

TODO

## Development

### Requirements

- Python (version >= 3.8)
- conda
- git


### Prepare development environment

### Using conda (recommended)

```
conda create -n documentation python=3.9
conda activate documentation
conda install -c conda-forge mamba   # this is optional, but makes everything install related much faster, if you don't use it, replace 'mamba' with 'conda' below
mamba install -c conda-forge -c dharpa kiara
mamba install -c conda-forge -c dharpa kiara_plugin.core_types kiara_plugin.tabular   # optional, adjust which plugin packages you depend on, those two are quite common
```

## Check out the source code

First, fork the [kiara.documentation](https://github.com/DHARPA-Project/kiara.documentation) repository into your personal Github account.

Then, use the resulting url (in my case: https://github.com/makkus/kiara.documentation.git) to clone the repository locally:

```
https://github.com/<YOUR_FORKED_GITHUB_ID>/kiara.documentation
```

## Install the kiara documentation package into it

```
cd kiara.documentation
pip install -e '.[all_dev]'
```

#### Try it out

After this is done, you can start the development 'serve' mode:

```console
kiara doc serve
...
...
```

This will create the documentation, and run a webserver on http://localhost:8000 where you can preview the generated documentation site.
The first startup will take a bit, because some of the pages use dynamically generated results to prevent the documentation becoming
out-of-date easily (and as a test against regressions). Those results are cached though, so the 2nd time around startup should be quicker.

The 'serve' command will watch documents under `docs`, if any of them is changed, it will auto-create the changed documentation page,
and reload the browser(s) that are viewing it.

### ``make`` targets (Linux & Mac OS X)

- ``init``: init development project (install project & dev dependencies into virtualenv, as well as pre-commit git hook)
- ``update-dependencies``: update development dependencies (mainly the core ``kiara`` package from git)
- ``flake``: run *flake8* tests
- ``mypy``: run mypy tests
- ``test``: run unit tests
- ``docs``: create static documentation pages (under ``build/site``)
- ``serve-docs``: serve documentation pages (incl. auto-reload) for getting direct feedback when working on documentation
- ``clean``: clean build directories

For details (and other, minor targets), check the ``Makefile``.


### Running tests

``` console
> make test
# or
> make coverage
```


## Copyright & license

This project is MPL v2.0 licensed, for the license text please check the [LICENSE](/LICENSE) file in this repository.
