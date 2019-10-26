# Python Virtual Environments in Windows PowerShell
My terminal of choice is PowerShell, run on Windows 10.
I use Python venv to create and manage virtual environments.
PowerShell functions/aliases make the process even easier.

## Step 1: Edit PowerShell profile
Assuming notepad++ is on your PATH variable, edit the path with `notepad++ $profile`.
Or get the path to your profile with `$profile` and edit it however you please.
- Add the following lines to your profile: 
```powershell
# PYTHON VIRTUAL ENVIRONMENTS
# activate the environment
function vv { .venv\scripts\activate }
# create venv virtual environment
function vc {   
	python -m venv .venv
	"Virtual environment .venv created!"
	vv
	ls
	}
# deactivate the environment
function vd { deactivate }
# remove/delete the environment
function vr {
	remove-item .venv -recurse -force
	"Virtual environment .venv removed!"
	ls
	}
```
Save the profile, then reload using `. $profile`. Or just reopen PowerShell.

## Step 2: Use PowerShell functions to create, (de)activate, and remove environments
- `vc` create and activate an environment
- `vv` activate an existing environment
- `vd` deactivate the current environment
- `vr` remove current environment. You can `vd` before or after this.

## Other
- add the .venv dir to gitignore
- the docs: `https://docs.python.org/3/library/venv.html`
