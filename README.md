[![Build Status](https://travis-ci.org/InformaticsMatters/pipelines-utils-rdkit.svg?branch=master)](https://travis-ci.org/InformaticsMatters/pipelines-utils-rdkit)
[![PyPI version](https://badge.fury.io/py/im-pipelines-utils-rdkit.svg)](https://badge.fury.io/py/im-pipelines-utils-rdkit)

# Pipelines Utils (RDKit)
A repository of common **Informatics Matters** _pipelines_ utilities shared
between a number of _Pipelines_ repositories that rely on the RDKit
open source cheminformatics software.

## Execution environment
You will need: -

-   Conda
-   Python (ideally v3)

The pipelines are based on the [RDKit] Open-Source Cheminformatics Software
and are best executed from within a suitably configured [Conda] environment.
You may need to install some additional modules before you can run the tests,
these dependencies are captured in our own `requirements.txt` file and
installed as normal:

    $ pip install -r requiremenmts.txt

>   The module utilities should support both Python 2 and 3 but we recommend
    any modules/pipelines you write support both flavours.

# Publishing the im-pipelines-utils-rdkit package to PyPI
This project's structure is similar to `pipelines-utils`. For details
on how to publish to pip refer to its documentation.

---

[Conda]: https://conda.io/docs/
[RDKit]: http://www.rdkit.org
