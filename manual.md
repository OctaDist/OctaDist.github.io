---
layout: default
---
[back to homepage](./)

## Usage
**Supported input file format**
- [XYZ file format](https://en.wikipedia.org/wiki/XYZ_file_format) (*.xyz)
- Output file of computational chemistry programs (*.out, *.log): Gaussian, NWChem, ORCA, and Q-Chem

## Example input file
***
OctaDist can automatically search and extract the octahedral structure (1 metal center and 6 ligand atoms) from the complex that user submitted.

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
