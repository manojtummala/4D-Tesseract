# 4D-Tesseract
<p align="center"><img src="sketch_4D_Tesseract/Capture3.PNG"></p>

This is a four dimensional cube, otherwise called a hyper-cube or a tesseract. Just note this is technically a tesseract because our screens are two dimensional and cannot hold three dimensional objects. Instead this is just a tesseract projected into three dimensions, and then into two dimensions. Also we are three dimensional creatures, so it is not possible for us to imagine the fourth dimension.

Similar to: https://github.com/manojtummala/Rubicks_Cube... there is a matrix and P4Vector used ... and also P3D(as i am doing in processing).

As it is being projected in 4D first all the points should we connecting to each other then ....its more like simultaneously there exits two cubes and they try to push one to each other everytime..

The co ordinates of the initial cubes are saved in a mtrix and then when they move mostly each cube's co ordinate's exchange... during this the movement of the connection between each edge is displayed to be in 4th Dimension...
```bash
points[0] = new P4Vector(-1, -1, -1, 1);
  points[1] = new P4Vector(1, -1, -1, 1);
  points[2] = new P4Vector(1, 1, -1, 1);
  points[3] = new P4Vector(-1, 1, -1, 1);
  points[4] = new P4Vector(-1, -1, 1, 1);
  points[5] = new P4Vector(1, -1, 1, 1);
  points[6] = new P4Vector(1, 1, 1, 1);
  points[7] = new P4Vector(-1, 1, 1, 1);
  points[8] = new P4Vector(-1, -1, -1, -1);
  points[9] = new P4Vector(1, -1, -1, -1);
  points[10] = new P4Vector(1, 1, -1, -1);
  points[11] = new P4Vector(-1, 1, -1, -1);
  points[12] = new P4Vector(-1, -1, 1, -1);
  points[13] = new P4Vector(1, -1, 1, -1);
  points[14] = new P4Vector(1, 1, 1, -1);
  points[15] = new P4Vector(-1, 1, 1, -1);
  ```
The rotation can take place in direction.. i took **Two directions** 
```bash
float[][] rotationXY = {
      {cos(angle), -sin(angle), 0, 0},
      {sin(angle), cos(angle), 0, 0},
      {0, 0, 1, 0},
      {0, 0, 0, 1}
    };

    float[][] rotationZW = {
      {1, 0, 0, 0},
      {0, 1, 0, 0},
      {0, 0, cos(angle), -sin(angle)},
      {0, 0, sin(angle), cos(angle)}
    };
```
Similarly all the llops are made for the correct iterative rotation and an angle is set.. for me: **angle += 0.02**.
Only in the matrix there are matrix calculations to be performed.

See through the code and try for yourself...

