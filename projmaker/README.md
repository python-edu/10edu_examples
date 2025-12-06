# About

A teaching script (tool) designed for:
- automatic project creation
- installation with the `pipx` manager


## What It Does

The script creates a complete project structure in the current directory:

  - creates directories and subdirectories (src layout only)
  - creates metadata files: pyproject.toml, README.md, requirements.txt
  - creates `__init__.py` files
  - creates a virtual environment
  - creates a `src-layout` structure on disk.


## Your Task

Extend the script with the following features:

  - allow the user to provide a list of additional modules using the -d option (dependencies), e.g.:
    
    ```bash
      makeproj projname -d numpy pandas scipy
    ```

  - the script should append these modules to the default list in requirements.txt
  - the script should install all modules listed in requirements.txt into the newly created virtual environment
  - the script should fill in a minimal pyproject.toml using information provided in the `args` object 

---

# How to install 

## Unzipping the zip archive
  1. Download the `projmaker.zip` file from GitHub
  2. Unzip it to the directory where you store your Python projects:
    - Linux/macOS: ```unzip projmaker.zip```
    - Windows: use Windows Explorer or PowerShell: ```Expand-Archive -Path .\projmaker.zip -DestinationPath .```


## Installation with pipx
  - Open the terminal
  - Go to the project's root directory
  - Install: ```pipx install .```


## Editing the code
To continue working with the code and make your own changes, use the `venv` module and the `pip` manager:
  - Create a virtual environment and activate it
  - Install the modules from the `requirements.txt` file
  - Install the script in dveleoper mode - ```python -m pip install -e .```

---


# How to use
## Script installed with pipx
1. Launch the terminal
2. Navigate to the directory where you want to create a new project, e.g., `python_course`
3. Run:
  - ```makeproj - h``` - to get help
  - ```makeproj proj_name``` - to create a new project named `proj_name`

## Working in developer mode
1. Launch the terminal
2. Activate the virtual environment
3. Run:
  - ```makeproj - h``` - to get help
  - ```makeproj proj_name``` - to create a new project named `proj_name`


**Warning:**
  > You must first:

  > - create and activate the virtual environment
  > - install the modules
  > - install the script in developer mode

---
