## Theoretical background

[back to homepage](./)

### Octahedral complex

Octahedral complex is composed of 7 atoms: metal center atom and 6 ligand atoms. It has 8 faces, 6 vertices, and 12 edges. It can be simply classified into two types: regular and distorted octahedrons. The complexes with regular octahedral geometry or perfect octahedron are expected to form, when all of the ligands are of the same kind. In contrast, if the ligands are of different kinds, the complex would turns the distorted octahedron instead. Generally, the structural distortion is found in the [metal-organic framework](https://en.wikipedia.org/wiki/Metal%E2%80%93organic_framework), the [spin-crossover complex](https://en.wikipedia.org/wiki/Spin_crossover), and [perovskite structures](https://en.wikipedia.org/wiki/Perovskite_(structure)).

### Octahedral distortion parameters

Octahedral distortion parameters contain three parameters: ![](https://latex.codecogs.com/svg.Latex?%5CDelta), ![](https://latex.codecogs.com/svg.Latex?%5CSigma), and ![](https://latex.codecogs.com/svg.Latex?%5CTheta). The following just explains how to compute these three parameters, especially we use our new method to compute the ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter. Please refer to [References](#references) for more details.

- Calculation of the ![](https://latex.codecogs.com/svg.Latex?%5CDelta) and ![](https://latex.codecogs.com/svg.Latex?%5CSigma) parameters are straightforward. The ![](https://latex.codecogs.com/svg.Latex?%5CDelta) is the avearge of the sum of the deviation of LG-M distance, where LG and M are ligand atom and metal center atom, from mean distance. The ![](https://latex.codecogs.com/svg.Latex?%5CSigma) is the sum of LG-M-LS angle ( ![](https://latex.codecogs.com/svg.Latex?%5Cphi) ) from the 90 degree.

- The ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter is the sum of the deviation of 24 unique LG-M-LG angles (![](https://latex.codecogs.com/svg.Latex?%5Ctheta)) from 60 degree, where ![](https://latex.codecogs.com/svg.Latex?%5Ctheta) is computed on the orthogonal projection of two twisting triangular faces of the octahedron projected along its pseudo-threefold axes onto the medium plane that containing metal center. However, in reality, becuase of the complex is distorted, the symmetry is changed, so the medium plane between two opposite faces cannot be determined directly. To solve this, we propose a new method to find the optimal 4 faces and use orthogonal vector projection for computing the unique (![](https://latex.codecogs.com/svg.Latex?%5Ctheta)) angles on twisting triangular faces, and for finding the most reasonable ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter.

Mathematical expression of three parameters are given by following equations

![](https://latex.codecogs.com/svg.Latex?%5CDelta%20%3D%20%5Cfrac%7B1%7D%7B6%7D%20%5Csum_%7Bi%20%3D%201%7D%5E%7B6%7D%20%28%5Cfrac%7Bd_%7Bi%7D%20-%20d%7D%7Bd%7D%29%5E2)

<br/>

![](https://latex.codecogs.com/svg.Latex?%5CSigma%20%3D%20%5Csum_%7Bi%20%3D%201%7D%5E%7B12%7D%20%5Cabs%20%5Cleft%20%7C%2090%20-%20%5Cphi_%7Bi%7D%20%7C)

<br/>

![](https://latex.codecogs.com/svg.Latex?%5CTheta%20%3D%20%5Csum_%7Bi%20%3D%201%7D%5E%7B24%7D%20%5Cabs%20%5Cleft%20%7C%2060%20-%20%5Ctheta_%7Bi%7D%20%7C) 

- To find the optimal 4 planes (faces), OctaDist firstly chooses 4 faces out of 8 faces of complex. The total number of combination is 70. Then OctaDist computes the 24 unique (![](https://latex.codecogs.com/svg.Latex?%5Ctheta)) angles for all 70 sets of planes and computes the 70 different values of ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter. The lowest value is chosen as a minimum ![](https://latex.codecogs.com/svg.Latex?%5CTheta) parameter representing the distortion of the octahedral metal complex.

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
