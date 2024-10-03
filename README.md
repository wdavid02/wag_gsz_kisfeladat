# `wag_gsz_kisfeladat` package
ROS 2 python package.  [![Static Badge](https://img.shields.io/badge/ROS_2-Humble-34aec5)](https://docs.ros.org/en/humble/)

## Packages and build

It is assumed that the workspace is `~/ros2_ws/`.

### Clone the packages
``` r
cd ~/ros2_ws/src
```
``` r
git clone https://github.com/wdavid02/wag_gsz_kisfeladat
```

### Build ROS 2 packages
``` r
cd ..
```
``` r
colcon build --packages-select wag_gsz_kisfeladat --symlink-install
```

<details>
<summary> Don't forget to source before ROS commands.</summary>

``` bash
source ~/ros2_ws/install/setup.bash
```
</details>

<details>
<summary> If you don't have Gazebo package.</summary>

``` bash
sudo apt install ros_humble_gazebo_ros_pkgs
```
</details>

Split pane 2 times. In the first pane we start the simulation with the following row:
``` r
ros2 launch wag_gsz_kisfeladat launch_sim.launch.py

```
### Control panel
You'll be able to control the robot with your keyboard
``` r
ros2 run teleop_twist_keyboard teleop_twist_keyboard

```

