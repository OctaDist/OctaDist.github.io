---
layout: default
---
[back to homepage](./)

## Development
***

### Introduction

OctaDist is written entirely in Python 3 binding to Tkinter GUI platform. 
It is available for Windows, Linux, and macOS for both 32-bit and 64-bit systems. 
It is divided into two versions as different types of uses: 
a graphical user interface (GUI) version and a command line interface (CLI) version. 
The former is mainly developed for the end-users, who are not familiar with Linux command, 
while the latter is appropriate for the end-users and programmer who are working with CLI, 
for example, on Linux or macOS. 

### Code maintenance

The source code of OctaDist is maintained on Github version control system. 
Both master revision and nightly development build have being tested and deployed on 
[Travis CI](https://travis-ci.org/), a continuous integration service. 

Program source code on Github: 
- [OctaDist GUI (master): github.com/OctaDist/OctaDist][Github-GUI-master-link]
- [OctaDist GUI (dev): github.com/OctaDist/OctaDist/tree/nightly-build][Github-GUI-dev-link]
- [OctaDist CLI : github.com/OctaDist/OctaDist-PyPI][Github-CLI-link]

[Github-GUI-master-link]: https://github.com/OctaDist/OctaDist
[Github-GUI-dev-link]: https://github.com/OctaDist/OctaDist/tree/nightly-build
[Github-CLI-link]: https://github.com/OctaDist/OctaDist-PyPI

### Contribution

To give a contribution on program development, please pull request on [the OctaDist Github](https://github.com/OctaDist/OctaDist).
If you found a bug in program, please submit it on [issues page](https://github.com/OctaDist/OctaDist/issues). 
We appreciate all help and contribution in getting program development.

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
| tools      | 3rd-party library |
| util       | Utilities |
| popup      | Error, warning, and info messages |

### Documents

OctaDist GUI Reference docs: [HTML][GUI-HTML-Link] / [PDF][GUI-PDF-Link] / [Epub][GUI-Epub-Link]

OctaDist CLI Reference docs: [HTML][CLI-HTML-Link] / [PDF][CLI-PDF-Link] / [Epub][CLI-Epub-Link]

[GUI-HTML-Link]: https://octadist.readthedocs.io/en/latest/
[GUI-PDF-Link]: https://readthedocs.org/projects/octadist/downloads/pdf/latest/
[GUI-Epub-Link]: https://readthedocs.org/projects/octadist/downloads/epub/latest/

[CLI-HTML-Link]: https://octadist-pypi.readthedocs.io/en/latest/
[CLI-PDF-Link]: https://readthedocs.org/projects/octadist-pypi/downloads/pdf/latest/
[CLI-Epub-Link]: https://readthedocs.org/projects/octadist-pypi/downloads/epub/latest/

### Prerequisites
***

OctaDist supports Python 3.5+. For using the program as CLI, you can use following command to check the version of your current Python:

```
python -v
```

The 3rd party libraries are required for OctaDist for GUI and CLI (PyPI) are following:

```
numpy
scipy
matplotlib
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
