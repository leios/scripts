1
[00:00:00,030 --> 00:00:02,030](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m0s)
Let's go back to the basics

2
[00:00:02,200 --> 00:00:10,139](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m2s)
Determinants, let's take a Matrix of [one] [two] [zero] [two] [one] [zero] [zero] [zero] negative [three] and let's use this matrix to

3
[00:00:10,139 --> 00:00:17,849](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m10s)
Transform every vertex on a unit cube of length width and height one aligned along the xy and z axes

4
[00:00:18,250 --> 00:00:19,199](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m18s)
after transformation

5
[00:00:19,199 --> 00:00:25,079](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m19s)
You'll see that we have a completely different object than we had before but now I have a bit of a question

6
[00:00:25,480 --> 00:00:27,900](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m25s)
How much larger is this new?

7
[00:00:28,510 --> 00:00:29,830](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m28s)
Transformed object

8
[00:00:29,830 --> 00:00:37,110](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m29s)
We could solve this problem with numerical integration by encapsulating both objects in a larger Cube and performing Monte Carlo integration

9
[00:00:37,870 --> 00:00:44,700](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m37s)
[after] integration we [can] say that the larger object is about nine times bigger than the unit Cube now

10
[00:00:44,700 --> 00:00:46,889](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m44s)
Let's think of this problem a little differently

11
[00:00:47,230 --> 00:00:51,360](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m47s)
During Matrix Transformation most vectors will stretch and rotate

12
[00:00:51,550 --> 00:00:58,980](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m51s)
however there are certain vectors that only stretch and do not at all change direction these vectors are known as

13
[00:00:59,440 --> 00:01:07,409](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h0m59s)
Eigenvectors and the amounts by which they stretch are known as eigenvalues if we align the sides of our unit cube along these

14
[00:01:07,780 --> 00:01:11,939](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m7s)
Eigenvectors and perform a matrix transformation on each vertex in the Cube

15
[00:01:11,970 --> 00:01:15,479](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m11s)
We'll find a rectangular prism that has not been skewed at all

16
[00:01:15,880 --> 00:01:21,839](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m15s)
This makes finding the ratio between the new Transformed object and the original unit Cube kind of trivial

17
[00:01:22,030 --> 00:01:28,559](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m22s)
It's simply the length times width times height of the new tuborg now because we allow the unit Cube along

18
[00:01:29,440 --> 00:01:36,580](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m29s)
Eigenvectors and each side of the unit cube is of length one, After transformation the new length width and height are all

19
[00:01:37,080 --> 00:01:40,940](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m37s)
Eigenvalues, So how much bigger is the object after transformation?

20
[00:01:41,560 --> 00:01:48,320](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m41s)
Well, it's simply a product of all of the eigenvalues which in this case is exactly nine here

21
[00:01:48,329 --> 00:01:54,179](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m48s)
I suppose it makes sense that any objects volume will increase by the amount of stretching in each dimension

22
[00:01:54,909 --> 00:02:00,118](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h1m54s)
Which is exactly what we said before the new volume is a product of the eigenvalues

23
[00:02:00,939 --> 00:02:07,709](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m0s)
Now at this point you might be thinking [that] we're pretty clever, but math magicians have at least one more trick up their sleeve

24
[00:02:08,679 --> 00:02:10,479](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m8s)
Determinants, so let's do it

25
[00:02:10,479 --> 00:02:12,958](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m10s)
Let's find the Determinant of our transformation Matrix

26
[00:02:13,390 --> 00:02:18,660](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m13s)
it will be 1 times 1 times [negative] 3 minus 0 times 0

27
[00:02:19,569 --> 00:02:27,208](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m19s)
subtracting 2 times 2 times negative 3 minus 0 times 0 plus 0 times 2 Times 0

28
[00:02:27,520 --> 00:02:31,919](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m27s)
minus 1 times 0 which is equal to negative 3 plus 12 or

29
[00:02:33,010 --> 00:02:40,620](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m33s)
exactly not the same as we saw before and that's that a simple Determinant can be determined by

30
[00:02:41,019 --> 00:02:43,019](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m41s)
[comparing] the new to the old

31
[00:02:48,280 --> 00:02:50,280](https://www.youtube.com/watch?v=vvR3JSXO2fo#t=0h2m48s)
Thanks for watching and I'll [see] you [next] time

