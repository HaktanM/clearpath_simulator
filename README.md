# clearpath_simulator
This is a customized version of the [clearpath simulator](https://github.com/clearpathrobotics/clearpath_simulator) tailored for ROS2 Humble. The default installation for ROS2 Humble only includes the warehouse world as built in, but I have added several other worlds that were originally available for the ROS2 Jazzy version.

Available worlds are:

| World                 | Description                                                                                                            | Screenshots                  | Geographic Location      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|------------------------------|--------------------------|
| `construction`        | The same floorplan as the `office` world, but under construction. Features non-solid walls and debris piles.           | [link](https://github.com/clearpathrobotics/clearpath_simulator/blob/jazzy/docs/construction.md) | Waterloo ON, Canada      |
| `office`              | The same floorplan as the `construction` world. Features narrow hallways, doorways, meeting rooms, and loading docks.  | [link](https://github.com/clearpathrobotics/clearpath_simulator/blob/jazzy/docs/office.md)       | Waterloo ON, Canada      |
| `orchard`             | An outdoor, agricultural environment featuring rows of trees. The terrain has small slopes, but is mostly flat.        | [link](https://github.com/clearpathrobotics/clearpath_simulator/blob/jazzy/docs/orchard.md)      | Nikea, Greece            |
| `pipeline`            | A rugged, outdoor environment featuring steeper hills, a river and bridge, a small cave, solar panels, and a pipeline. | [link](https://github.com/clearpathrobotics/clearpath_simulator/blob/jazzy/docs/pipeline.md)     | Northern Alberta, Canada |
| `solar_farm`          | An outdoor, agricultural environmentf featuring gentle hills, a barn, rows of solar panels, and fences.                | [link](https://github.com/clearpathrobotics/clearpath_simulator/blob/jazzy/docs/solar_farm.md)   | Stonewall MB, Canada     |
| `warehouse` (default) | A flat, indoor warehouse environment. Features shelves and people.                                                     | [link](https://github.com/clearpathrobotics/clearpath_simulator/blob/jazzy/docs/warehouse.md)    | Rio de Janeiro, Brazil   |

## Setup

Prerequisites:
  - Install [ROS 2 Humble](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)
  - Install [Gazebo Ignition Fortress](https://gazebosim.org/docs/fortress/install/)

### Workspace
```
mkdir ~/clearpath_ws/src -p
cd ~/clearpath_ws/src
git clone https://github.com/clearpathrobotics/clearpath_simulator.git
cd ~/clearpath_ws
rosdep install -r --from-paths src -i -y
colcon build --symlink-install
```

### Setup path
```
mkdir ~/clearpath
```

Copy your `robot.yaml` into `~/clearpath`

## Launch
```
ros2 launch clearpath_gz simulation.launch.py
```

