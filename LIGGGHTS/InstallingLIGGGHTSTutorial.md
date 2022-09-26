---
layout: page
title: Installing PICI-LIGGGHTS
parent: LIGGGHTS
permalink: /InstallingPICI-LIGGGHTS/
---

# Installing PICI-LIGGGHTS
{: .fs-9 }

A step-by-step guide with video, instructions and commands for installing _PICI-LIGGGHTS_ with high level Python interface _CoExSiST_ on Ubuntu 20.04.
**Note**: This doesn't work on Ubuntu 22.04 so make sure to use **Ubuntu 20.04**. 
If you don't have a computer running Ubuntu I would recommend using a VM software such as VirtualBox to set up an Ubuntu VM.

1. Firstly, download a clone of the _PICI-LIGGGHTS_ zip from GitHub found [here](https://github.com/uob-positron-imaging-centre/PICI-LIGGGHTS){:target="_blank"}.

2. Extract the zip file and move to your location of choice.

3. Install build-essential to install everything required for compiling basic C and C++ software.

       sudo apt install build-essential

4. Install libboost-dev for additional C++ source libraries (Prevents some errors when compiling _PICI-LIGGGHTS_).

       sudo apt install libboost-dev

5. Install CMake that can be used to automatically build _PICI-LIGGGHTS_ for us later.

       sudo snap install cmake --classic

6. Install Open MPI, an open source MPI to allow _PICI-LIGGGHTS_ to make use of parallelisation.

       sudo apt install openmpi-bin

7. Go to the extracted _PICI-LIGGGHTS_ master folder and make build folder inside.

       mkdir build && cd build

8. Once inside the build folder run the CMake command to make the CMake files.

       cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_CXX_FLAGS="-O3 -march=native -fPIC" ../src/

9. Once CMake is finished, run the 'make' command to start building _PICI-LIGGGHTS_. (This make take some time)

       make -j4

10. Copy 'libliggghts.so' to a standard location.

        sudo cp libliggghts.so /usr/local/lib

11. Copy liggghts.py to the Python packages location.

        cd ..
        cd python
        sudo cp liggghts.py /usr/local/lib/python3.8/dist-packages/

12. Add /usr/local/lib to library path.

        LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH

13. A simple Python interface of _PICI-LIGGGHTS_ should now be able to be run from Python. It is a good idea to test at this point if it works.
    1. Optional: Test _PICI-LIGGGHTS_ works in Python: Install idle (Or your text editor/IDE of choice)
             
           sudo apt install idle

    2. Run idle

           idle

    3. Type Python lines to import _PICI-LIGGGHTS_ and start liggghts object.
    
           from liggghts import liggghts
           liggghts()
        
14. To use the high level Python interface we need to install the Python package _CoExSiST_. To do this we need the Python package manager pip.
    
        sudo apt install pip

15. Install _CoExSiST_ Python package.

        pip install coexist

16. All done! _PICI-LIGGGHTS_ and _CoExSiST_ are installed. Check _CoExSiST_ works by opening your text editor/IDE of choice and importing coexist to make sure no errors occur.

        import coexist
