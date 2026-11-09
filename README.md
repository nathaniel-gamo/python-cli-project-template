# Python CLI Project Template

A template for Python command-line interface (CLI) projects.

## Commands

### Create a .env file
```
MAX_RETRIES=3
RETRY_INTERVAL_SECONDS=0
RETRY_RAISE_EXCEPTION=True
```

### Create a virtual environment
```bash
python -m venv .venv
```

### Activate the virtual environment
```bash
.venv\Scripts\Activate.ps1
```

### Verify that the virtual environment is activated
```bash
Get-Command python
```

### Upgrade pip
```bash
python -m pip install --upgrade pip
```

### Install dependencies
```bash
pip install -r requirements.txt
```

### Update packages using pip-review
```bash
pip-review
pip-review --auto
pip-review --interactive
```

### Build a package using build
```bash
pip install build
python -m build
```

### Upload the package to TestPyPI using twine
```bash
pip install twine
python -m twine check dist/*
python -m twine upload --repository testpypi dist/*
```

### Upload the package to PyPI using twine
```bash
pip install twine
python -m twine check dist/*
python -m twine upload dist/*
```

### Create an executable using Nuitka
```bash
python -m nuitka main.py --onefile --windows-console-mode=force --remove-output --assume-yes-for-downloads --output-filename=python-cli-project-template.exe --output-dir="C:\Users\{User Profile}\Downloads"
```

### Create an executable using PyInstaller
```bash
pip install pyinstaller
pyinstaller main.py --onefile --console --clean --name "python-cli-project-template" --distpath "C:\Users\{User Profile}\Downloads"
```