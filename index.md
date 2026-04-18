# Geant4
For any possible Geant4 Simulation

# Setup
*This manual setup is for Ubuntu distribution (or WSL). For other OS, please find the tutorial at [Installation Guide](https://geant4-userdoc.web.cern.ch/UsersGuides/InstallationGuide/html/ "Link to installation guide")*.

1. Download the source file & directory from the official website.
- Copy the tar.gz link (right click &rarr; copy address link).

2. Unzip the tar file using below command at bash terminal.
'''bash
tar xyfv geant4-v11.4.1.tar.gz
'''
The decompressed tar file will be located in the folder named `geant4-v<version>`

3. Create a build directory. `geant4-v<version>-build` and direct into it `cd *build`.  

4. Compile the installed source file. (`cmake` with argument of where the `CMakeLists.txt` file is located, for this case is in the directory we unzip just now.) 
```bash
cmake ../geant4-v<version>
```

Remarks
- *if cmake is not installed in your system, please install by* 
```bash
sudo apt install cmake
```.
- *check if below prerequisites packages are installed, if not, install using the one liner command below.*
```bash
sudo apt install -y g++ gcc binutils libx11-dev libxpm-dev libxft-dev libxext-dev libglew-dev libjpeg-dev libpng-dev libtiff-dev libgif-dev libxml2-dev libssl-dev libfftw3-dev libqt5core5a
```

Compiler        : `g++`,`gcc`
Geant Recommend : `binutils`
Development pkg : `libx11-dev`,`libxpm-dev` `libxft-dev`,`libxext-dev`.`libglew-dev`,`libjpeg-dev`,
                  `libpng-dev`,`libtiff-dev`,`libgif-dev`.`libxml2-dev`,`libssl-dev`,`libfftw3-dev`,`libqt5core5a`
*development package corresponding to output of graphics*.

5. Start the build in same directory.
```bash
make -j$(nproc1)
```
