Installation
============

.. code-block:: shell

    # Pull Code
    git clone https://github.com/grap/pywebdriverlib
    cd pywebdriverlib

    # Create virtual env and activate it
    virtualenv env --python=python3
    . ./env/bin/activate
    ./env/bin/python3 -m pip install -e .


Package Deployment
==================

.. code-block:: shell

    pip3 install --upgrade setuptools wheel
    pip3 install  --upgrade twine

    # Generate wheel and package
    python3 setup.py sdist bdist_wheel

    # Push on pyPi Test
    twine upload --repository-url https://test.pypi.org/legacy/ dist/*

    # Push on pyPi Production
    twine upload dist/*
