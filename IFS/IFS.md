Let's start with a triangle defined by points A, B, and C.
I'll now define 3 functions:

- Function 1 takes a point and returns another halfway towards A
- Function 2 takes a point and returns another halfway towards B
- Function 3 takes a point and returns another halfway towards C

Now I will force points A, B, and C to create 3 offspring, where each child follows another function.
For example, of A's 3 children, one will follow function 1 and stay at A, another will move towards B, and another towards C.
B and C's children will do the same.

This will create a set of points that are equidistant from A, B, and C, and I will force all of these points to have 3 children, following the same rule: each child must follow a different function than it's siblings.
The new kids will then make kids that do the same thing, and those kids will do it again, and again.
Eventually, the pattern becomes clear, showing a rather famous fractal: the Sierpinski triangle.

Essentially, there is a little mathematical magic hidden in this function system that attracts all points towards the shape of the Sierpinski triangle.
There are a large number of function systems we could try here to generate a huge number of different fractally shapes, but we'll focus on the triangle for this video.

The most common method people use to generate fractals with function systems is with a concept known as a "chaos game."
For this process, we start with a random point in space and allow the point to randomly pick any of the three functions it wants.
As long as it only moves according to the 3 prescribed functions, it will eventually wander onto the Sierpinski triangle, and once it lands on the triangle, it cannot leave.

After thousands of iterations, this random sampling method will eventually re-draw the Sierpinski triangle like before.

Essentially, there are a huge number of ways to iterate through this function system and create fractally patterns, and there are a bunch of interesting directions to go from here.
Also, there is a lot more information in the chapter on Iterated Function Systems in the AAA, which is currently awaiting language-specific implementations.

Anyway, that's all for now.
I'll be making a short update video soon to explain where I've been in the past... uh, year?
For now, twitch, discord, and github sponsors links are all in the description.
Thanks for watching and I'll see you next time!
