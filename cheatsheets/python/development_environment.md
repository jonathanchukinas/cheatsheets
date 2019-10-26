## Overview
- OS: Windows
- PowerShell terminal
- `venv` for managing virtual environments
- `flit` for packaging, installing, and publishing applications
  - `flit install --pth-file` - editable install

## Build, Package, Publish
```powershell
# KEYRING for storing PyPI login
pip install keyring  # saves password for PyPI
keyring set https://upload.pypi.org/legacy/ <username>
# type password when prompted

# FLIT for build, package, publish
pip install flit
flit publish
```
