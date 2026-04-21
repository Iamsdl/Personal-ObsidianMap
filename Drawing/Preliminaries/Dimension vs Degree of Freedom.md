# Dimension
A dimension is the number of directions in which you can "move" from a given point in the world called "origin".
The directions of movement are usually called axes, and movement can be "positive" or "negative". This system is called the "world coordinate system", or "world coordinates" or "global coordinates".
> For the math meaning, see [[/Math/Dimension]]. In math, the "world" is usually called "Space" (Vector Space, Hilbert Space, etc.), but for our purposes the world will be called "**Scene**".
# Degree of Freedom
The degree of freedom is the number of directions in which you can move, but this time starting from a given point on an (geometrical) object, and the movement being limited to/on the object.
> Every object also has its own origin and axes, called the "local coordinate system", or "local coordinates".
# Examples
## 0 Dimensions = 0D
You can't move in any direction. You are left with only the origin point.
## 1D
You can move in one direction (labeled X). With this movement you can create:
- Points = 1D objects with 0 degrees of freedom
- Edges = 1D objects with 1 degree of freedom
> The world of 1D is a line.
## 2D
You can move in two directions (labeled X and Y). With this movement you can create:
- Surfaces = 2D objects with two degrees of freedom (disc = filled circle, filled square, filled rectangle, etc.)
- Paths = 2D objects with only one degree of freedom (edge, circle, square, rectangle, etc.)
> The world of 2D is a plane.
## 3D
You can move in 3 directions (labeled X, Y and Z). With this movement you can create:
- Solids (or just Object but it gets confusing) = 3D objects with three degrees of freedom (filled sphere, filled cube, etc.)
- Surfaces = 3D objects with two degrees of freedom (sphere, cube, etc.)
- Paths = 3D objects with only one degree of freedom (circle, square, maybe edges of a cube, etc)
> The world of 3D is the world, or also called scene.