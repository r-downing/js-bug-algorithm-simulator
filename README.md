# js-bug-algorithm-simulator
Robot simulator that runs bug algorithms. It was built with jQuery and an svg display.

- [js-bug-algorithm-simulator](#js-bug-algorithm-simulator)
- [How it works](#how-it-works)
	- [Right Turn Method](#right-turn-method)
	- [Bug 1](#bug-1)
	- [Bug 2](#bug-2)
- [Simulator](#simulator)

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

## Bug 2

The robot moves toward the goal. If it hits an object, it remembers a line from the robot to the goal. It circles the object until it meets this line again at a place closer to the goal than the point of collision.

![](https://i.imgur.com/hJt5Uae.png)

# Simulator

Click to draw <span style="background-color:blue">obstacle</span> edges. Double-click to finish obstacle. Double-click inside obstacle to remove.

Click and drag to move <span style="background-color:red">robot</span> or <span style="background-color:green">goal</span>.

Right-click to choose an algorithm and run the simulation.

Run simulator below or <a href="#" onClick="MyWindow=window.open('sim.html','MyWindow',width=600,height=400); return false;">open in new window</a>

<iframe src="sim.html" style="width:600px;height:400px"></iframe>

----

[Home](http://ryandowning.net)
