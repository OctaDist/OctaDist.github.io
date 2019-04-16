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
Installation instruction of PyInstaller
1. Install [PyInstaller](https://www.pyinstaller.org/)
2. Change directory to `./src`.
3. Compile the source code, for example, using following command
```
`pyinstaller --onefile --version-file=version.txt --distpath=../ -i molecule.ico --windowed main.py`
```

[back to homepage](./)
