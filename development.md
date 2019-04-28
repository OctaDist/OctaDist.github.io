---
layout: default
---
[back to homepage](./)

## Development
***
OctaDist is written in Python 3 binding to TkInter GUI platform. 
It has been tested on Windows OS, macOS, and Linux OS for 32/64-bit system. 
Matplotlib library is used for plotting the graph and displaying the molecule and octahedral structure. <br/>

The program is maintained on Github version control system. If you found a bug in program, please submit it on [issues page](https://github.com/OctaDist/OctaDist/issues). 
To give a contribution on program development, please pull request on [the source code Github](https://github.com/OctaDist/OctaDist). <br/>

We appreciate all help and contribution in getting program development.

## Program structure
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

## Prerequisite
***
OctaDist can run only with Python 3. For Linux user, use following command to check the version of your python.
```
python3 -V
```
The following packages/modules are required.
```
numpy==1.16.0
tkinter==8.6
matplotlib==3.0.2
```

## Program compilation
***
OctaDist source code can be compiled to executable easily using PyInstaller.
```
PyInstaller==3.4
```
Compilation instruction
1. Install [PyInstaller](https://www.pyinstaller.org/)
```
pip install pyinstaller
```
2. Check the version of PyInstaller
```
pyinstaller --version
```
3. Change directory to `./src`, e.g.
```
cd OctaDist-XXX/src/
```
4. Compile the source code, for example, using following command
```
pyinstaller --windowed --onefile -i molecule.ico --version-file=version.txt --distpath=../ main.py
```
5. A standalone executable will be build in `build` directory

[back to homepage](./)
