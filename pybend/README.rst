Python Backend
==============

Setup Dev Local
---------------

.. code-block:: bash

    conda env create -n "conda-<project-name>"
    conda env list
    conda activate "conda-<project-name>"

    cd pybend
    python -m venv .venv
    source .venv/bin/activate
    poetry install


Run Internal API
----------------

.. code-block:: bash

    uvicorn api.main:app
