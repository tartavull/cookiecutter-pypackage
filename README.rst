======================
Cookiecutter PyPackage
======================
Features
--------

* Testing setup with ``unittest`` and ``python setup.py test`` or ``py.test``
* Travis-CI_: Ready for Travis Continuous Integration testing
* Sphinx_ docs: Documentation ready for generation with using github pages
* Bumpversion_: Pre-configured version bumping with a single command
* Auto-release to PyPI_ when you push a new tag to master (optional)
* Command line interface using Click (optional)




Quickstart
----------

Install the latest Cookiecutter if you haven't installed it yet (this requires
Cookiecutter 1.4.0 or higher)::

    pip install -U cookiecutter

Generate a Python package project::

    cookiecutter https://github.com/tartavull/cookiecutter-pypackage.git

Then:

* Create a repo in github and then:
* Go to settings and activate gitub pages in master branch /docs folder
* git init
* make docs
* git add --all
* git commit -m "first commit"
* git remote add origin git@github.com:tartavull/{{repo}}.git
* git push -u origin master
* Add the repo to your Travis-CI_ account.
* Install the dev requirements into a virtualenv. (``pip install -r requirements_dev.txt``)
* Run the script `travis_pypi_setup.py` to encrypt your PyPI password in Travis config
  and activate automated deployment on PyPI when you push a new tag to master branch.
* Register your package in PyPI
* python setup.py register
* Release your package by pushing a new tag to master.
* bumpversion (major|minor|patch)
* git push origin --tags

For more details, see the `cookiecutter-pypackage tutorial`_.

.. _`cookiecutter-pypackage tutorial`: https://cookiecutter-pypackage.readthedocs.io/en/latest/tutorial.html
