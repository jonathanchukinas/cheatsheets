# Sphinx

## Project Structure
my_project
│
│   .gitignore
│   Pipfile
│   README.md
│
├───docs
│   │   make.bat
│   │   Makefile
│   │
│   ├───build
│   └───source
│       │   change_log.rst
│       │   conf.py
│       │   eager_lizard.rst
│       │   index.rst
│       │   modules.rst
│       │   readme_pointer.rst
│       │
│       ├───_static
│       └───_templates
└───unnatural_sock
    │   eager_lizard.py

## Step One: Quickstart
```powershell
sphinx-quickstart --ext-autodoc
```

## Step Two: Autodoc
- If you forgot to include the `--ext-autodoc` option during sphinx-quickstart, add `'sphinx.ext.autodoc',` to your list of extensions in conf.py
- run `sphinx-apidoc .\unnatural_sock\ -o .\docs\source\`. This creates a modules.rst and eager_lizard.rst.
- in `eager_lizard.rst`, you have to update `eager_lizard` to say `unnatural_sock.eager_lizard`
- There's actually a better way to do that - append another option to the apidoc command:
	- `sphinx-apidoc .\unnatural_sock\ -o .\docs\source\ --implicit-namespaces`
	
## Pick a Theme
https://github.com/ryan-roemer/sphinx-bootstrap-theme

	
## Step 3: Numpy / Google Docstrings
- https://www.sphinx-doc.org/en/master/usage/extensions/napoleon.html
- https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html


## Step 4: Build the docs
- docs/make.bat clean
- docs/make.bat html

# Examples of good documentation:
- https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_excel.html

## references
- :doc:`filename`


## References

https://romanvm.pythonanywhere.com/post/autodocumenting-your-python-code-sphinx-part-i-5/
- has two links at the bottom to two different reST cheatsheets
- https://github.com/mitmproxy/pdoc: pdoc is an alternative to sphinx, but it doesn't look as well supported.

https://romanvm.pythonanywhere.com/post/autodocumenting-your-python-code-sphinx-part-ii-6/
- What does this mean? `On Windows you need to add \Scripts sub-folder of your Python environment to %PATH%.`
- His example project: https://github.com/romanvm/sphinx_tutorial

https://stackoverflow.com/questions/15090894/how-to-generate-python-documentation-using-sphinx-with-zero-configuration

Then this stackoverflow:
https://stackoverflow.com/questions/56047011/sphinx-auto-documentation-of-project


