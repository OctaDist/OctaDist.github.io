---
layout: default
---

## OctaDist

OctaDist (**Octa**hedral **Dist**ortion Analysis) is a program for computing the octahedral distortion parameters of a distorted octahedral complexes. Octahedral distortion parameters have been being widely used in inorganic cheemistry, especially crystallography, for determining the structural distortion of octahedral metal complex. Even though the people in community generally compute these parameters for their synthesized complex, but they not used a certain way to do this. Moreover, there is no software for determining this kind of parameter yet. Therefore, we present the OctaDist program as a choice for those who are interested in this. [Click here to read more about theretical background of OctaDist](./param.md)

***

## Development
OctaDist has been written in Python 3.7.2 binding to TkInter graphical interface and tested on PyCharm 2018.3.2 (Community Edition). Program executable was compiled by Pyinstaller. The program supports Windows, macOS, and Linux OS for both 32-bit and 64-bit systems

***

## Release
The latest stable version of OctaDist is 2.2 (February 2019). [The release is available here](https://github.com/OctaDist/OctaDist/releases/latest) 

***

## Usage
**Windows**
1. Download program executable `.exe` to your machine
2. Right click on program icon and select `Run as administrator`
3. Click `Yes`
4. Wait program for process until open

**macOS**
<br/>
_Please wait for update_

**Linux**
1. Download the tarbal of program source code from to your machine
2. Uncompress the tarball: `tar -xzvf OctaDist-*`
3. Enter OctaDist directory: `cd OctaDist-*/src`
4. Change file permission of all python files: `chmod +x *.py`
5. Execute program: `python3 main.py`

**Requirements**
* Use `python3 -V` to check python version and use `python3 -m pip install -U PACKAGE_NAME` to update python packages.
* For running OctaDist on graphical display client through SSH session, you should add `-X` or `-Y` when logging-in SSH.
* The following Python modules are required
```
numpy==1.16.0
tkinter==8.6
matplotlib==3.0.2
PyInstaller==3.4
```

**Supported input file format**
- [XYZ file format](https://en.wikipedia.org/wiki/XYZ_file_format) (*.xyz)
- Text file format (*.txt)
- Output file of several computational chemistry programs (*.out, *.log): Gaussian, NWChem, ORCA, and Q-Chem

[Click here for input preparation and testing examples](./testing.md)

***

## Screenshots
**Program GUI**

Program UI | Console window |
:-------------------------:|:-------------------------:
![](images/Capture_Program.png)   | ![](images/Capture_Window.png) 


**Display of full complex and selected octahedron**

|All atoms                         | Full complex with faces of octahedron  |
|:--------------------------------:|:--------------------------------------:|
|![](images/Figure_1.png)          | ![](images/Figure_2.png)               |
|**Selected octahedral structure** | **Optimal 4 faces**                    |
|![](images/Figure_3.png)          | ![](images/Figure_4.png)               |

## Citation
If your work has been done by OctaDist, please citing as following

```
OctaDist - A program for determining the structural distortion of the octahedral complexes.
https://octadist.github.io
```

## References
1. [J. A. Alonso, M. J. Martı´nez-Lope, M. T. Casais, M. T. Ferna´ndez-Dı´az. Inorg. Chem. 2000, 39, 917-923](https://pubs.acs.org/doi/abs/10.1021/ic990921e)
2. [J. K. McCusker, A. L. Rheingold, D. N. Hendrickson. Inorg. Chem. 1996, 35, 2100-2112](https://pubs.acs.org/doi/abs/10.1021/ic9507880)
3. [M. Marchivie, P. Guionneau, J. F. Letard, D. Chasseau. Acta Crystal-logr. Sect. B Struct. Sci. 2005, 61, 25-28](https://onlinelibrary.wiley.com/doi/full/10.1107/S0108768104029751)

## Developer team
- [Rangsiman Ketkaew](https://sites.google.com/site/rangsiman1993) (Thammasat University, Thailand) E-mail: rangsiman1993@gmail.com
- [Yuthana Tantirungrotechai](https://sites.google.com/site/compchem403/people/faculty/yuthana) (Thammasat University, Thailand)
- [David J. Harding](https://www.funtechwu.com/david-j-harding) (Walailak University, Thailand)
