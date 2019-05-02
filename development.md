---
layout: default
---
[back to homepage](./)

## Development
***

### Code maintenance

OctaDist is written in Python 3 binding to Tkinter GUI platform.
It has been tested and deployed on [Travis CI](https://travis-ci.org/), a continuous integration service. It is available for on Windows OS, macOS, and Linux OS for 32/64-bit system. 
Matplotlib library is used for plotting the graph and displaying the molecule and octahedral structure. <br/>

The program is maintained on Github version control system. If you found a bug in program, please submit it on [issues page](https://github.com/OctaDist/OctaDist/issues). 
To give a contribution on program development, please pull request on [the OctaDist Github](https://github.com/OctaDist/OctaDist). <br/>

We appreciate all help and contribution in getting program development.

### OctaDist on PyPI
OctaDist is also available as a Python package, which can be used with command line interface (CLI).
The program is archived on [Python Package Index (PyPI)](https://pypi.org/project/octadist/). 
The source code repository for development build is at [OctaDist-PyPI](https://github.com/OctaDist/OctaDist-PyPI). 

### Program structure
***

| Module | Description |
| ------ | ----------- |
| main   | Main program |
| coord | Read and extract atomic coordinate from input file |
| elements | Atomic properties |
| calc | Calculate octahedral distortion parameters |
| linear | Linear algebra functions |
| projection | Vector projection |
| plane | Manipulate projection plane |
| tools | Utilities |
| draw | Molecular displays |
| popup | Error, warning, and info messages |

OctaDist uses the following built-in Python packages for molecular 3D visualization.
```
tkinter
```

### Prerequisites
***

OctaDist can run only with Python 3. For Linux user, use following command to check the version of your python:
```
python3 -V
```
The following external packages/modules are required for running OctaDist.
```
numpy
scipy
matplotlib
```

### Program compilation
***

OctaDist source code can be compiled to executable easily using [PyInstaller](https://www.pyinstaller.org/).

Compilation instruction
1. Install PyInstaller:
    ```
    pip install pyinstaller
    ```
2. Check the version of PyInstaller:
    ```
    pyinstaller --version
    ```
3. Change directory to `./src`, for example:
    ```
    cd OctaDist-XXX/src/
    ```
4. Compile the source code, for example, using following command:
    ```
    pyinstaller --windowed --onefile -i molecule.ico --version-file=version.txt --distpath=../ main.py
    ```
5. A standalone executable will be build in `build` directory

[back to homepage](./)
