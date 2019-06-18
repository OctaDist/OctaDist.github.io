---
layout: default
---
[back to homepage](./)

## Development
***

### Introduction

OctaDist is written entirely in Python 3 binding to Tkinter GUI platform. 
It is available for Windows, Linux, and macOS for both 32-bit and 64-bit systems. 
It supports both of the graphical user interface (GUI) and the command line interface (CLI). 
The first one is usually suitable for the end-users who are not familiar with Linux command, 
while the latter is for those who are working with CLI such as Linux users. 

### Code maintenance

The source code of OctaDist has been being maintained on Github version control system. 
Both master revision and nightly development build have being tested and deployed on 
[Travis CI][Travis-link], a continuous integration service. 

[Travis-link]: https://travis-ci.org/OctaDist/OctaDist

Program source code on Github: 
- [OctaDist Master: github.com/OctaDist/OctaDist][OctaDist-master-link]
- [OctaDist Dev: github.com/OctaDist/OctaDist/tree/nightly-build][OctaDist-dev-link]

[OctaDist-master-link]: https://github.com/OctaDist/OctaDist
[OctaDist-dev-link]: https://github.com/OctaDist/OctaDist/tree/nightly-build

### Contribution

To give a contribution on program development, please pull request on [the OctaDist Github](https://github.com/OctaDist/OctaDist).
If you found a bug in program, please submit it on [issues page](https://github.com/OctaDist/OctaDist/issues). 
We appreciate all help and contribution in getting program development.

### Program structure
***

| Module     | Description       |
| ---------- | ----------------- |
| main       |  Main program |
| calc       |  Calculating distortion parameters |
| molecule   |  Manipulating atomic coordinates |
| draw       |  Displaying molecule |
| elements   |  Atomic properties |
| linear     |  Built-in mathematical functions |
| plane      |  Manipulate projection plane |
| plot       |  Plotting graph and chart |
| popup      |  Error, warning, and info messages |
| projection |  2D & 3D vector projections |
| structure  |  All data about structure |
| tools      |  Analysis tools by 3rd-party libraries |
| util       |  Frequently-used functions e.g. find atomic bonds |

### Documents

OctaDist Nightly Dev Reference docs: [HTML][Dev-HTML-Link] / [PDF][Dev-PDF-Link] / [Epub][Dev-Epub-Link]

[Dev-HTML-Link]: https://octadist.readthedocs.io/en/nightly-build/
[Dev-PDF-Link]: https://readthedocs.org/projects/octadist/downloads/pdf/nightly-build/
[Dev-Epub-Link]: https://readthedocs.org/projects/octadist/downloads/epub/nightly-build/

### Prerequisites
***

OctaDist supports Python 3.5+. For using the program as CLI, you can use following command to check the version of your current Python:

```sh
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
   ```sh
   pip install --upgrade --user pip
   ```
2. Install PyInstaller:
   ```sh
   pip install --user pyinstaller
   ```
3. Check the version of PyInstaller:
   ```sh
   pyinstaller --version
   ```
4. Change directory to `./octadist` directory, `where main.py` is:
   ```sh
   cd OctaDist-XXX/octadist/
   ```
5. Compile a standalone executable, like this:
   ```sh
   pyinstaller --onefile -windowed -i molecule.ico -n OctaDist main.py
   ```
   Additionally useful option for compilation can be found at PyInstaller manual.
6. The standalone executable will be build in `dist` directory

[back to homepage](./)
