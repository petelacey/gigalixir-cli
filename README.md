# GIGALIXIR Command-Line Interface

## Installation

    pip install gigalixir

If you don't have pip install, see https://pip.pypa.io/en/stable/installing/

## Quickstart

    gigalixir signup
    gigalixir login
    gigalixir create 
    git push gigalixir
    curl https://$APP_NAME.gigalixirapp.com/

## Documentation

    http://gigalixir.readthedocs.io/en/latest/
    https://www.gigalixir.com

## Testing

    # for python3 
    sudo apt-get install -y python3-venv
    sudo apt-get install -y python3-pip
    python3 -m venv venv3
    source venv3/bin/activate
    pip3 install -e .[dev]
    pip3 install -e .[test]
    python setup.py test

    # e2e tests
    source venv3/bin/activate
    unset GIGALIXIR_ENV
    pip install pytest
    export GIGALIXIR_EMAIL=foo
    export GIGALIXIR_PASSWORD=bar
    pytest -s e2e/test.py

    # hit a development server
    # get into the venv (see above)
    GIGALIXIR_ENV=dev gigalixir account

## Distribute

    # may have to upgrade pip and setuptools with
    # pip install --upgrade pip
    # pip install --upgrade setuptools
    python setup.py sdist upload -r pypitest
    python setup.py sdist upload -r pypi

## Modify documentation

    pip install sphinx
    pip install sphinx_rtd_theme
    cd docs
    make html
    xdg-open build/html/index.html

## Credits

Beaker by Eugen Belyakoff from the Noun Project
