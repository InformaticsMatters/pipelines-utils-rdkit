[![Build Status](https://travis-ci.org/InformaticsMatters/pipelines-utils-rdkit.svg?branch=master)](https://travis-ci.org/InformaticsMatters/pipelines-utils-rdkit)
[![Coverage Status](https://coveralls.io/repos/github/InformaticsMatters/pipelines-utils-rdkit/badge.svg?branch=master)](https://coveralls.io/github/InformaticsMatters/pipelines-utils-rdkit?branch=master)

# Pipelines Utils (RDKit)
A repository of common **Informatics Matters** _Pipeline_ utilities shared
between a number of _Pipelines_ repositories that rely on the RDKit
open source cheminformatics software.

## Execution environment
You will need: -

-   Java
-   Conda
-   Groovy (v2.4)
-   Python
-   An operating system that supports symbolic links

>   It is vital that you install and setup a Java installation (especially by
    also setting `JAVA_HOME` correctly) _before_ you install groovy. Observed
    on Windows 7. If you do not groovy assumes a 32-bit environment and
    then cannot call into a 64-bit java. 

Although the project is based on [Gradle], which is Groovy-based,
you will need to install **Groovy**. We've tested this framework using Groovy
`v2.4.11`.

The pipelines are based on the [RDKit] Open-Source Cheminformatics Software
and are best executed from within a suitably configured [Conda] environment.
You may need to install some additional modules before you can run the tests,
these dependencies are captured in our own `requiremenmts.txt` file and
installed as normal:

    $ pip install -r requiremenmts.txt

>   The module utilities should support both Python 2 and 3 but we recommend
    any modules/pipelines you write support both flavours.

### Publishing the im-pipelines-utils-rdkit package to PyPI
The utilities are published to PyPI for easy installation
(normally automatically by the Travis CI/CD framework
when the repository is tagged on master).

If you are going to publish the utilities yourself (not recommended) you will
need our PyPI account details. For Informatics Matters you should add the
following to your `~/.pypirc` file (or create one if you don't have one): -

    [pypi]
    username: informaticsmatters
    password: <password>

To publish a new set of Python utilities you then simply need to build
and upload them from the `src/python` directory: -

    $ pip install -r requirments.txt
    $ python setup.py bdist_wheel
    $ twine upload dist/*

>   Before publishing (or tagging for automatic publishing) you must ensure
    that the package version is new (currently defined in `setup.py`).
    If you re-publish a package PyPI will respond with an error. Once you
    have released version 1.0.0 you cannot release it again. Ever.
    
>   For acceptable version number formatting you should follow [PEP-440].

>   The Travis CI/CD service (controlled by the `.travis.yml` file)
    automatically publishes the PyPI package when the `master` branch is tagged
    using label begins `pypi-`
    
---

[RDKit]: http://www.rdkit.org
