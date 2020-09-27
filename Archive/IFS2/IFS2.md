In the last video, we made an animation of the Sierpinski triangle by allowing points D, E, and F to generate three children that move according to predefined functions.
Those children then had more children, and those children had more children.
The process continued until the Sierpinski triangle was clearly visible.

I want to talk about this animation, in particular, because we *may have* massively over-engineered the problem for fun.
Firstly, let's look at the problem again from the perspective of the trees we are generating.
Every time a new generation of children are born, we increase the number of points in the simulation by 3^{generation number}, thus the number of points grows exponentially.
If each node holds a tuple of the (x,y) location for each point, then the memory footprint also grows exponentially.
The simplest way of creating this animation would be to fully generate the tree we want in the end (in this case up to 4 generations), and then do a Breadth-First Search over the elements.

This would definitely work for the purposes of this video.
We only needed 10 generations at most, so there is no reason *not* to store the whole tree in memory, but you know what they say, "Premature optimization is the root of good video content."
So what would we need to do if we wanted the largest possible Sierpinski triangle animation ever?

Well, let's go back to another fun topic: Huffman encoding.
Here, we were able to uniquely create a code word for each character in a string we would like to encode by traversing through our tree.
Every time we go down the left branch, we add a 0, and when we go down the right, we add a 1.
What if the final string of 1's and 0's was actually a set of functions to apply?

That is to say the string 010 would mean applying f_0, f_1, and f_0 to our root node's location.

Well, in this case, each node would not need to keep a location, but instead a set of function pointers or a bit string that can be interpreted into a set of function pointers.
More than that, because we have a set of three functions for this animation, we could not use bits, but instead would need to use base-3 bits, sometimes called trits, in a bijective 3-based number system.
This simply means that our counting would need to look like this, not this.

This doesn't really help us yet, but it would allow for us to do a series of Depth-First Searches to emulate a Breadth-First Search.
We could, for example, say we want to do a Depth-First search and only return trit-strings at a certain level depth.
This is cool, but I am used to the world of GPUs, which have essentially no recursion depth.
Also, we want to do a Breadth-First Search, and if we are over-engineering the problem, we might as well fully over-engineer it, right?
No cheating with Depth-First Searches.

So the trick here is that a Breadth-First Search for this tree is actually just counting in bijective base 3 trit space.
This means that instead of having to keep a tree, we just need to keep a trit string and increment it by one each time, then interpret each trit string as a series of functions to implement to find the new location of each child.
So that's what we did.

We ended up having to do some fancy bit logic to get our bits to act as trits, but it all worked out in the end.
The code shown here was actually written by Kroppeb on stream.
Honestly, it's really cool, but might need it's own video to fully describe.

After we created a trit number system for the triangle, we then did the same for the square to create this animation and called it quits.
In general, if you use a bijective, base n number system, you should be able to do a BFS of a full n-ary tree by simply counting.
The neat thing about this particular case is that now the memory footprint grows linearly with the number of levels, not exponentially.
Admittedly, the computation required for each point goes way, way up, but that'sa fair price to pay for minimizing memory.
As a note, I *think* this is the minimum amount of space necessary to do a BFS of an n-ary tree without resorting to DFS shenanigans.
Feel free to discuss this further in the comment section or on discord!

I very rarely show my process here on YouTube and instead leave that for twitch.
If you are interested in more videos like this, please let me know!
This particular animation incorporated Tree Traversal, Huffman Encoding, bit logic, and Iterated Function Systems, which are all topics we have covered in the past and are both on YouTube and the algorithm archive.
We have done a bunch of tricky animations over the years, which have lead to some pretty interesting discussions and community interactions, so I have a lot of material to work with here if you want more videos of this type.

Anyway, that's all for now.
Twitch, discord and GitHub sponsors links are all in the description.
I decided for GitHub sponsors instead of Patreon for 2 reasons:
1. Github will match any contributions, so if you pledge $1 to the algorithm archive, you are actually providing $2.
2. This is a programming project and I want to reflect that and support the open source ecosystem in the best way I can.

I am not asking you to donate, but if you like the content, please consider it!
Thanks again for watching, and I'll see you next time!
