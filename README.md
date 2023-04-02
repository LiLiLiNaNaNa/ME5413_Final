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

After finishing mapping, run the following command in the thrid terminal to save the map:

```bash
# Save the map as `my_map` in the `maps/` folder
roscd me5413_world/maps/
rosrun map_server map_saver -f my_map map:=/map
```

### 2. Navigation

Once completed **Step 1** mapping and saved your map, quit the mapping process.

Then, in the second terminal:

```bash
roslaunch me5413_world teb_hybridastar_nav.launch
```

or

```bash
roslaunch me5413_world navigation.launch
```

or

```bash
roslaunch me5413_world navigation_teb_loc.launch
```

or

```bash
roslaunch me5413_world navigation_hybridastar.launch
```

You can check the introductions to these navigation algorithms and results in our report.

## Evaluation

Run the evaluation program in the Analysis folder.
