---
layout: default
---
[back to homepage](./) | [manual](./manual.md)

## Installing
***

- [Installing](#installing)
  - [Windows](#windows)
  - [Linux](#linux)
  - [macOS](#macos)
  - [PyPI](#pypi)
  - [Anaconda](#anaconda)
  - [Source Code](#source-code)

***

### Windows

Most of the Windows end-users do not have Python installed on the system. 
Thus, we strongly suggest you download and use a pre-built OctaDist executable 
instead of compile a binary file your self.

1. Download program executable (\*.exe) to your machine.
   ```sh
   OctaDist-2.6.1-Win-x86-64.exe
   ```
   
2. Right click on program icon and select **`Run as administrator`**.

3. Click **`Yes`**.

FYI: For first time using OctaDist, you should run it as an administrator with full rights.

### Linux

OctaDist is available on Python package index (PyPI) library, 
which can be found at [https://pypi.org/project/octadist]().

The easiest way to install OctaDist for the end-user is the use of `pip`, 
a Python package-management system.

Installing OctaDist can be done in a few steps, as follows:

1. Use ``pip`` command to install OctaDist:
   ```sh
   pip install octadist
   ```
  
2. Start OctaDist GUI, just type:
   ```sh
   octadist
   ```
   
   or
   
   ```sh
   octadist_gui
   ```
   
3. If you want to run OctaDist with command-line, just type:
   ```sh
   octadist_cli
   ```

### macOS

Like Linux, installing OctaDist on macOS can be completed in a few steps as follows:

1. Press **Command** - **spacebar** to launch Spotlight and type `Terminal`,
then double-click the search result.

2. Use ``pip`` command to install OctaDist:
   ```sh
   pip install octadist
   ```
  
3. Start OctaDist GUI, just type:
   ```sh
   octadist
   ```
   
   or
   
   ```sh
   octadist_gui
   ```
   
4. If you want to start OctaDist by command-line, just type:
   ```sh
   octadist_cli
   ```

### PyPI  

[![PyPI-Server][PyPI-badge]][PyPI-link]

[PyPI-badge]: https://img.shields.io/pypi/v/octadist.svg
[PyPI-link]: https://pypi.org/project/octadist/

The following commands are also useful for those who want to play with ``pip``:

- Show info of package:
  ```sh
  pip show octadist
  ```
  
- Install requirements packages:
  ```sh
  pip install -r requirements.txt
  ```

- Upgrade to the latest version:
  ```sh
  pip install --upgrade octadist
  ```

- Upgrade/downgrade to a certain version, for example, version 2.6.1:
  ```sh
  pip install --upgrade octadist==2.6.1
  ```

- Uninstall program:
  ```sh
  pip uninstall octadist
  ```

More details on installing Python package can be found on Python tutorial website: 
[https://packaging.python.org/tutorials/installing-packages/][Packaging-Python-link].

[Packaging-Python-link]: https://packaging.python.org/tutorials/installing-packages/
  
OctaDist installed by `pip` can be called anywhere with command-line: 

For example:

```sh
octadist_cli
```

Moreover, OctaDist can be imported as an external library in Python source file, like this:

```python
import octadist

print(octadist.__version__)     # '2.6.1'
```

### Anaconda 

[![Conda-Server][Conda-badge]][Conda-link]
[![Anaconda-Server Badge][Conda-platform-badge]][Conda-platform-link]

[Conda-badge]: https://anaconda.org/rangsiman/octadist/badges/version.svg
[Conda-link]: https://anaconda.org/rangsiman/octadist
[Conda-platform-badge]: https://anaconda.org/rangsiman/octadist/badges/platforms.svg
[Conda-platform-link]: https://anaconda.org/rangsiman/octadist


OctaDist is also available on Anaconda cloud server.
The channel of OctaDist is at [https://anaconda.org/rangsiman/octadist][OctaDist-Conda].

[OctaDist-Conda]: https://anaconda.org/rangsiman/octadist 

It can be installed on system using command:
```sh
conda install -c rangsiman octadist 
```

To update OctaDist to the latest version:
```sh
conda update -c rangsiman octadist
```

It is also a good idea to create a personal environment. 
For example, I create the environment called `newenv` for OctaDist project.

```sh
conda create -n newenv python=3.7
activate newenv
conda update --all
```

Then install OctaDist using `conda`:

```sh
conda install -c rangsiman octadist
```

FYI: OctaDist package on the conda server is imported from PyPI server.


### Source Code

To build OctaDist from source:

1. Check if your system has all dependencies for OctaDist:
   ```sh
   python CheckPyModule.py
   ```
   
2. Download the source code (\*.tar.gz) to your machine, for example, at **Download** directory:
   ```sh
   OctaDist-*-src-x86-64.tar.gz
   ```
   
3. Uncompress the tarball, using **tar**:
   ```sh
   tar -xzvf OctaDist-*-src-x86-64.tar.gz
   ```
   
4. Move to OctaDist root directory, using **cd**:
   ```sh
   cd OctaDist-*-src-x86-64
   ```
   
5. Execute program like a package (you have to stay outside **octadist** directory):
   ```sh
   python -m octadist
   ```
   or command-line:
   ```sh
   python -m octadist_cli
   ```
   

[back to homepage](./) | [manual](./manual.md)
