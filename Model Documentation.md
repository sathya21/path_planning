# Reflection

##

1) Use the sensor fusion and check if the car is too close to the car in front, left or right

2) If the car is too close to the car in front and there are no cars to the left, then set the lane to left lane. Else, if there is no car to the right, then set the lane to right lane

3) Reduce the acceleration gradually when the  car is too close to a car in front.

4) Increase the acceleration gradually when the no car is in front and the speed is within the permissible speed limit. This will avoid the jerk


5) Use Previous path of the car to get last two points,  if there is no previous path, then use the angle of the car and its current x,y co ordinates and create two previous points
   
   
6) Create 3 more points spaced 30m apart at 30m,60m and 90m.

7) transform all the 5 points to car's local coordinates

8) Use these 5 points and create a spline

9) Use the previous remaining path and push it into the next vals 

10) Get the remaining  points using spline and push it into the next vals after converting to the global coordinates


This will ensure a smooth path planning with the following charateristics

- No Speed limit violation
- No Jerk
- Smoother acceleration
- No collisions







