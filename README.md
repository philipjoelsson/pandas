<div align="center">
  <img src="https://pandas.pydata.org/static/img/pandas.svg"><br>
</div>

-----------------

# Report for assignment 4

This is a template for your report. You are free to modify it as needed.
It is not required to use markdown for your report either, but the report
has to be delivered in a standard, cross-platform format.

## Project

Name: pandas-dev/pandas

URL: https://github.com/pandas-dev/pandas

#### One or two sentences describing it
pandas is a Python package that provides fast, flexible, and expressive data structures designed to make working with "relational" or "labeled" data both easy and intuitive. It aims to be the fundamental high-level building block for doing practical, real world data analysis in Python.

## Onboarding experience

#### Did you choose a new project or continue on the previous one?

We chose a new project. In Assignment 3 we had a project with Algorithms, hence we
hade to choose a new one for this assignment.

#### If you changed the project, how did your experience differ from before?

Much more difficult to build and get an understanding of how to run all tests.
The installation process was not perfect either, with a few of us struggling.
Also more difficult to get an understanding of the program as a whole. 

## Effort spent

For each team member, how much time was spent in

1. plenary discussions/meetings;

2. discussions within parts of the group;

3. reading documentation;

4. configuration and setup;

5. analyzing code/output;

6. writing documentation;

7. writing code;

8. running code?

For setting up tools and libraries (step 4), enumerate all dependencies
you took care of and where you spent your time, if that time exceeds
30 minutes.

## Overview of issue(s) and work done.

Title:

URL:

Summary in one or two sentences

Scope (functionality and code affected).

## Requirements for the new feature or requirements affected by functionality being refactored

### Issue resolution
#### Identify requirements related to the issue. If the requirements are not documented yet, try to describe them based on code reviews and existing test cases. Create a project plan for testing these requirements, and working on the issue.

There are no documented requirements for this issue. In the issue there is documented expected behaviour, which works as
requirement and guide for understanding what the program should do. From looking at other parts of the code, you get an understanding for the expected behaviour. There are existing tests that are marked as xfail, meaning they are expected to fail. When xfail assertion is removed the tests fail. The plan is to fix the issue and then remove the xfail markings and confirm that the tests then pass. Since there already are tests
for this issue and the tests existing are sufficient, there is no need for further adding new tests.

Optional (point 3): trace tests to requirements.

## Code changes

### Patch


```
git diff main..refactor1
```

#### Optional (point 4): the patch is clean.
Yes, the patch is clean. There is no debug output and all code that was no longer neccesary was removed rather than commented out.

#### Optional (point 5): considered for acceptance (passes all automated checks).

## Test results

#### Overall results with link to a copy or excerpt of the logs (before/after refactoring).

Only the testfile referenced in issue was tested. Testing the whole test-suite did not work, as there are to
many test-cases. Approximately 500000 tests in total in the whole test-suite.

Before issue was resolved:
104 failed, 416 passed, 104 skipped

After issue was resolved:
520 passed, 104 skipped

## UML class diagram and its description

<div>
  <img src='/assignment4_uml.png' width='400'/>
</div>

### Key changes/classes affected

Optional (point 1): Architectural overview.

Optional (point 2): relation to design pattern(s).

## Overall experience

#### What are your main take-aways from this project? What did you learn?

#### How did you grow as a team, using the Essence standard to evaluate yourself?
We evaluated that according to the essence checklist (p. 52), we are working on the "Performing" level. This is because we fulfill all the checklist items before "Performing" in addition to the ones directly linked to "Performing". The team identifies and adresses problem without any outside help and is effective in the sense that minimal backtracking or reworking has been neccesary. We do not consider ourselves to fulfill "Adjourned" however, as we are not yet done with everything related to the issue. Further work could be done to resolve the issue in a better way.

Optional (point 6): How would you put your work in context with best software engineering practice?

Optional (point 7): Is there something special you want to mention here?


# pandas: powerful Python data analysis toolkit
[![PyPI Latest Release](https://img.shields.io/pypi/v/pandas.svg)](https://pypi.org/project/pandas/)
[![Conda Latest Release](https://anaconda.org/conda-forge/pandas/badges/version.svg)](https://anaconda.org/anaconda/pandas/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3509134.svg)](https://doi.org/10.5281/zenodo.3509134)
[![Package Status](https://img.shields.io/pypi/status/pandas.svg)](https://pypi.org/project/pandas/)
[![License](https://img.shields.io/pypi/l/pandas.svg)](https://github.com/pandas-dev/pandas/blob/main/LICENSE)
[![Coverage](https://codecov.io/github/pandas-dev/pandas/coverage.svg?branch=main)](https://codecov.io/gh/pandas-dev/pandas)
[![Downloads](https://static.pepy.tech/personalized-badge/pandas?period=month&units=international_system&left_color=black&right_color=orange&left_text=PyPI%20downloads%20per%20month)](https://pepy.tech/project/pandas)
[![Slack](https://img.shields.io/badge/join_Slack-information-brightgreen.svg?logo=slack)](https://pandas.pydata.org/docs/dev/development/community.html?highlight=slack#community-slack)
[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Imports: isort](https://img.shields.io/badge/%20imports-isort-%231674b1?style=flat&labelColor=ef8336)](https://pycqa.github.io/isort/)

## What is it?

**pandas** is a Python package that provides fast, flexible, and expressive data
structures designed to make working with "relational" or "labeled" data both
easy and intuitive. It aims to be the fundamental high-level building block for
doing practical, **real world** data analysis in Python. Additionally, it has
the broader goal of becoming **the most powerful and flexible open source data
analysis / manipulation tool available in any language**. It is already well on
its way towards this goal.

## Main Features
Here are just a few of the things that pandas does well:

  - Easy handling of [**missing data**][missing-data] (represented as
    `NaN`, `NA`, or `NaT`) in floating point as well as non-floating point data
  - Size mutability: columns can be [**inserted and
    deleted**][insertion-deletion] from DataFrame and higher dimensional
    objects
  - Automatic and explicit [**data alignment**][alignment]: objects can
    be explicitly aligned to a set of labels, or the user can simply
    ignore the labels and let `Series`, `DataFrame`, etc. automatically
    align the data for you in computations
  - Powerful, flexible [**group by**][groupby] functionality to perform
    split-apply-combine operations on data sets, for both aggregating
    and transforming data
  - Make it [**easy to convert**][conversion] ragged,
    differently-indexed data in other Python and NumPy data structures
    into DataFrame objects
  - Intelligent label-based [**slicing**][slicing], [**fancy
    indexing**][fancy-indexing], and [**subsetting**][subsetting] of
    large data sets
  - Intuitive [**merging**][merging] and [**joining**][joining] data
    sets
  - Flexible [**reshaping**][reshape] and [**pivoting**][pivot-table] of
    data sets
  - [**Hierarchical**][mi] labeling of axes (possible to have multiple
    labels per tick)
  - Robust IO tools for loading data from [**flat files**][flat-files]
    (CSV and delimited), [**Excel files**][excel], [**databases**][db],
    and saving/loading data from the ultrafast [**HDF5 format**][hdfstore]
  - [**Time series**][timeseries]-specific functionality: date range
    generation and frequency conversion, moving window statistics,
    date shifting and lagging


   [missing-data]: https://pandas.pydata.org/pandas-docs/stable/user_guide/missing_data.html
   [insertion-deletion]: https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#column-selection-addition-deletion
   [alignment]: https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html?highlight=alignment#intro-to-data-structures
   [groupby]: https://pandas.pydata.org/pandas-docs/stable/user_guide/groupby.html#group-by-split-apply-combine
   [conversion]: https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#dataframe
   [slicing]: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#slicing-ranges
   [fancy-indexing]: https://pandas.pydata.org/pandas-docs/stable/user_guide/advanced.html#advanced
   [subsetting]: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#boolean-indexing
   [merging]: https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html#database-style-dataframe-or-named-series-joining-merging
   [joining]: https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html#joining-on-index
   [reshape]: https://pandas.pydata.org/pandas-docs/stable/user_guide/reshaping.html
   [pivot-table]: https://pandas.pydata.org/pandas-docs/stable/user_guide/reshaping.html
   [mi]: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#hierarchical-indexing-multiindex
   [flat-files]: https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#csv-text-files
   [excel]: https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#excel-files
   [db]: https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#sql-queries
   [hdfstore]: https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#hdf5-pytables
   [timeseries]: https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#time-series-date-functionality

## Where to get it
The source code is currently hosted on GitHub at:
https://github.com/pandas-dev/pandas

Binary installers for the latest released version are available at the [Python
Package Index (PyPI)](https://pypi.org/project/pandas) and on [Conda](https://docs.conda.io/en/latest/).

```sh
# conda
conda install pandas
```

```sh
# or PyPI
pip install pandas
```

## Dependencies
- [NumPy - Adds support for large, multi-dimensional arrays, matrices and high-level mathematical functions to operate on these arrays](https://www.numpy.org)
- [python-dateutil - Provides powerful extensions to the standard datetime module](https://dateutil.readthedocs.io/en/stable/index.html)
- [pytz - Brings the Olson tz database into Python which allows accurate and cross platform timezone calculations](https://github.com/stub42/pytz)

See the [full installation instructions](https://pandas.pydata.org/pandas-docs/stable/install.html#dependencies) for minimum supported versions of required, recommended and optional dependencies.

## Installation from sources
To install pandas from source you need [Cython](https://cython.org/) in addition to the normal
dependencies above. Cython can be installed from PyPI:

```sh
pip install cython
```

In the `pandas` directory (same one where you found this file after
cloning the git repo), execute:

```sh
python setup.py install
```

or for installing in [development mode](https://pip.pypa.io/en/latest/cli/pip_install/#install-editable):


```sh
python -m pip install -e . --no-build-isolation --no-use-pep517
```

or alternatively

```sh
python setup.py develop
```

See the full instructions for [installing from source](https://pandas.pydata.org/pandas-docs/stable/getting_started/install.html#installing-from-source).

## License
[BSD 3](LICENSE)

## Documentation
The official documentation is hosted on PyData.org: https://pandas.pydata.org/pandas-docs/stable

## Background
Work on ``pandas`` started at [AQR](https://www.aqr.com/) (a quantitative hedge fund) in 2008 and
has been under active development since then.

## Getting Help

For usage questions, the best place to go to is [StackOverflow](https://stackoverflow.com/questions/tagged/pandas).
Further, general questions and discussions can also take place on the [pydata mailing list](https://groups.google.com/forum/?fromgroups#!forum/pydata).

## Discussion and Development
Most development discussions take place on GitHub in this repo. Further, the [pandas-dev mailing list](https://mail.python.org/mailman/listinfo/pandas-dev) can also be used for specialized discussions or design issues, and a [Slack channel](https://pandas.pydata.org/docs/dev/development/community.html?highlight=slack#community-slack) is available for quick development related questions.

## Contributing to pandas [![Open Source Helpers](https://www.codetriage.com/pandas-dev/pandas/badges/users.svg)](https://www.codetriage.com/pandas-dev/pandas)

All contributions, bug reports, bug fixes, documentation improvements, enhancements, and ideas are welcome.

A detailed overview on how to contribute can be found in the **[contributing guide](https://pandas.pydata.org/docs/dev/development/contributing.html)**.

If you are simply looking to start working with the pandas codebase, navigate to the [GitHub "issues" tab](https://github.com/pandas-dev/pandas/issues) and start looking through interesting issues. There are a number of issues listed under [Docs](https://github.com/pandas-dev/pandas/issues?labels=Docs&sort=updated&state=open) and [good first issue](https://github.com/pandas-dev/pandas/issues?labels=good+first+issue&sort=updated&state=open) where you could start out.

You can also triage issues which may include reproducing bug reports, or asking for vital information such as version numbers or reproduction instructions. If you would like to start triaging issues, one easy way to get started is to [subscribe to pandas on CodeTriage](https://www.codetriage.com/pandas-dev/pandas).

Or maybe through using pandas you have an idea of your own or are looking for something in the documentation and thinking ‘this can be improved’...you can do something about it!

Feel free to ask questions on the [mailing list](https://groups.google.com/forum/?fromgroups#!forum/pydata) or on [Slack](https://pandas.pydata.org/docs/dev/development/community.html?highlight=slack#community-slack).

As contributors and maintainers to this project, you are expected to abide by pandas' code of conduct. More information can be found at: [Contributor Code of Conduct](https://github.com/pandas-dev/.github/blob/master/CODE_OF_CONDUCT.md)
