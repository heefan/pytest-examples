# Most Simplest Installable Package Example

Goal: to understand make a installable package.
keyword: `setup.py` `setuptools`


### Project Structure:

```bash
❯ exa
drwxr-xr-x  - litian 22 Feb 17:41 .
.rw-r--r-- 31 litian 22 Feb 17:37 ├── module.py
.rw-r--r-- 68 litian 22 Feb 17:36 ├── setup.py
.rw-r--r-- 45 litian 22 Feb 17:42 └── tu.md
```

### Important code snippet

```python
from setuptools import setup

setup(name="ex1", py_modules=["ex1"])
```

### Run it

```bash
❯ pip install .
Processing /Users/litian/workspace/github/pytest-examples/installable-module/ex1
  Preparing metadata (setup.py) ... done
Building wheels for collected packages: ex1
  Building wheel for ex1 (setup.py) ... done
  Created wheel for ex1: filename=ex1-0.0.0-py3-none-any.whl size=935 sha256=ed53a2083a1e9f222bef12c12929a4951d0f3a6ea29cf1dfdc92497adb289772
  Stored in directory: /private/var/folders/q6/vtdblmbj1fzbsnk823npxt8r0000gn/T/pip-ephem-wheel-cache-zgehpokm/wheels/56/04/9c/71a95a3482a9ef33c5984394b2150075ec07b80e47b867bf20
Successfully built ex1
Installing collected packages: ex1
Successfully installed ex1-0.0.0
```

Generated Folder

`build/` `ex1.egg-info/` generated

1. should not commit to github.
2. put them into gitignore.

```bash
❯ exa
drwxr-xr-x   - litian 22 Feb 17:45 .
drwxr-xr-x   - litian 22 Feb 17:45 ├── build
drwxr-xr-x   - litian 22 Feb 17:45 │  └── bdist.macosx-13.1-arm64
drwxr-xr-x   - litian 22 Feb 17:45 ├── ex1.egg-info
.rw-r--r--   1 litian 22 Feb 17:45 │  ├── dependency_links.txt
.rw-r--r-- 128 litian 22 Feb 17:45 │  ├── PKG-INFO
.rw-r--r-- 116 litian 22 Feb 17:45 │  ├── SOURCES.txt
.rw-r--r--   4 litian 22 Feb 17:45 │  └── top_level.txt
.rw-r--r--  31 litian 22 Feb 17:37 ├── module.py
.rw-r--r--  68 litian 22 Feb 17:36 ├── setup.py
.rw-r--r-- 476 litian 22 Feb 17:45 └── tu.md
```

Q: Where is the package installed?  

`pip show [your-package]`

```bash
❯ pip show ex1
Name: ex1
Version: 0.0.0
Summary: UNKNOWN
Home-page: UNKNOWN
Author: 
Author-email: 
License: UNKNOWN
Location: /Users/litian/.pyenv/versions/3.9.10/Library/Frameworks/Python.framework/Versions/3.9/lib/python3.9/site-packages
Requires: 
Required-by: 
```

Q: How to uninstall it?

`pip uninstall ex1`