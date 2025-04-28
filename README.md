# clearpath_simulator
This is a modified version of the [clearpath simulator](https://github.com/clearpathrobotics/clearpath_simulator). Specifically, Humble branch. ROS2 Humble version of clearpath only installs warehouse as default. I gently integrate other worlds, which are readly availabel for ROS2 Jazzy version to ROS2 Humbler version. Enjoy it

Available worlds are:

| World                 | Description                                                                                                            | Screenshots                  | Geographic Location      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|------------------------------|--------------------------|
| `construction`        | The same floorplan as the `office` world, but under construction. Features non-solid walls and debris piles.           | [link](docs/construction.md) | Waterloo ON, Canada      |
| `office`              | The same floorplan as the `construction` world. Features narrow hallways, doorways, meeting rooms, and loading docks.  | [link](docs/office.md)       | Waterloo ON, Canada      |
| `orchard`             | An outdoor, agricultural environment featuring rows of trees. The terrain has small slopes, but is mostly flat.        | [link](docs/orchard.md)      | Nikea, Greece            |
| `pipeline`            | A rugged, outdoor environment featuring steeper hills, a river and bridge, a small cave, solar panels, and a pipeline. | [link](docs/pipeline.md)     | Northern Alberta, Canada |
| `solar_farm`          | An outdoor, agricultural environmentf featuring gentle hills, a barn, rows of solar panels, and fences.                | [link](docs/solar_farm.md)   | Stonewall MB, Canada     |
| `warehouse` (default) | A flat, indoor warehouse environment. Features shelves and people.                                                     | [link](docs/warehouse.md)    | Rio de Janeiro, Brazil   |

## Setup

Prerequisites:
  - Install [ROS 2 Humble](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)

### Ignition Fortress

```
sudo apt-get update && sudo apt-get install wget
sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'
wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
sudo apt-get update && sudo apt-get install ignition-fortress
```

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

