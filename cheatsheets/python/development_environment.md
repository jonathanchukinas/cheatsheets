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
  - (optional) `git push --set-upstream origin featurename`
- code
  - write tests, commit
  - write code, commit
  - tox - ensure all PASSes and 100% coverage
  - commit
- documentation
  - docstrings
  - tutorial, readme
  - update change log
  - make html
  - quality check in browser
- version
  - increment version (semver)
  - commit
- git
  - `git fetch`, check, then `git pull`
  - `git rebase -i master`
- flit
  - `flit publish`
  - if fail, go back to git step
- git
  - `git tag -a vX.Y.Z -m featurename`
  - `git push --delete origin featurename` (only if I had pushed it to remote)
  - `git checkout master`
  - `git merge featurename`
  - `git branch -d featurename`
  - `git push`
  - `git push --tags`
- readthedocs

# TODO
- connect to and automate readthedocs
- Show project structure
- Create a cookiecutter for my process
