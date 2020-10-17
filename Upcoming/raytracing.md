Today, we are going to begin our journey into raytracing, which is a method used by game designers and 3D animators to create high-quality animations and visual effects.
Though we will end next week with the ability to make images like these, we will focus on the prerequisites this week.
In particular, we will talk about how raytracing models physical light and create a simpe two-dimensional simulation of refraction through a lens and reflaction off a mirror.

So, let's get started by talking a bit about light. *Turn on Lamp*
Firstly, the white light from this lamp is a composite of all the colors of the rainbow.
We can model the light emanating from the lamp as a nearly infinite number of rays moving in all directions, all of which hit different objects before bouncing back into our eyes for us to make sense of the world around us.

For example, let's look at this orange.
Here, some of the light rays from various light sources make their way towards the orange.
The orange then absorbs most of this light, but reflects off orange light.
The orange light from the orange then goes off in a number of different directions, some of which end up in our eye.

**This is essentially the process we are trying to replicate with raytracing. Light leaves a light source, bounces around the room and accrues color from different objects before eventually landing in our eye.**

**When thinking about how to implement this in code, there are a number of important questions to consider:**
1. How we model light propagation? How does light move forward?
2. How does light reflect off of objects?
3. What about transparent objects like water and glass?

For the first point, we will talk about 2 different methods:
1. Timestepping light. This is typically used for simulating how light moves through clouds or smoke... Anything without a hard edge.
2. Event-driven simulations of light. This is where we mathematically determine when each light ray will interact with another object, resulting in less overall computation.

We will be discussing 1 in today's lecture, but 2
is the traditional form of raytracing, which will be done in homework. As a note: there will be a lecture on Thursday on event-driven simulations with something known as a billiard model, which will also set the stage for subsequent lectures.

So, if we were going to timestep light, what would that look like in code?
Well, I typically create a struct for the ray, itself, with the position of the tip of the ray, and a direction.
Both of these will just be vectors with an x and y element inside of them.
In addition, I keep another metric to help me understand the speed at which the ray is moving.
I am going to call this metric an index of refraction or ior in code... but there is a lot of physics hidden in this value that we should probably talk about.

Here's the deal: Light is actually really, really weird, and some of you might have heard that light is simultaneously a wave and a particale and that light moves the same speed regardless of how fast we are moving.
Both of these are 100% correct; however, this lecture lives in the world of computer graphics.
We do not need to care about the wave-like nature of light.
We also assume that our reference frame is not changing.

For us, the speed of light is 3.0e8 m/s... Assuming there is nothing around it.
If light moves inside of something else, like water, for instance, it will be a significant amount slower.
How much slower?
Well, we know from experiments that it is ~1.33 times slower.
This means that the speed of light in water x 1.33 = 3.0e8.
This value is often called an index of refraction, denoted with the character "n".

Air is a special case. Because it's mostly empty space, it's index of refraction is roughly 1, which means the speed of light in air is incredibly close to 3.0e8.

No matter what medium light is moving through, the relationship between the velocities can be given by a simple equation:

c = 3.0e8 = n_{air}v_{air} = n_{water}v_{water}

We'll come back to this later, but here I wanted to drill home the point that if we want to move our light rays forward with time, we need to know their current position, and the velocity at that position, which can be provided with the index of refraction, as

v = c/n

Now, why didn't I use "n" in my code? That's because "n" will be used for something later on.

For now, we can create a simple function to allow our rays to move forward with time, by saying that the new position of each ray will be equal to the old position with it's velocity * some small timestep.
This is the simplest possible form of timestepping, which is an entire field of study unto itself.

Finally, we need to create a main function that creates a bunch of light rays and moves them forward.
Here, I am storing all the values in some large matrix, where each column is an independent ray, and each row is a timestep.
This allows me to easily plot it at the end to create this image.

It's not much to look at now, but don't worry... It gets better.

Now that we have light propagation out of the way, we need to implement the concept of a mirror (show slide with 1 crossed out).
**I'll be honest, most people probably have an intuitive grasp for what mirros do. Light comes from some source, hits the mirror, and then is reflected right into the lens of the camera."

If we were to animate this, we would see light hitting the mirror and then bouncing of like so.
Of course, to put this into code, we need a more mathematical definition, so let's draw a line down the center.

Let's constrain our mirror to be lying horizontally on a table. No matter what ray of light we send onto the mirror, the reflected ray will be moving at the same speed in the x direction, but the opposite speed in the y.

If the mirror is hung on a wall, the opposite is true. The ray will move the same speed in y, but the opposite speed in x.

in both cases, we see that the angle of reflection is always the same angle as it hit the mirror with.
This means as long as we can find that angle, we should be able to find the new, reflected direction, by first finding the component of the velocity we want to flip (cos(theta)*v), and then subtracting it twice to the appropriate direction (v.y -= 2cos(theta)*v).
Note here that the projected vector is pointing perpendicularly outward from the mirror on the line we drew before.
This is why that vector is particularly important and given a special name: the normal.

Ok. It's kinda a weird honor to be called the normal, but it does hold particular importance. Any time we talk about a normal vector, it is simply a vector pointing directly outward from a surface.

If we only consider horizontal and vertical mirrors, we could write some simple code that does the flipping for us, but what about mirrors that are neither horizontal nor vertical?
Well, in these cases, we need to figure out the relative alignment of the ray of light and the mirror, and there is a particular vector operation to do this for us: the dot product.

This operation conceptually returns the amount of one vector projected onto another, so let's look at a concrete example:

Here, we will be taking two vectors, A and B, where b is aligned in the x direction and acts as the vector (1,0). If A and B are the same vector, the dot product will return a 1. If they are perpendicular, it will return a 0. 
As A sweeps between all possible values between those two vectors, we see that the dot product returns only the x component of A.
This is because B is entirely aligned along x.

If B was in some other direction and we performed the same analysis, the dot product would still return the amount of A projected onto B.

In fact, the dot product can also be defined in terms of trigonometric functions as

dot(A,B) = |A||B|cos(theta)

This is why we can directly substitute the dot product in for the reflectivity function we created before.

So, going back to our reflection example, any reflection will simply be:

l .-= 2*dot(ray.l,n)*n

By multiplying by the normal direction at the end, we will always find the amount of the light vector being projected in the direction perpendicular to the surface and then we just subtract it twice to reflect.

Ok, at this point, if we go back to the rays of light from before and put in a tilted mirror, they will all reflect upwards, which is cool.

Now on to the final step: dealing with translucent objects like glass and water.

For this, we need to describe the concept of refraction, a well-loved sibling of reflection.
Essentially, if we send light towards a body of water, the majority of that light will enter the water and tilt a little towards the normal of the surface.
The obvious question is, "how much does it tilt by?"

Well, let's go back a second. When we discussed light propagation, we mentioned that light moves differently depending on the medium it was moving through and we created this equation:

c = 3.0e8 = n_{air}v_{air} = n_{water}v_{water}

By rearranging this equation, we can find that:

n_{air}/n_{water} = v_{water}/v_{air}

There is a rather famous equation called Snell's law that adds to this slightly:

n_{air}/n_{water} = v_{water}/v_{air} = sin(theta_{water})/sin(theta_{air})

So, doing the math, we can see that the angle of the light in water will be

theta_{water} = asin(sin(theta_{air})*n_{air}/n_{water})

and the new direction should be

l_{water} = -n/cos(theta_{water})

If we were to write this in code, it would work just fine; however, trigonometric functions are slow, so we typically like to rewrite everything in the form of vector operations like before.

To do this, we need to figure out how much the new vector has bent towards the normal. This will unfortunately take a lot of math, so let's get started! To start, we can say that...

ior_{water}*l_{water} = ior_{air}*l_{air} + (ior_{air}*cos(theta_{air}) - ior_{water}*cos(theta_{water})*n

where 

(ior_{air}*cos(theta_{air}) - ior_{water}*cos(theta_{water})*n

is a description of the difference between the incoming ray's projection on the normal and the outgoing ray's projection on the normal.

The issue here is that there are not 2 unknowns: l_{water} and theta__{water}, so we need to find some way to get rid of the second theta term.

Using Snell's law, we know that

sin(theta_{water}) = (n_{air}/n_{water})sin(theta_{air}).

We also know that

sin^2(theta) + cos2(theta) = 1

therefore, 

sin(theta_{water}) = (n_{air}/n_{water})sqrt(1-cos(theta_{air})^2))

and

cos(theta_{water} = sqrt(1-sin(theta_{water})^2).

The issue is that dot products are usually defined in terms of cosines, like so...

|l_{air}||n|cos(theta_{air}) = dot(l_{air}, n)
|l_{water}||n|cos(theta_{water}) = dot(l_{water}, n)

Note that because l and n are normalized, they can be ignored.

So we'll want that cos equation to also be in terms of cosines, so

cos(theta_{water}) = sqrt(1-(n_{air}/n_{water})^2(1-cos(theta_{air})^2))

Putting it altogether, we know that the final direction will be...

l_{water} = (n_{air}/n_{water})l_{air}+((n_{air}/n_{water})cos(theta_{air} - cos(theta_{water})*n

For convenience, we usually define

r = ratio = n_{air} / n_{water}

and

c = -dot(n,l_{air})

providing a final relation...

l_{water} = rl_{air}+(rc-sqrt(1-r^2(1-c^2)))

And there you have it!

There is one final note we have to bring up, though. There are some situations where a ray of light will actually reflect from the inside of a medium with a high refractive index. This is called Total Internal Reflection.

Essentially, if the cos(theta_{water}) term is irrational or 0, the light will reflect, and this needs to be taken into account with the refraction function.

That aside, here it is:

With this, we should be able to send our rays of light towards a water surface and see them refract.

Finally, there is only one last thing to do: introduce lenses.

For the purposes of this lecture, we will only target spherical lenses... so think of a giant ball of glass or something.
This will work identically to the water.

We need to find the normal to the surface and refract at that boundary.
Luckily, the normal is easy to find for a sphere (which is part of the reason we are confining this discussion to this shape). It's just the ray's position - the lens's origin after normalization.

There is only one small hitch... What if you are leaving the sphere instead of entering it? Well, in this case, the normal will just go in the opposite direction, so we use the dot product to determine if the normal and light vector are going in opposite directions, and if so, we flip the sign of the returned normal.

That's it.

When we put the lens in the simulation, we should be able to see spherical aberration, which is a semi-focusing event on the far side.

Now, this is still very far from the cool 3d renders you can find online, but to get there, we need to talk about event-driven simulations on thursday. In addition, we will be introducing some naive parallelism later today, which will be used in the next section.

Again, the homework for this week will be priducing this image I have here with an event-driven simulation, and next week we will talk about 3D, color, recursion, and a whole lot more.

Thanks again for watching, and I'll see you next time!


