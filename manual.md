---
layout: default
---
[back to homepage](./)

## Supported file format
***
1. [XYZ file format](https://en.wikipedia.org/wiki/XYZ_file_format) (*.xyz)
2. Output file of computational chemistry programs (*.out, *.log): Gaussian, NWChem, ORCA, and Q-Chem


## Running OctaDist
***
OctaDist can automatically search and extract the octahedral structure from the complex that user submitted.

### Windows OS
1. Download program executable to your PC/Laptop
2. Right click on program icon and select `Run as administrator`
3. Click `Yes`
4. Wait program for process until open

### macOS
- More to come.

### Linux OS
1. Download program source code from [this page](https://github.com/OctaDist/OctaDist/src)
2. Uncompress the tarball: `tar -xzvf OctaDist-*`
3. Enter OctaDist directory: `cd OctaDist-*/src`
4. Change file permission of all python files: `chmod +x *.py`
5. Execute program: `python3 main.py`

## Prerequisite
***
- OctaDist can run only with Python 3. For Linux user, use `python3 -V` to check python version.

- The following packages/modules are required.
```
numpy==1.16.0
tkinter==8.6
matplotlib==3.0.2
PyInstaller==3.4
```

## Program compilation
***
OctaDist source code can be compiled to executable easily using PyInstaller.
1. Install [PyInstaller](https://www.pyinstaller.org/)
2. Change directory to `./src`.
3. Compile the source code, for example, using following command
```
`pyinstaller --onefile --version-file=version.txt --distpath=../ -i molecule.ico --windowed main.py`
```

## Example usage
***
**Perfect octahedral metal complex** <br/>
([Perfect-octahedron.xyz](https://raw.githubusercontent.com/OctaDist/OctaDist/master/test/Perfect-octahedron.xyz))

Calculate octahedral distortion parameters

- ![](https://latex.codecogs.com/svg.Latex?%5CDelta) = 0.00000000
- ![](https://latex.codecogs.com/svg.Latex?%5CSigma) = 0.00000000 degree
- ![](https://latex.codecogs.com/svg.Latex?%5CTheta) = 0.00000000 degree

---

**XRD structure of [Fe(1-bpp)2][BF4]2 complex in low-spin state, taken from Malcolm Halcrow's CCDC library** <br/>
([[Fe(1-bpp)2][BF4]2-LS-Full.xyz](https://raw.githubusercontent.com/OctaDist/OctaDist/master/test/%5BFe(1-bpp)2%5D%5BBF4%5D2-LS-Full.xyz))

Calculate octahedral distortion parameters
- ![](https://latex.codecogs.com/svg.Latex?%5CDelta) = 0.000348
- ![](https://latex.codecogs.com/svg.Latex?%5CSigma) = 86.081494 degree
- ![](https://latex.codecogs.com/svg.Latex?%5CTheta) = 271.388567 degree

---

**XRD structure of [Fe(1-bpp)2][BF4]2 complex in high-spin state, taken from Malcolm Halcrow's CCDC library** <br/>
([[Fe(1-bpp)2][BF4]2-HS-Full.xyz](https://raw.githubusercontent.com/OctaDist/OctaDist/master/test/%5BFe(1-bpp)2%5D%5BBF4%5D2-HS-Full.xyz))

Calculate octahedral distortion parameters
- ![](https://latex.codecogs.com/svg.Latex?%5CDelta) = 0.000168
- ![](https://latex.codecogs.com/svg.Latex?%5CSigma) = 150.814795 degree
- ![](https://latex.codecogs.com/svg.Latex?%5CTheta) = 469.590198 degree

[back to homepage](./)
