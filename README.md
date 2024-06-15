# Environment Toolkit

In pure python, define a 3D grid world and obstacles in that world for robot traversal.\
Good for students who want to learn algorithms and not learn middleware like ROS\
\
Incorporated is an `occupancy_map.py` file that contains an `OccupancyMap` class, which turns\
the Environment that you created into an occupancy grid, allowing to implement graph search algorithms, etc\
\
Look at my [a_star](https://github.com/anthonyn2121/a_star) repo for usage

## Worlds
The Environment class must be initialized with a `dict` and the following 'keys' MUST be valid:
 - bounds: A tuple consisting of `(x_min, x_max, y_min, y_max, z_min, z_max) `that define the grid boundaries
 - blocks: A list of dicts that define objects in the grid world. These are cube shaped objects. These dict MUST
          contain the following keys:
   - position: A tuple consisting of the `(x, y, z)` position of where to start the cube object
   - size: A tuple consisting of `(dx, dy, dz)` which defines how much the cube "grows" along each axis


I find it easy to pre-configure worlds as a json file and load the data in your own scripts.\
See the `worlds/` directory as an example of few pre configured environments 