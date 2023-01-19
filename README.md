# Basic ROS wrapper for Duckietown gym. For more information about ROS template, see the V2 branch. 

This wrapper is based on exercise 26 in the documentation: https://docs.duckietown.org/daffy/duckietown-robotics-development/out/duckietown_simulation.html

## How to use it

### 1 Fork this branch

### 2 Get the Necessary files
Download the files necassary for the ROS wrapper (found in ex 26 in the documentation: https://drive.google.com/file/d/1BU17Gkl5wEjvxv0OtZ2bv5EbcyyH09ZN/view ). 

### 3 Edit the paths in these files to the correct path

### 4 Declare the file simulator_wrapper.py as executable
$ `chmod +x ./packages/simulator_wrapper/src/simulator_wrapper.py`

### 5 Build the image
While being in the template-ros folder, run the `dts devel build -f` command.

### 6 Run docker-compose
Go the the folder where you stored the files of step 2, here is the docker-compose.yaml located. Run the `docker-compose up` command.

### 7 Run 
Open a new terminal, go to the template-ros foler, run the `dts devel run` command.

### 8 Show published images
Open a new terminal, `dts start_gui_tools fakebot`, then run `rqt_image_view` and select the /fakebot/camera_node/image/compressed.

### 9 Use keyboard control
Open a new terminal, run the `dts duckiebot keyboard_control fakebot` command.

## Change map
The costum_map.yaml file can be edited to create a costum map. See the Duckietown-gym for more information and examples. Note that this file can be placed somehwere else. Then you should edit the  map_name='/code/catkin_ws/src/<template-ros>/packages/simulator_wrapper/src/costum_map' in src/simulator_wrapper.py 
