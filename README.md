# psv_bev_loop (We are cleaning the code, It will be soon available online)

This is the repository for our novel loop closure detection approach using surface variation to build the BEV image.
It also builds three BEV for robust rejection of invalid loop closures. The use of surface variation yields more ORB features than normalized point density in our tests.

## Installation
### Dependencies
- DBoW3 library (included in ThirdParty folder)
- srrg_hbst library
- OpenCV library
- Eigen library
- Boost library
- PCL library
- OpenMP library

### Method 1:
Note that the loop closing library is header-only. If you want to include to your code just copy the psv_bev_loop_dbow3.hpp and psv_bev_utils.h to your project.
You need to link the DBoW3 library and srrg_hbst to your project. Check the provided CMakeLists.txt for details.

### Method 2:
You can also build the ROS2 package and use it as a dependency in your own ROS2 project.

## Usage
### Evaluation
Go to your workspace where the evaluation codes are built
The second command is of the form ./evaluate_MC <path_to_bag_file> <path_to_output_file>
```
cd /ros2_ws/install/psv_lcd/lib/psv_lcd
./evaluate_MC /media/autoj/autoj1-T7/research_data/open_data/MulRan/bags2/Riverside02 /media/autoj/ouattaraT7/research_data/loop_results/gupta_check.txt

```
To be updated.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation
If you use this code in your research, please cite our paper (and leave a star):

```
@article{psv_lcd,
title = {PSV-LCD: Point cloud Surface Variation based Loop Closure Detection},
<!-- journal = {IFAC-PapersOnLine}, -->
note = {8th IFAC Conference on Sensing, Control and Automation Technologies for Agriculture AGRICONTROL 2025},
year={2025}
author = {Issouf Ouattara and Arto Visala},
keywords = {loop closure detection, surface variation, LiDAR, point cloud, SLAM}
}
```

## Acknowledgments
This project was highly inspired by the work of [Saurabh Gupta](https://github.com/PRBonn/MapClosures). The use of HBST was based on their implementation.
This work also uses several open-source libraries such as DBoW3, srrg_hbst, OpenCV, Eigen, Boost, PCL, and OpenMP. Thanks to the contributors of these libraries for their valuable work.

## Contributions
We welcome contributions to this project. Please submit a pull request or open an issue if you have any suggestions or improvements.
Feel free to fork this repository and contribute your improvements.
