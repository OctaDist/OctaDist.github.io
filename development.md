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

| Module     | Description       |
| ---------- | ----------------- |
| main       | Main program |
| coord      | Manipulating atomic coordinates |
| elements   | Atomic properties |
| calc       | Calculating distortion parameters |
| linear     | Built-in mathematical functions |
| projection | 2D & 3D vector projections |
| plot       | Plotting graph and chart |
| plane      | Manipulate projection plane |
| draw       | Displaying molecule |
| tools      | 3rd-part program |
| util       | Other utility |
| popup      | Error, warning, and info messages |

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
or
```
python -v
```
The following external packages/modules are required for running OctaDist:
```
numpy
scipy
matplotlib
```

3rd-party package additionally used in OctaDist-PyPI:
```
rmsd
```

### Program compilation
***

OctaDist source code can be compiled to executable easily using [PyInstaller](https://www.pyinstaller.org/).

Compilation instruction
1. Upgrade pip
   ```
   pip install --upgrade pip
   ```
2. Install PyInstaller:
   ```
   pip install pyinstaller
   ```
3. Check the version of PyInstaller:
   ```
   pyinstaller --version
   ```
4. Change directory to `./octadist` directory, `where main.py` is:
   ```
   cd OctaDist-XXX/octadist/
   ```
5. Compile a standalone, like this:
   ```
   pyinstaller --onefile -i molecule.ico main.py
   ```
   Additionally useful option for compilation can be found at PyInstaller manual.
6. The standalone executable will be build in `dist` directory

[back to homepage](./)
