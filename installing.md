---
layout: default
---
[back to homepage](./) | [manual](./manual.md)

## Installing and Running OctaDist
***

- [Windows OS](#windows-os)
- [Linux OS](#linux-os)
- [macOS](#macos)
- [PyPI repository](#pypi)

***

### Windows OS

1. Download program executable (\*.exe) to your PC/Laptop.
2. Right click on program icon and select **`Run as administrator`**.
3. Click **`Yes`**.
4. Wait program for process until open.

### Linux OS

1. Download the source code (*.tar.gz) to your machine.
2. Uncompress the tarball: 
   ```
   tar -xzvf OctaDist-*-Linux-x86-64.tar.gz
   ```
3. Move to OctaDist root directory:
   ```
   cd OctaDist-*-Linux-x86-64
   ```
4. Check is your machine has required packages for running OctaDist:
   ```
   python CheckPyModule.py
   ```
5. Execute program:
   ```
   python -m src/main
   ```

### macOS

1. Download program executable ([Mach-O](https://en.wikipedia.org/wiki/Mach-O)) to your Mac.
2. Press Command - spacebar to launch Spotlight and type "*Terminal*", then double-click the search result.
3. Navigate to directory where the OctaDist file is, using **`cd`**.
4. Execute program:
   ```
   ./OctaDist-*-macOS-x86-64
   ```

### PyPI  [![PyPI-Server][PyPI-badge]][PyPI-link]

[PyPI-badge]: https://img.shields.io/pypi/v/octadist.svg
[PyPI-link]: https://pypi.org/project/octadist/

OctaDist is also an on-going package of Python package index (PyPI), which is available at [https://pypi.org/project/octadist/](https://pypi.org/project/octadist/).
The end-user can use `pip`, a Python package manager, to find and install OctaDist and other dependencies on OS at the same time.

The following commands are useful:
- Install (and upgrade to) the latest version: 
  ```
  pip install --upgrade octadist
  ```
- Downgrade to a certain version:
  ```
  pip install --upgrade octadist==2.5.0
  ```

More details on installing Python package is [here](https://packaging.python.org/tutorials/installing-packages/).

### Conda [![Conda-Server][Conda-badge]][Conda-link]

[Conda-badge]: https://anaconda.org/rangsiman/octadist/badges/version.svg
[Conda-link]: https://anaconda.org/rangsiman/octadist

OctaDist on Anaconda cloud server is available at [https://anaconda.org/rangsiman/octadist](https://anaconda.org/rangsiman/octadist). 

It can be installed on system using command.

```
conda install -c rangsiman octadist 
```

The platforms that OctaDist-Conda supported: [![Anaconda-Server Badge](https://anaconda.org/rangsiman/octadist/badges/platforms.svg)](https://anaconda.org/rangsiman/octadist)

[back to homepage](./) | [manual](./manual.md)
