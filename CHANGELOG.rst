^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package costmap_converter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.5 (2016-02-01)
------------------
* Major changes regarding the line detection based on the convex hull
  (it should be much more robust now).
* Concave hull plugin added.
* The cluster size can now be limited from above using a specific parameter.
  This implicitly avoids large clusters forming a 'L' or 'U'.
* All parameters can now be adjusted using dynamic_reconfigure (rqt_reconfigure).
* Some parameter names changed.
* Line plugin based on ransac: line inliers must now be placed inbetween the start and end of a line.

0.0.4 (2016-01-11)
------------------
* Fixed conversion from map to world coordinates if the costmap is not quadratic.

0.0.3 (2015-12-23)
------------------
* The argument list of the initialize method requires a nodehandle from now on. This facilitates the handling of parameter namespaces for multiple instantiations of the plugin.
* This change is pushed immediately as a single release to avoid API breaks (since version 0.0.2 is not on the official repos up to now).

0.0.2 (2015-12-22)
------------------
* Added a plugin for converting the costmap to lines using ransac

0.0.1 (2015-12-21)
------------------
* First release of the package including a pluginlib interface, two plugins (costmap to polygons and costmap to lines) and a standalone conversion node.

