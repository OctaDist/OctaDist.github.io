---
layout: default
---
[back to homepage](./)

## User manual
***

### Supported file format
1. [XYZ file format](https://en.wikipedia.org/wiki/XYZ_file_format) (*.xyz)
2. Output file of computational chemistry programs (*.out, *.log): 
[Gaussian](https://gaussian.com/), 
[NWChem](http://www.nwchem-sw.org/index.php/Main_Page), 
[ORCA](https://orcaforum.kofo.mpg.de/app.php/portal), 
and [Q-Chem](https://www.q-chem.com)

### Installing and Running OctaDist
***

#### Windows OS
1. Download program executable (\*.exe) to your PC/Laptop.
2. Right click on program icon and select `Run as administrator`.
3. Click `Yes`.
4. Wait program for process until open.

#### macOS
1. Download program executable ([Mach-O](https://en.wikipedia.org/wiki/Mach-O)) to your Mac.
2. Press Command - spacebar to launch Spotlight and type "*Terminal*", then double-click the search result.
3. Navigate to directory where the OctaDist file is, using `cd`.
4. Execute program: `./OctaDist-*`.

#### Linux OS
1. Download the source code (*.tar.gz) to your machine.
2. Uncompress the tarball: `tar -xzvf OctaDist-*`.
3. Enter OctaDist directory: `cd OctaDist-*`.
4. Check is your machine has required packages for running OctaDist: `python3 CheckPyModule.py`.
5. Enter OctaDist source code sub-directory: `cd src`.
6. Execute program: `python3 main.py`.

#### PyPI

Additionally, other way for using OctaDist is running it with command user interface (CLI).
At PyPI, the end-user can find and install OctaDist using `pip` command on the terminal command line in their OS.

1. For installing OctaDist, use the following command:
   - Install the latest version:
   
        ```
        pip install octadist
        ```
        
   - Upgrade to the latest version: 
   
        ```
        pip install --upgrade octadist
        ```
        
   - Upgrade/downgrade to a specific version: 
   
        ```
        pip install --upgrade octadist==2.5.0
        ```

2. Pip will find the dependencies at the same time, and install all packages.


More details on installing Python package is [here](https://packaging.python.org/tutorials/installing-packages/).

### Computing the parameters
***

#### OctaDist - GUI version
1. Click `Browse file`, choose one or multiple input files, then click `Open`.
2. OctaDist will automatically search octahedral structure and atomic labels and coordinates from the complex that user submitted.
3. Check whether the program has loaded and read input file successfully.
4. If yes, then click `Compute`.
5. The computed parameters will be shown in output box.
6. To save the computational results, click `File`, then `Save results`.

#### OctaDist - CLI version

Example scripts are available at [here](https://github.com/OctaDist/OctaDist-PyPI/tree/master/example-py).

1. Install OctaDist using  `pip` (see above).

2. First of all, you have to import necessary modules for computing the octahedral distortion parameters, called `calc`:

    ```
    from octadist import calc
    ```

3. Prepare list (or array) for atomic labels and coordinates:

    ```
    atom = ['Fe', 'O', 'O', 'N', 'N', 'N', 'N']
    
    coor = [[2.298354000, 5.161785000, 7.971898000],
            [1.885657000, 4.804777000, 6.183726000],
            [1.747515000, 6.960963000, 7.932784000],
            [4.094380000, 5.807257000, 7.588689000],
            [0.539005000, 4.482809000, 8.460004000],
            [2.812425000, 3.266553000, 8.131637000],
            [2.886404000, 5.392925000, 9.848966000]]
    ```

    or you can open input file and extract the octahedral structure from input metal complex using a module called `coord`:

    ```
    from octadist import coord, calc
    ```

    For example, input file `full\path\of\your\input\file\Multiple-metals.xyz` 
    (other example input files are available at [here](https://github.com/OctaDist/OctaDist-PyPI/tree/master/example-input)):
    
    ```
    file = r"full\path\of\your\input\file\Multiple-metals.xyz"
    
    atom, coor = coord.extract_octa(file)
    ```

4. Then calculate all octahedral parameters

    ```
    d_mean, zeta, delta, sigma, theta = calc.calc_all(atom, coor)
    ```

5. Print all computed parameters:

    ```
    All computed parameters
    -----------------------
    Zeta  = 0.22807256171728651
    Delta = 0.0004762517834704151
    Sigma = 47.926528379270124
    Theta = 122.688972774546
    ```

### Example usage
***

**1. Perfect octahedral metal complex** <br/>
([Perfect-octahedron.xyz](https://raw.githubusercontent.com/OctaDist/OctaDist/master/example-input/Perfect-octahedron.xyz))

Calculate octahedral distortion parameters

- ![](https://latex.codecogs.com/svg.Latex?%5CDelta) = 0.00000000
- ![](https://latex.codecogs.com/svg.Latex?%5CSigma) = 0.00000000 degree
- ![](https://latex.codecogs.com/svg.Latex?%5CTheta) = 0.00000000 degree

---

**2. XRD structure of [Fe(1-bpp)2][BF4]2 complex in low-spin state, taken from Malcolm Halcrow's CCDC library** <br/>
([[Fe(1-bpp)2][BF4]2-LS-Full.xyz](https://raw.githubusercontent.com/OctaDist/OctaDist/master/example-input/%5BFe(1-bpp)2%5D%5BBF4%5D2-LS-Full.xyz))

Calculate octahedral distortion parameters
- ![](https://latex.codecogs.com/svg.Latex?%5CDelta) = 0.000348
- ![](https://latex.codecogs.com/svg.Latex?%5CSigma) = 86.081494 degree
- ![](https://latex.codecogs.com/svg.Latex?%5CTheta) = 271.388567 degree

---

**3. XRD structure of [Fe(1-bpp)2][BF4]2 complex in high-spin state, taken from Malcolm Halcrow's CCDC library** <br/>
([[Fe(1-bpp)2][BF4]2-HS-Full.xyz](https://raw.githubusercontent.com/OctaDist/OctaDist/master/example-input/%5BFe(1-bpp)2%5D%5BBF4%5D2-HS-Full.xyz))

Calculate octahedral distortion parameters
- ![](https://latex.codecogs.com/svg.Latex?%5CDelta) = 0.000168
- ![](https://latex.codecogs.com/svg.Latex?%5CSigma) = 150.814795 degree
- ![](https://latex.codecogs.com/svg.Latex?%5CTheta) = 469.590198 degree

[back to homepage](./)
