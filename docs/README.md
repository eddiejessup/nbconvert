# Documenting nbconvert

[Documentation for `nbconvert`](https://nbconvert.readthedocs.org/en/latest/)
is hosted on ReadTheDocs.

## Build Documentation locally

1. Change directory to documentation root:

           $ cd docs

2. Create conda env (and install relevant dependencies):

           $ conda env create -f environment.yml

3. Activate the newly built conda environment `nbconvert_docs`

           $ source activate nbconvert_docs

4. Build documentation using Makefile for Linux and OS X:

           $ make html

  or on Windows:

           $ make.bat html

5. Display the documentation locally by navigating to
   ``build/html/index.html`` in your browser:

   Or alternatively you may run a local server to display
   the docs. In Python 3:

           $ python -m http.server 8000

   In your browser, go to `http://localhost:8000`.

Note: If you want, you can manually convert this install to an editable install 
by using ``pip uninstall nbconvert`` and ``pip install -e ..`` while still at the
top of this ``docs`` directory. This will allow you to rebuild the html on the fly 
to reflect the current edits you are making to the documentation (though that will still require re-running the `make html` command). 

## Developing Documentation

### Helpful files and directories

* `conf.py` - Sphinx build configuration file
* `source` directory - source for documentation
* `source/api` directory - source files for generated API documentation
* `autogen_config.py` - Generates configuration of ipynb source files to rst
* `index.rst` - Main landing page of the Sphinx documentation
