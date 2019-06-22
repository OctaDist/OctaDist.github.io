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

### Contribution

To give a contribution on program development, please pull request on [the OctaDist Github][OctaDist-master-link].
If you found a bug in program, please submit it on [issues page][OctaDist-issue-github]. 
We appreciate all help and contribution in getting program development.

[OctaDist-master-link]: https://github.com/OctaDist/OctaDist
[OctaDist-dev-link]: https://github.com/OctaDist/OctaDist/tree/nightly-build
[OctaDist-issue-github]: https://github.com/OctaDist/OctaDist/issues

### Program structure
***

| Module     | Description       |
| ---------- | ----------------- |
| main       | Main program |
| calc       | Calculating distortion parameters |
| draw       | Displaying molecule |
| elements   | Atomic properties |
| linear     | Built-in mathematical functions |
| molecule   | Manipulating atomic coordinates |
| plane      | Manipulate projection plane |
| plot       | Plotting graph and chart |
| popup      | Error, warning, and info messages |
| projection | 2D & 3D vector projections |
| scripting  | Interactive code Console |
| structure  | All data about structure |
| tools      | Analysis tools by 3rd-party libraries |
| util       | Frequently-used functions e.g. find atomic bonds |

### Application Program Interface (API)
***

| API version  | Description       | 
| ------------ | ----------------- |
| octadist_gui | Graphical user interface (__main__.py) | 
| octadist_cli | Command line interface (octadist_cli.py) | 


### Reference Documents

OctaDist Master Stable docs: [HTML][Stable-HTML-Link] / [PDF][Stable-PDF-Link] / [Epub][Stable-Epub-Link]

OctaDist Nightly Dev docs: [HTML][Dev-HTML-Link] / [PDF][Dev-PDF-Link] / [Epub][Dev-Epub-Link]

[Stable-HTML-Link]: https://octadist.readthedocs.io/en/latest/
[Stable-PDF-Link]: https://readthedocs.org/projects/octadist/downloads/pdf/latest/
[Stable-Epub-Link]: https://readthedocs.org/projects/octadist/downloads/epub/latest/
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

You need to install these libraries before running the program, 
otherwise it will fail to start. The latest version is suggested.

To install requirements:
```sh
pip install -r requirements.txt
```

### Build the tarball, wheel, and egg files

- `.tar.gz` : the tarball (supported by PIP)
- `.whl` : wheel file (supported by PIP)
- `.egg` : cross-platform zip file (supported by easy_install)

1. Build source code:
   ```sh
   python setup.py sdist bdist_wheel bdist_egg
   ```
   
2. Install OctaDist:
   ```sh
   python setup.py install
   ```
   or:
   ```sh
   pip install dist/*.tar.gz
   ```
   
3. Run test zip files:
   ```sh
    python setup.py test
   ```
   
4. Installed library of OctaDist will be install at ``build/lib/octadist`` directory.

5. OctaDist executable files will be automatically added to environment variables,
you can call the program anywhere and anytime:

- To start GUI:
   ```sh
   octadist
   ```
   
  or:
   ```sh
   octadist_gui
   ```
   
- To start command-line:
  ```sh
  octadist_cli
  ```
   
More details on Python package can be found its official website:
https://packaging.python.org/tutorials/installing-packages.

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
   cd OctaDist-*-src-x86-64/octadist/
   ```
   
5. Compile a standalone executable, like this:
   ```sh
   pyinstaller --onefile --windowed -n OctaDist-*-src-x86-64 main.py
   ```
   
6. The standalone executable will be build in `dist` directory

[back to homepage](./)
