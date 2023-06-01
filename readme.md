# G4SimpleApplication

## ⭐ About this project
This project is very simple example to approach Geant4.

#### Geometry
The main geometry including a World volume that has $100\times100\times100 cm^3$ of dimensions. The World volume was filled Air material.

#### Physics
The interface is defined in G4VModularPhysicsList. This interface is derived from the G4VUserPhysicsList interface.

I used RegisterPhysics() method to add G4EmStandardPhysics_option3 constructor. This physic constructor is recommended for medical physic application. 

#### Primary Generator
A point source placed at center of World volume. The source emitted gamma rays isotropic has 1.0 MeV.

The G4ParticleGun() method was used to define source.

#### Scoring


## 🔧 Requirements
* Ubuntu 20.04 (Tested)
* Geant4.10.07 (Tested)

#### a) Pre-Packages installation
- Open Ubuntu Terminal and type the following commands to update Ubuntu system.
    ```c++
    $ sudo apt-get update && sudo apt-get upgrade
    ```

- Installing pre-package using the following commands
    ```c++
    $ sudo apt-get install build-essential apt-file gcc g++ autoconf automake automake1.11 tcl8.6-dev tk8.6-dev libglu1-mesa-dev libgl1-mesa-dev libxt-dev libxmu-dev libglew-dev libglw1-mesa-dev gfortran inventor-dev libxaw7-dev freeglut3-dev libxerces-c-dev libxmltok1-dev qt5-default libxi-dev libclutter-gtk-1.0-0 cmake libxmlrpc-core-c3-dev tclxml tclxml-dev libexpat1-dev libgtk2.0-dev libxpm-dev x11proto-gl-dev x11proto-input-dev -y
    sudo apt-get install dpkg-dev cmake g++ gcc binutils libx11-dev libxpm-dev libxft-dev libxext-dev python libssl-dev gfortran libpcre3-dev xlibmesa-glu-dev libglew1.5-dev libftgl-dev libmysqlclient-dev libfftw3-dev libcfitsio-dev graphviz-dev libavahi-compat-libdnssd-dev libldap2-dev python-dev libxml2-dev libkrb5-dev libgsl0-dev qtwebengine5-dev
    ```

#### b) Geant4 installation
- I assumed that I want to install Geant4 in path ../Software/
- Create a new "Geant4" inside "Softwares" folder 
- Create 2 new folders named "build" and "install" inside "Geant4" folder.
- Copy Geant4 source code that downloaded from Geant4 Homepage to "Geant4" folder and rename to "source".
- Download all data files and extract to "data" folder that created inside "Geant4" folder.
- We will have 4 folders

    ../Softwares/Geant4/\
    ├── build\
    ├── data\
    ├── install\
    └── source

- Let open Terminal in "build" folder and type
    ```c++
    $ cmake -DGEANT4_INSTALL_DATADIR=../data \
    -DGEANT4_USE_GDML=ON \
    -DGEANT4_USE_HDF5=OFF \
    -DGEANT4_USE_OPENGL_X11=ON \
    -DGEANT4_USE_QT=ON \
    -DGEANT4_BUILD_MULTITHREADED=ON \ 
    -DCMAKE_INSTALL_PREFIX=../install \
    ../source
    $ make -j4
    $ sudo make install
    ```
#### c) Environment variables
- Add "geant4.sh" and "geant4make.sh" to at the end of file "/home/user_name/.bashrc", for example
    ```c++
    source "/home/hungbt/Softwares/Geant4/install/bin/geant4.sh"
    source "/home/hungbt/Softwares/Geant4/install/share/Geant4-10.7.4/geant4make/geant4make.sh"
    ```

## 🏃‍♂️ How to run
- Create a new folder to build example. For example, I created "bld" folder.
    ```c++
    mkdir bld
    cd bld
    ```
- Build
    ```c++
    cmake ..
    make -j4
    ```
- Run example in interactive mode
    ```c++
    ./SimApp
    ```
- Run example in batch mode
    ```c++
    ./SimApp run.mac
    ```

## 📒 References

## 🚀 About Me
**Bùi Tiến Hưng**

Master of Science in Nuclear Engineering.

Nuclear Engineering Lab, Hanoi University of Science and Technology (HUST).

Department of Planning and R&D Management, Vietnam Atomic Energy Institute (VINATOM).

**Interestet Fields**

Medical physics, Monte-Carlo simulation, Machine learning.
 
buitienhung@vinatom.gov.vn\
hungbt1908@gmail.com

Vietnam Atomic Energy Institute, No 59 Ly Thuong Kiet street, Hoan Kiem district, Hanoi, Vietnam. 