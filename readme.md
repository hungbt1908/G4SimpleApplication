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
No quantities were recorded.

## 🔧 Requirements
* Ubuntu 20.04
* Geant4.10.07

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
    ![](image/Screenshot%202023-06-02%20103517.png)

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