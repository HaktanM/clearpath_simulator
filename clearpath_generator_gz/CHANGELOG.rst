^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package clearpath_generator_gz
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.3.0 (2025-04-15)
------------------
* Add Ouster (`#68 <https://github.com/clearpathrobotics/clearpath_simulator/issues/68>`_)
* Feature: MoveIt Parameters and Enable (`#70 <https://github.com/clearpathrobotics/clearpath_simulator/issues/70>`_)
* Contributors: Luis Camero

1.0.0 (2024-11-25)
------------------
* Added minimum version.
* Contributors: Tony Baltovski

0.3.0 (2024-09-19)
------------------
* Removed prefix_launch_arg no longer used
* Add ridgeback
* Fixed change log order
* Added manipulators to generator and spawn
* Contributors: Luis Camero

0.2.6 (2024-07-25)
------------------
* Add gz image transport for cameras
* IMU data raw remap
* Generate gazebo bridge config parameters
* Removed bridging using remappings and arguments
* Contributors: Luis Camero

0.2.5 (2024-05-28)
------------------
* Added Zed to simulator
* Contributors: Luis Camero

0.2.4 (2024-04-15)
------------------

0.2.3 (2024-01-18)
------------------
* Removed print
* Removed namespaced tf_static
* 0.2.2
* Changes.
* 0.2.1
* Changes.
* Added all dingo to generator
* 0.2.0
* Changes.
* Added Warthog and Dingo to generator
* Added Generic robot components
* Sensor static tf should use robot namespace
* Contributors: Luis Camero, Roni Kreinin, Tony Baltovski, luis-camero

0.2.2 (2024-01-15)
------------------

0.2.1 (2023-12-11)
------------------
* Added all dingo to generator
* Contributors: Luis Camero

0.2.0 (2023-12-08)
------------------
* Added Warthog and Dingo to generator
* Added Generic robot components
* Sensor static tf should use robot namespace
* Contributors: Luis Camero, Roni Kreinin

0.1.3 (2023-11-03)
------------------

0.1.2 (2023-10-04)
------------------
* Initial addition of Blackfly (`#19 <https://github.com/clearpathrobotics/clearpath_simulator/issues/19>`_)
  * Initial addition of Blackfly
* Contributors: Hilary Luo

0.1.1 (2023-08-25)
------------------
* Linting
* Added additional supported IMUs and GPSs
* Fix imu and gps bridge topic remapping
* Remove static tf nodes, no longer necessary
* Update topic names to match other packages
* Contributors: Hilary Luo

0.1.0 (2023-08-17)
------------------
* Renamed UST10 to UST
* Contributors: Roni Kreinin

0.0.3 (2023-07-24)
------------------
* Linting
* Added prefix launch arg for A200
* Updated param generator 'use_sim_time' implementation
* Launch generator cleanup
* Contributors: Roni Kreinin

0.0.2 (2023-07-13)
------------------
* Updated imports and getters
* Contributors: Luis Camero

0.0.1 (2023-07-05)
------------------
* Changed colour to color
* Added dependencies.repos
  Updated topic names to match API
* Support for empty namespace
  Generate tf and cmd_vel bridges
* Namespacing support
* Renamed clearpath_simulator to clearpath_gz
  clearpath_simulator is now a metapackage
  Added clearpath_generator_gz
* Contributors: Roni Kreinin
