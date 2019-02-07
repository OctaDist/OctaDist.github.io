---
layout: default
---

# OctaDist

OctaDist has been written in Python 3.7.2 and tested on PyCharm 2018.3.2 (Community Edition). Program executable was compiled by Pyinstaller. The program supports Windows systems, Mac OS, and GNU/Linux OS. <br/>

[Click here](https://github.com/OctaDist/OctaDist/releases/latest) to download the latest stable version of OctaDist.

## Why OctaDist?
### Distortion in Octahedral Geometry

Octahedral complex is composed of 7 atoms: metal center atom and 6 ligand atoms. It has 8 faces, 6 vertices, and 12 edges. It can be simply classified into two types: regular and distorted octahedrons. The complexes with regular octahedral geometry or perfect octahedron are expected to form, when all of the ligands are of the same kind. In contrast, if the ligands are of different kinds, the complex would turns the distorted octahedron instead. Generally, the structural distortion is found in the [metal-organic framework](https://en.wikipedia.org/wiki/Metal%E2%80%93organic_framework), the [spin-crossover complex](https://en.wikipedia.org/wiki/Spin_crossover), and [perovskite structures](https://en.wikipedia.org/wiki/Perovskite_(structure)).

### Purpose
Octahedral distortion parameters have been being widely used in inorganic cheemistry, especially crystallography, for determining the structural distortion of octahedral metal complex. Even though the people in community generally compute these parameters for their synthesized complex, but they not used a certain way to do this. Moreover, there is no software for determining this kind of parameter yet. Therefore, we present the OctaDist program as a choice for those who are interested in this.

[Click here](./param.md) to read more about octahedral distortion parameters

## Usage
### Windows OS
1. Download program executable from [this page](https://github.com/rangsimanketkaew/OctaDist/releases)
2. Right click and select `Run as administrator`
3. Click `Yes`
4. Wait program for process until open

### Mac OS X
1. Download program source code from [this page](https://github.com/rangsimanketkaew/OctaDist/releases)
2. Uncompress the tarball: `tar -xzvf OctaDist-*`
3. Enter OctaDist directory: `cd OctaDist-*/src`
4. Change file permission of all python files: `chmod +x *.py`
5. Compile executable using PyInstaller: `pyinstaller --onefile main.py`

### Linux OS
For Linux user, use `python3 -V` to check python version.
1. Download program source code from [this page](https://github.com/rangsimanketkaew/OctaDist/src)
2. Uncompress the tarball: `tar -xzvf OctaDist-*`
3. Enter OctaDist directory: `cd OctaDist-*/src`
4. Change file permission of all python files: `chmod +x *.py`
5. Execute program: `python3 main.py`

### Required module

```
numpy==1.16.0
tkinter==8.6
matplotlib==3.0.2
PyInstaller==3.4
```

### Supported input file format
- [XYZ file format](https://en.wikipedia.org/wiki/XYZ_file_format) (*.xyz)
- Text file format (*.txt)
- Output file of several computational chemistry programs (*.out, *.log): Gaussian, NWChem, and ORCA

### Input preparation
The current version of OctaDist only supports the cartesian (XYZ) coordinate file (see [Testing](#testing)) <br/>
**1. First seven atoms must be the studied octahedral structure.** <br/>
**2. A metal center atom of octahedron must be the first atom. So the next six atoms would be six ligand atoms.**


[Click here for testing examples](./testing.md)


## Screenshots

Program UI | Console window |
:-------------------------:|:-------------------------:
![](images/Capture_Program.png)   | ![](images/Capture_Window.png) 

**Display of full complex and selected octahedron**

Full complex | Full complex with faces of octahedron |
:-------------------------:|:-------------------------:
![](images/Figure_1.png)   | ![](images/Figure_2.png) 
**Selected octahedral structure** | **Optimal 4 faces** 
![](images/Figure_3.png)  | ![](images/Figure_4.png)

## References
1. [J. A. Alonso, M. J. Martı´nez-Lope, M. T. Casais, M. T. Ferna´ndez-Dı´az. Inorg. Chem. 2000, 39, 917-923](https://pubs.acs.org/doi/abs/10.1021/ic990921e)
2. [J. K. McCusker, A. L. Rheingold, D. N. Hendrickson. Inorg. Chem. 1996, 35, 2100-2112](https://pubs.acs.org/doi/abs/10.1021/ic9507880)
3. [M. Marchivie, P. Guionneau, J. F. Letard, D. Chasseau. Acta Crystal-logr. Sect. B Struct. Sci. 2005, 61, 25-28](https://onlinelibrary.wiley.com/doi/full/10.1107/S0108768104029751)

## Special thanks
I would like to thank

- [Prof. Yuthana Tantirungrotechai](https://sites.google.com/site/compchem403/people/faculty/yuthana) (Thammasat University, Thailand)
- [Prof. David J. Harding](https://www.funtechwu.com/david-j-harding) (Walailak University, Thailand)

for useful advices and comments.

## Author
Rangsiman Ketkaew<br/>
Computational Chemistry Research Unit <br/>
Department of Chemistry, Faculty of Science and Technology <br/>
Thammasat University, Pathum Thani, 12120 Thailand <br/>
E-mail: [rangsiman1993@gmail.com](rangsiman1993@gmail.com) <br/>
Website: [https://sites.google.com/site/rangsiman1993](https://sites.google.com/site/rangsiman1993)
