# ME5413_Final_Project
ME5413 Final Project from Group 16

Authors: Shen Xiaoting, Zeng Jinling, Lei Haoran, Shang Jiajian
# Installation
cd
git clone https://github.com/<YOUR_GITHUB_USERNAME>/ME5413_Final_Project.git
cd ME5413_Final_Project

# Install all dependencies
rosdep install --from-paths src --ignore-src -r -y

# Build
catkin_make
# Source 
source devel/setup.bash
