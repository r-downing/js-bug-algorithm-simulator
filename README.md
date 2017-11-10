# js-bug-algorithm-simulator
Robot simulator that runs bug algorithms with an svg display

# How it works
The robot only has knowledge of three things: the global position of itself, the global position of the goal, and the point at which it is in collision with an obstacle, if any.

## Right Turn Method

With this method, the robot moves straight toward the goal. If it hits an obstacle, it turns right and follows the wall until it has a straight path to the goal again.

![](https://i.imgur.com/albGKkB.png)

This method can fail though...

![](https://i.imgur.com/vXyh83x.png)

## Bug 1

The robot moves toward the goal. If it hits an object, it circumnavigates the object, keeping track of the closest it gets to the goal. Once it has completely circled the object, it returns to the closest point, then proceeds from there.

![](https://i.imgur.com/KQWwbB3.png)

# Simulator

Click to draw <span style="color:blue">obstacle</span> edges. Double-click to finish obstacle. Double-click inside obstacle to remove.

Click and drag to move <span style="color:red">robot</span> or <span style="color:green">goal</span>.

Right-click to choose an algorithm and run the simulation.

<iframe src="sim.html" style="width:600px;height:400px"></iframe>
