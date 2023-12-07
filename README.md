# About The Repository

Welcome to the CellWorld System Git repository! This repository serves as the main hub for the CellWorld System, which relies on several external submodules. These submodules contain essential software required for the operation of the CellWorld System. 


## Content index

### Notes
Usage column notation:
- M: Used in Main Computer
- H: Used in Habitat Raspberry pi (doors and water feeder controller)
- R: Used in Robot
- A: Used for Data Analysis

### Platforms:
Step: standard computer-aided design (CAD) file format, Step and STL
Eagle: Autodesk Eagle PCB design files
C++: CMake, Make, g++-10 toolchain project
Python: Python 3.7 or newer project
CUDA: NVidia CUDA 12.0 
Pixci: XCLib 3.8 Frame grabber driver with support for linux 6.x kernel


| Folder Name                  | Developed by                                         | Description                                                                       | Type        | Platform         | M        | H        | R        | A        | Prerequisites                                                                |
|------------------------------|------------------------------------------------------|-----------------------------------------------------------------------------------|-------------|------------------|----------|----------|----------|----------|------------------------------------------------------------------------------|
| arena_assembly               | [MacIver Lab](https://github.com/cellworld)          | Designs, CAD files, electronics, software and instructions to build the arena.    | CAD                                                                               | Step, Eagle      | &#10007; | &#10007; | &#10007; | &#10007; | AutoCAD, EAGLE                                                               |
| cellworld                    | [MacIver Lab](https://github.com/cellworld)          | Main software library. Provides access to all objects and services in the system. | Library                                                                           | C++, Python      | &#x2713; | &#x2713; | &#x2713; | &#x2713; | cmake, make, python 3.7 or newer                                             |
| cellworld_agent_tracking     | [MacIver Lab](https://github.com/cellworld)          | Agent tracking library.                                                           | Library                                                                           | C++, Python      | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make, python 3.7 or newer                                             |
| cellworld_experiment_service | [MacIver Lab](https://github.com/cellworld)          | Experiment service library                                                        | Library                                                                           | C++, Python      | &#x2713; | &#x2713; | &#10007; | &#10007; | Python 3.7 or newer, python package: cellworld                               |
| cellworld_habitat_controller | [MacIver Lab](https://github.com/cellworld)          | Experiment control terminal. Main user interface.                                 | Application                                                                       | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | Python 3.7 or newer, python package: cellworld-experiment-service            |
| cellworld_habitat_cv         | [MacIver Lab](https://github.com/cellworld)          | Experiment control terminal. Computer vision application.                         | Application                                                                       | C++, CUDA, Pixci | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make, CUDA, Pixci frame buffer software                               |
| cellworld_habitat_pi         | [MacIver Lab](https://github.com/cellworld)          | Door controller raspberry pi software.                                            | Application                                                                       | C++              | &#x2713; | &#x2713; | &#10007; | &#10007; | Raspberry PI running Raspbian. Python 3.7 or newer, python package cellworld |
| cellworld_pid_controller     | [MacIver Lab](https://github.com/cellworld)          | Robot behavior library.                                                           | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| cellworld_robot_library      | [MacIver Lab](https://github.com/cellworld)          | Robot communication library.                                                      | Library                                                                           | C++, Python      | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make, python 3.7 or newer                                             |
| dependency_catch             | [German Espinosa](https://github.com/germanespinosa) | Unit test library.                                                                | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| dependency_date              | [Howard Hinnant](https://github.com/HowardHinnant)   | Date formatting library.                                                          | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| dependency_easy_tcp          | [German Espinosa](https://github.com/germanespinosa) | TCP network communication library.                                                | Library                                                                           | C++, Python      | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make, python 3.7 or newer                                             |
| dependency_gamepad_lib       | [German Espinosa](https://github.com/germanespinosa) | Gamepad controller library.                                                       | Library                                                                           | C++, Python      | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make, python 3.7 or newer                                             |
| dependency_gauges            | [German Espinosa](https://github.com/germanespinosa) | Progress bars library.                                                            | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| dependency_json_cpp          | [German Espinosa](https://github.com/germanespinosa) | Json data manipulation library.                                                   | Library                                                                           | C++, Python      | &#x2713; | &#x2713; | &#10007; | &#10007; | cmake, make, python 3.7 or newer                                             |
| dependency_mcp2221           | [German Espinosa](https://github.com/germanespinosa) | MCP2221 USB External GPIO library.                                                | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| dependency_params_cpp        | [German Espinosa](https://github.com/germanespinosa) | C++ program argument manipulation library.                                        | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| dependency_perf_analysis     | [German Espinosa](https://github.com/germanespinosa) | C++ performance monitoring library.                                               | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| dependency_perf_request      | [German Espinosa](https://github.com/germanespinosa) | Curl wrapper library.                                                             | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| dependency_tcp_messages      | [German Espinosa](https://github.com/germanespinosa) | Json messages over TCP network library.                                           | Library                                                                           | C++, Python      | &#x2713; | &#x2713; | &#10007; | &#10007; | cmake, make, python 3.7 or newer                                             |
| dependency_thread_poo        | [German Espinosa](https://github.com/germanespinosa) | Optimal Multithreading library.                                                   | Library                                                                           | C++              | &#x2713; | &#10007; | &#10007; | &#10007; | cmake, make                                                                  |
| public_data                  | [MacIver Lab](https://github.com/cellworld)          | Experimental data used for figures.                                               | Data                                                                              | Data             | &#10007; | &#10007; | &#10007; | &#x2713; | Python 3.7 or newer, python packages: cellworld, pandas                      |
| robot_assembly               | [MacIver Lab](https://github.com/cellworld)          | Designs, CAD files, electronics, software and instructions to build the robot.    | CAD                                                                               | Step, Eagle      | &#10007; | &#10007; | &#10007; | &#10007; | AutoCAD, EAGLE                                                               |
| robot_embedded_code          | [MacIver Lab](https://github.com/cellworld)          | Robot ESP32 software including OTA library for real time deployment.              | Embedded                                                                          | C++, ino         | &#10007; | &#10007; | &#x2713; | &#10007; | Arduino GUI                                                                  |


## C++ projects  instructions:
All the C++ projects were developed specifically for Ubuntu 22.04 using C++20 standards. 
Library projects should not be built or installed, they are downloaded from the application projects during configuration time (cmake).
To build an application project, go to the folder containing the CMakeFiles.txt file and follow these instructions:

```shell
mkdir build
cd build
cmake ..
make
```

## Python library installation
All the python libraries are available in pypi and can be installed using pip, e.g: 

```shell
pip install cellworld
pip install cellworld-experiment-service
```
 


## Related Work

The code in this repository is directly related to the methods presented in our research paper titled "A robot-rodent interaction arena with adjustable spatial complexity for ethologically relevant behavioral studies". Here, you'll find the version of all the software essential for operating the system, along with the experimental data presented in this research paper. 

### Supplementary Videos

The supplementary videos referenced in our paper "A robot-rodent interaction arena with adjustable spatial complexity for ethologically relevant behavioral studies" provide a comprehensive demonstration of key aspects of the system. For example, these videos showcase results from a behavior task that leverages the system.

Access the supplemental videos [here](https://doi.org/10.5281/zenodo.10157838) (DOI: 10.5281/zenodo.10157838)

### Figure Code 

A notebook to generate the figures presented in our paper "A robot-rodent interaction arena with adjustable spatial complexity for ethologically relevant behavioral studies" can be accessed [here](https://colab.research.google.com/drive/1EbFh44LEhl9npWPzdv3WODliqK4Q9_h3?usp=sharing). Additionally, the data used to generate these figures is stored within the submodule [public_data](https://github.com/cellworld/public_data/tree/47ff373d1e4ca16e2baa5412820e7f439adcc326).


## More Information
For more detailed information about the CellWorld System, please visit our [cellworld website](https://cellworld.github.io/paper.html). 


## Contact
If you have any questions or need further assistance, feel free to reach out to our lead contact:

Lead Contact: Dr. Malcolm MacIver<br>
Email: maciver@northwestern.edu