# Overview
- OS: Windows
- PowerShell terminal
- `venv` for managing virtual environments
- `flit` for packaging, installing, and publishing applications
  - `flit install --pth-file` - editable install
  
# Documentation
- Sphinx - see this great intro article: https://dont-be-afraid-to-commit.readthedocs.io/en/latest/documentation.html

# Build, Package, Publish
```powershell
# KEYRING for storing PyPI login
pip install keyring  # saves password for PyPI
keyring set https://upload.pypi.org/legacy/ <username>
# type password when prompted

# FLIT for build, package, publish
pip install flit
flit publish
```

# Versioning
- See semantic versioning (semver)

# Development Pipeline
- git
  - make sure the previous version was tagged in git
  - `git checkout -b featurename`
- code
  - write tests
  - write code
  - tox - ensure all PASSes and 100% coverage
- documentation
  - docstrings
  - tutorial, readme
  - update change log
  - make html
  - quality check in browser
  - increment version (semver)
- git
  - `git fetch`, check, then `git pull`
  - `git rebase -i master`
- flit
  - `flit publish`
- git
  - `git tag -a vX.Y.Z -m featurename`
  - `git push --delete origin featurename`
  - `git checkout master`
  - `git merge featurename`
  - `git push`
- readthedocs

# TODO
- connect to and automate readthedocs
- Show project structure
- Create a cookiecutter for my process
