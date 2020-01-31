This assignment uses three python executable files called as circle.py, square_openloop.py and square_closedloop.py which can be found in src folder of the file assignment2_ws.
To navigate there follow path catkin_ws/src/assignment2_ws/src.

Please run the following commands to in your terminal to run the files:
1. roscore
2. rosrun turtlesim turtlesim_node
3. rosrun assignment2_ws circle.py
4. rosrun assignment2_ws square_openloop.py
5. rosrun assignment2_ws square.closedloop.py

1. circle.py
This file contains code which makes the turtle follow a circle with the given input as the radius of the circle. The turtle first traces a straight line using move.py in turtlesim_cleaner until it reaches the distance of radius and then traces a circle. It then rotates 90 degrees based rotate.py of turtlesim_cleaner. It then takes angular velocity and linear velocity together to trace the circle.

2. square_openloop.py
This code is used to make the turtle move in a square when the given input is the length of a side. It uses move.py code to trace the linear distance and then uses rotate.py to rotate 90 degrees about its axis. It performs this 4 times to complete the entire sqaure. This is executed using a for loop.

3. square_closedloop.py
This code is based out of the gotogoal.py in turtlesim_cleaner package. The only difference is in how the code is executed step by step. 
A new while condition is imposed on the angular constraint. This while condition calculates the desired orientation and the turtle's original orientation and takes the absolute value of it.
Until it reaches a limiting value which is fixed at 0.01 the turtle calculates the new orientation based on the formula arctan(y2-y1/x2-x1) and publishes the angular velocity data to the topic. Once the condition is satisfied it goes on to the original condition of distance less than the given input tolerance.
A for loop is also included to append the co-ordinates of the given user input values to a list. The coordinates are accessed from this list for guiding the turtle.

Please find screenshots of the traced paths in the assignment2_ws with the below names
1. circle.png: Trace of the turtle by giving input as radius as 3.
2. square_openloop: Trace of the turtle by giving input as side as 2.
3. square_closedloop: Trace of the turtle by giving input as co-ordinates.
4. square_closedloop_input: Inputs of the given 5 co-ordinates.
