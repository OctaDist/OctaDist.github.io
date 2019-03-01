---
layout: default
---
[back to homepage](./)

## About OctaDist
***
### Background
Octahedral complex can be simply classified into two types: regular and distorted octahedrons. The complexes with regular octahedral geometry or perfect octahedron are expected to form, when all of the ligands are of the same kind. In contrast, if the ligands are of different kinds, the complex would turns the distorted octahedron instead. Octahedral distortion parameters has been widely used for determining the change of the distortion of the complexes. Even though the people in community generally compute the octahedral distortion parameters for their complexes, but they not used a certain way to do this. Moreover, there is no software for determining this kind of parameter yet. Therefore, we present the OctaDist program as a choice for those who are interested in this.

### Octahedral distortion parameters
Octahedral distortion parameters contain three parameters: ![](https://latex.codecogs.com/svg.Latex?%5CDelta), ![](https://latex.codecogs.com/svg.Latex?%5CSigma), and ![](https://latex.codecogs.com/svg.Latex?%5CTheta). The following just explains how to compute these three parameters, especially we use our new method to compute the ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter. Please refer to [References](#references) for more details. <br/>

Calculation of the ![](https://latex.codecogs.com/svg.Latex?%5CDelta) and ![](https://latex.codecogs.com/svg.Latex?%5CSigma) parameters are straightforward. The ![](https://latex.codecogs.com/svg.Latex?%5CDelta) is the avearge of the sum of the deviation of LG-M distance, where LG and M are ligand atom and metal center atom, from mean distance. The ![](https://latex.codecogs.com/svg.Latex?%5CSigma) is the sum of LG-M-LS angle ( ![](https://latex.codecogs.com/svg.Latex?%5Cphi) ) from the 90 degree. <br/>

The ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter is the sum of the deviation of 24 unique LG-M-LG angles (![](https://latex.codecogs.com/svg.Latex?%5Ctheta)) from 60 degree, where ![](https://latex.codecogs.com/svg.Latex?%5Ctheta) is computed on the orthogonal projection of two twisting triangular faces of the octahedron projected along its pseudo-threefold axes onto the medium plane that containing metal center. However, in reality, becuase of the complex is distorted, the symmetry is changed, so the medium plane between two opposite faces cannot be determined directly. To solve this, we propose a new method to find the optimal 4 faces and use orthogonal vector projection for computing the unique (![](https://latex.codecogs.com/svg.Latex?%5Ctheta)) angles on twisting triangular faces, and for finding the most reasonable ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter.

Mathematical expression of three parameters are given by following equations

![](https://latex.codecogs.com/svg.Latex?%5CDelta%20%3D%20%5Cfrac%7B1%7D%7B6%7D%20%5Csum_%7Bi%20%3D%201%7D%5E%7B6%7D%20%28%5Cfrac%7Bd_%7Bi%7D%20-%20d%7D%7Bd%7D%29%5E2) <br/>

![](https://latex.codecogs.com/svg.Latex?%5CSigma%20%3D%20%5Csum_%7Bi%20%3D%201%7D%5E%7B12%7D%20%5Cabs%20%5Cleft%20%7C%2090%20-%20%5Cphi_%7Bi%7D%20%7C) <br/>

![](https://latex.codecogs.com/svg.Latex?%5CTheta%20%3D%20%5Csum_%7Bi%20%3D%201%7D%5E%7B24%7D%20%5Cabs%20%5Cleft%20%7C%2060%20-%20%5Ctheta_%7Bi%7D%20%7C) <br/>

To determine the distortion parameters, OctaDist firstly find the optimal 4 faces out of 8 faces of octahedral complexes. The total number of combination of faces is 70. OctaDist then computes the 24 unique (![](https://latex.codecogs.com/svg.Latex?%5Ctheta)) angles for all 70 sets. Therefore, a distorted octahedral structure has 70 different values of ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter. The lowest ![](https://latex.codecogs.com/svg.Latex?%5CTheta) is chosen for representing the deviation of a distorted complex from perfect octahedral structure.

**Graphical representation of orthogonal projection and twisting triangular faces**

|Distorted octahedron | Orthogonal projection of atoms onto the given (opposite) plane | The ![](https://latex.codecogs.com/svg.Latex?%5Ctheta) angle between the atom vectors defined by two twisting triangular faces|
|:-------------------------:|:-------------------------:|:-------------------------:|
|![](images/Co-complex-8faces.png) | ![](images/Co-complex-projection.png) | ![](images/Co-complex-2D-projection.png)|

### References
1. [J. A. Alonso, M. J. Martı´nez-Lope, M. T. Casais, M. T. Ferna´ndez-Dı´az. Inorg. Chem. 2000, 39, 917-923](https://pubs.acs.org/doi/abs/10.1021/ic990921e)
2. [J. K. McCusker, A. L. Rheingold, D. N. Hendrickson. Inorg. Chem. 1996, 35, 2100-2112](https://pubs.acs.org/doi/abs/10.1021/ic9507880)
3. [M. Marchivie, P. Guionneau, J. F. Letard, D. Chasseau. Acta Crystal-logr. Sect. B Struct. Sci. 2005, 61, 25-28](https://onlinelibrary.wiley.com/doi/full/10.1107/S0108768104029751)

<br/>

[back to homepage](./)
