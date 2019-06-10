---
layout: default
---
[back to homepage](./) | [manual](./manual.md)

## Installing
***

- [Windows OS](#windows-os)
- [Linux OS](#linux-os)
- [macOS](#macos)
- [PyPI](#pypi)
- [Anaconda](#anaconda)

***

### Windows OS

Most of the Windows end-users do not have Python installed on their OS, 
so it is suggested to download a ready-to-use OctaDist GUI for your system.

For first time using OctaDist, you should run the program as an administrator with full rights.
Changing property of program can be completed in a few steps as follows:

1. Download program executable (\*.exe) to your machine.
   ```
   OctaDist-2.5.4-Win-x86-64.exe
   ```
2. Right click on program icon and select **`Run as administrator`**.
3. Click **`Yes`**.
4. Wait program for process until open.

### Linux OS

1. Download the source code (*.tar.gz) to your machine, for example, at **`Download`** directory.
2. Uncompress the tarball, using **`tar`**: 
   ```
   tar -xzvf OctaDist-2.5.4-Linux-x86-64.tar.gz
   ```
3. Move to OctaDist root directory, using **`cd`**:
   ```
   cd OctaDist-2.5.4-Linux-x86-64
   ```
4. Check if your system has all dependencies for OctaDist:
   ```
   python CheckPyModule.py
   ```
5. Execute program as a package (note that you have to stay outside **`octadist`** directory):
   ```
   python -m octadist.Run
   ```

### macOS

Installing and running the program on Mac are the same as Linux.

1. Download the source code (*.tar.gz) to your machine, for example, at **`Download`** directory.
2. Press Command - spacebar to launch Spotlight and type "*Terminal*", then double-click the search result.
3. Uncompress the tarball, using **`tar`**: 
   ```
   tar -xzvf OctaDist-2.5.4-macOS-x86-64.tar.gz
   ```
4. Move to OctaDist root directory, using **`cd`**:
   ```
   cd OctaDist-2.5.4-macOS-x86-64
   ```
5. Check if your system has all dependencies for OctaDist:
   ```
   python CheckPyModule.py
   ```
6. Set `TkAgg` backend environment variable to prevent the dependencies error:
   ```
   export MPLBACKEND=TkAgg
   ``` 
7. Execute program (you have to stay outside **`octadist`** directory):
   ```
   python -m octadist.Run
   ```

### PyPI  

[![PyPI-Server][PyPI-badge]][PyPI-link]

[PyPI-badge]: https://img.shields.io/pypi/v/octadist.svg
[PyPI-link]: https://pypi.org/project/octadist/

OctaDist is also available on Python package index (PyPI) library, 
which can be found at [https://pypi.org/project/octadist/][OctaDist-PyPI-link].

The end-user can use `pip`, a Python package-management system, 
to find and install OctaDist and other dependencies at the same time.

[OctaDist-PyPI-link]: https://pypi.org/project/octadist/

The following commands might be useful:
- Install program: 
  ```
  pip install octadist
  ```
- Upgrade to the latest version: 
  ```
  pip install --upgrade octadist
  ```
- Downgrade to a certain version, for example, version 2.5.4:
  ```
  pip install --upgrade octadist==2.5.4
  ```

More details on installing Python package can be found its official website: 
[https://packaging.python.org/tutorials/installing-packages/][Packaging-Python-link].

[Packaging-Python-link]: https://packaging.python.org/tutorials/installing-packages/

### Anaconda 

[![Conda-Server][Conda-badge]][Conda-link]

[Conda-badge]: https://anaconda.org/rangsiman/octadist/badges/version.svg
[Conda-link]: https://anaconda.org/rangsiman/octadist

OctaDist is also available on Anaconda cloud server.
The channel of OctaDist is at [https://anaconda.org/rangsiman/octadist][OctaDist-Conda].

[OctaDist-Conda]: https://anaconda.org/rangsiman/octadist 

It can be installed on system using command.

```
conda install -c rangsiman octadist 
```

The platforms that OctaDist-Conda supported: [![Anaconda-Server Badge][Conda-platform-badge]][Conda-platform-link]

[Conda-platform-badge]: https://anaconda.org/rangsiman/octadist/badges/platforms.svg
[Conda-platform-link]: https://anaconda.org/rangsiman/octadist


[back to homepage](./) | [manual](./manual.md)
