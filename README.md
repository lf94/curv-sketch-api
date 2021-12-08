# Sketch API for Curv

A sketching API is useful in an engineering context because it mimics that of
what would be done on a blueprint. They convey exactly what's needed in a simple
way.

A benefit to sketching is it lends itself well to parametricity, since each
function's argument can be adjusted very easily and affect all subsequent 
functions.

This sketching API is based around CADQuery's. Things like selectors and assembly
will be missing. They may never be added.

Below is a list of CADQuery sketching function which will be implemented over time:

|Function                                   | Description |
--------------------------------------------|-------------
| [x] `center(x, y)                         ` | Shift local coordinates to the specified location.                                                                                    |
| [x] `lineTo(x, y[, forConstruction])      ` | Make a line from the current point to the provided point                                                                              |
| [x] `line(xDist, yDist[, forConstruction])` | Make a line from the current point to the provided point, using dimensions relative to the current point                              |
| [x] `vLine(distance[, forConstruction])   ` | Make a vertical line from the current point the provided distance                                                                     |
| [x] `vLineTo(yCoord[, forConstruction])   ` | Make a vertical line from the current point to the provided y coordinate.                                                             |
| [x] `hLine(distance[, forConstruction])   ` | Make a horizontal line from the current point the provided distance                                                                   |
| [x] `hLineTo(xCoord[, forConstruction])   ` | Make a horizontal line from the current point to the provided x coordinate.                                                           |
| [x] `polarLine(distance, angle[, …])      ` | Make a line of the given length, at the given angle from the current point                                                            |
| [x] `polarLineTo(distance, angle[, …])    ` | Make a line from the current point to the given polar coordinates                                                                     |
| [x] `moveTo([x, y])                       ` | Move to the specified point, without drawing.                                                                                         |
| [x] `move([xDist, yDist])                 ` | Move the specified distance from the current point, without drawing.                                                                  |
| [ ] `spline(listOfXYTuple[, tangents, …]) ` | Create a spline interpolated through the provided points (2D or 3D).                                                                  |
| [ ] `parametricCurve(func[, N, start, …]) ` | Create a spline curve approximating the provided function.                                                                            |
| [ ] `parametricSurface(func[, N, …])      ` | Create a spline surface approximating the provided function.                                                                          |
| [ ] `threePointArc(point1, point2[, …])   ` | Draw an arc from the current point, through point1, and ending at point2                                                              |
| [ ] `sagittaArc(endPoint, sag[, …])       ` | Draw an arc from the current point to endPoint with an arc defined by the sag (sagitta).                                              |
| [ ] `radiusArc(endPoint, radius[, …])     ` | Draw an arc from the current point to endPoint with an arc defined by the radius.                                                     |
| [ ] `tangentArcPoint(endpoint[, …])       ` | Draw an arc as a tangent from the end of the current edge to endpoint.                                                                |
| [ ] `mirrorY()                            ` | Mirror entities around the y axis of the workplane plane.                                                                             |
| [ ] `mirrorX()                            ` | Mirror entities around the x axis of the workplane plane.                                                                             |
| [ ] `wire([forConstruction])              ` | Returns a CQ object with all pending edges connected into a wire.                                                                     |
| [ ] `rect(xLen, yLen[, centered, …])      ` | Make a rectangle for each item on the stack.                                                                                          |
| [ ] `circle(radius[, forConstruction])    ` | Make a circle for each item on the stack.                                                                                             |
| [ ] `ellipse(x_radius, y_radius[, …])     ` | Make an ellipse for each item on the stack.                                                                                           |
| [ ] `ellipseArc(x_radius, y_radius[, …])  ` | Draw an elliptical arc with x and y radiuses either with start point at current point or or current point being the center of the arc |
| [ ] `polyline(listOfXYTuple[, …])         ` | Create a polyline from a list of points                                                                                               |
| [ ] `close()                              ` | End 2D construction, and attempt to build a closed wire.                                                                              |
| [ ] `rarray(xSpacing, ySpacing, xCount, …)` | Creates an array of points and pushes them onto the stack.                                                                            |
| [ ] `polarArray(radius, startAngle, …)    ` | Creates an polar array of points and pushes them onto the stack.                                                                      |
| [ ] `slot2D(length, diameter[, angle])    ` | Creates a rounded slot for each point on the stack.                                                                                   |
| [ ] `offset2D(d[, kind, forConstruction]) ` | Creates a 2D offset wire.                                                                                                             |
