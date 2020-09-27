Let's start with a triangle defined by points A, B, and C.
I'll now define 3 functions:

- Function 1 takes a point and returns another halfway towards A
- Function 2 takes a point and returns another halfway towards B
- Function 3 takes a point and returns another halfway towards C

Now, I will create 3 new points.
D will be midway between A and B, E will be midway between B and C, and F will be midway between C and A.

I will now force all three of these new points to generate 3 children, each of which will choose a specific function to follow that is different than it's siblings.
That is to say, exactly one child from each parent will move towards A, B, or C.
I will force all of these new points to have 3 children, following the same rules.
Those new kids will then again make kids that do the same thing, and those kids will do it again, and again.
Eventually, the pattern becomes clear, showing a rather famous fractal: the Sierpinski triangle.

Essentially, there is a little mathematical magic hidden in this function system that attracts all points towards the shape of the Sierpinski triangle.
There are a large number of function systems we could try here to generate a huge number of different fractally shapes, but we'll focus on the triangle for this video.

The most common method people use to generate fractals with function systems is with a concept known as a "chaos game."
For this process, we start with a random point in space and allow the point to randomly pick any of the three functions it wants.
As long as it only moves according to the 3 prescribed functions, it will eventually wander onto the Sierpinski triangle, and once it lands on the triangle, it cannot leave.

Now, if we ignore the first 20 points or so of this simulation and then run it for thousands of iterations, this random sampling method will eventually re-draw the Sierpinski triangle like before.
It's somewhat remarkable how roughly 10 lines of code can generate such an interesting set of shapes.

Essentially, there are a huge number of ways to iterate through this function system and other systems like it to create fractally patterns, and there are a bunch of interesting directions to go from here.
Also, there is a lot more information in the chapter on Iterated Function Systems in the AAA, which is currently awaiting language-specific implementations.
In that chapter, there is a small teaser for another interesting topic: restricted chaos games, which leads us down a huge rabbit-hole eventually ending up with fractal flames, which are downright amazing, but again... a topic for another time.

Anyway, that's all for now.
I'll be making a short update video soon to explain where I've been in the past... uh, year?
For now, twitch, discord, and github sponsors links are all in the description.
Thanks for watching and I'll see you next time!
