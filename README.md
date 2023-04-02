# ME5413_Final_Project
ME5413 Final Project from Group 16
> Authors: Shen Xiaoting, Zeng Jinling, Lei Haoran, Shang Jiajian
## Installation
```bash
# Clone your own fork of this repo (assuming home here `~/`)
cd
git clone https://github.com/LiLiLiNaNaNa/ME5413_Final_Project.git
cd ME5413_Final_Project

# Install all dependencies
rosdep install --from-paths src --ignore-src -r -y

# Build
catkin_make
# Source 
source devel/setup.bash
```
## Usage

### 0. Gazebo World

This command will launch the gazebo with the project world

```bash
# Launch Gazebo World together with our robot
roslaunch me5413_world world.launch
```
### 1. Mapping

After launching **Step 0**, in the second terminal:

```bash
# Launch Karto Mapping
roslaunch me5413_world mapping_karto.launch
```
