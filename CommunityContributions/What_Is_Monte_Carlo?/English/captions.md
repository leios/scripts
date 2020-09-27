1
[00:00:00,030 --> 00:00:06,330](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m0s)
let's talk about some programming magic

2
[00:00:02,550 --> 00:00:09,870](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m2s)
Monte Carlo integration let's start with

3
[00:00:06,330 --> 00:00:12,300](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m6s)
the question what is an integral well if

4
[00:00:09,870 --> 00:00:14,759](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m9s)
we draw an XY axis and a single line

5
[00:00:12,300 --> 00:00:17,670](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m12s)
across the axis following the equation y

6
[00:00:14,759 --> 00:00:20,609](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m14s)
equals x the integral is simply the area

7
[00:00:17,670 --> 00:00:23,939](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m17s)
under the curve or the area within this

8
[00:00:20,609 --> 00:00:26,010](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m20s)
shaded triangular region we know from

9
[00:00:23,939 --> 00:00:28,380](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m23s)
basic calculus that the integral of this

10
[00:00:26,010 --> 00:00:30,539](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m26s)
equation is one-half x squared which

11
[00:00:28,380 --> 00:00:33,210](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m28s)
looks suspiciously like the area of a

12
[00:00:30,539 --> 00:00:35,790](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m30s)
triangle as 1/2 base times height in

13
[00:00:33,210 --> 00:00:38,700](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m33s)
fact if the base is X and the height is

14
[00:00:35,790 --> 00:00:41,579](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m35s)
also X then the area of a triangle is

15
[00:00:38,700 --> 00:00:44,070](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m38s)
exactly the same as the integral of this

16
[00:00:41,579 --> 00:00:46,410](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m41s)
equation so let's think of this problem

17
[00:00:44,070 --> 00:00:49,110](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m44s)
a little differently instead of an XY

18
[00:00:46,410 --> 00:00:51,920](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m46s)
axis with the line on the axis let's

19
[00:00:49,110 --> 00:00:53,579](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m49s)
imagine a box with width and height X

20
[00:00:51,920 --> 00:00:55,980](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m51s)
inside of this box

21
[00:00:53,579 --> 00:00:59,160](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m53s)
let's embed the same triangle we saw

22
[00:00:55,980 --> 00:01:01,590](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m55s)
before now obviously the area of the box

23
[00:00:59,160 --> 00:01:03,899](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h0m59s)
is simply the base times the height or x

24
[00:01:01,590 --> 00:01:06,570](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m1s)
squared an area of the triangle within

25
[00:01:03,899 --> 00:01:09,570](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m3s)
the box takes up half the space so it's

26
[00:01:06,570 --> 00:01:12,420](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m6s)
1/2 of the area of the box or 1/2 x

27
[00:01:09,570 --> 00:01:14,220](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m9s)
squared this is great it means that we

28
[00:01:12,420 --> 00:01:16,500](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m12s)
can find the area of any arbitrary

29
[00:01:14,220 --> 00:01:18,810](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m14s)
object within the square so long as we

30
[00:01:16,500 --> 00:01:22,080](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m16s)
know the ratio of how filled the square

31
[00:01:18,810 --> 00:01:24,180](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m18s)
is by the arbitrary object so now we

32
[00:01:22,080 --> 00:01:27,390](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m22s)
have a question how exactly do we

33
[00:01:24,180 --> 00:01:29,159](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m24s)
calculate that value of 1/2 well in this

34
[00:01:27,390 --> 00:01:30,570](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m27s)
case it's easy we simply take the area

35
[00:01:29,159 --> 00:01:35,130](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m29s)
of the triangle and divide it by the

36
[00:01:30,570 --> 00:01:37,020](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m30s)
area of the box but wait we're looking

37
[00:01:35,130 --> 00:01:39,750](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m35s)
for the area of the triangle so we can't

38
[00:01:37,020 --> 00:01:42,720](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m37s)
exactly use that there must some other

39
[00:01:39,750 --> 00:01:45,390](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m39s)
way to calculate this ratio monte-carlo

40
[00:01:42,720 --> 00:01:47,520](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m42s)
solution to this problem is random the

41
[00:01:45,390 --> 00:01:49,380](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m45s)
sampling the idea is that if we take a

42
[00:01:47,520 --> 00:01:51,000](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m47s)
whole bunch of points in the box and we

43
[00:01:49,380 --> 00:01:52,860](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m49s)
divide the number of points that fall

44
[00:01:51,000 --> 00:01:55,829](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m51s)
within the triangle by the total number

45
[00:01:52,860 --> 00:01:58,500](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m52s)
of points used in the box we should find

46
[00:01:55,829 --> 00:02:01,860](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m55s)
that ratio of the areas necessary to

47
[00:01:58,500 --> 00:02:03,509](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h1m58s)
compute the integral so let's try it out

48
[00:02:01,860 --> 00:02:04,250](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m1s)
I'm going to plot a whole bunch of

49
[00:02:03,509 --> 00:02:06,650](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m3s)
random

50
[00:02:04,250 --> 00:02:09,259](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m4s)
within the box and afterwards you'll see

51
[00:02:06,650 --> 00:02:12,370](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m6s)
that 17 fall within the triangle and a

52
[00:02:09,259 --> 00:02:15,410](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m9s)
total of 36 fall within the entire box

53
[00:02:12,370 --> 00:02:18,410](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m12s)
now I guess that ratio isn't quite

54
[00:02:15,410 --> 00:02:20,090](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m15s)
one-half but it's pretty close this

55
[00:02:18,410 --> 00:02:23,330](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m18s)
highlights something important about the

56
[00:02:20,090 --> 00:02:26,510](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m20s)
Monte Carlo algorithm it is inherently

57
[00:02:23,330 --> 00:02:28,340](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m23s)
random that said the more random points

58
[00:02:26,510 --> 00:02:30,980](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m26s)
we take the better our approximation

59
[00:02:28,340 --> 00:02:32,000](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m28s)
becomes so let's draw a square and

60
[00:02:30,980 --> 00:02:35,030](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m30s)
inside of the square

61
[00:02:32,000 --> 00:02:37,370](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m32s)
let's embed a circle now let's perform a

62
[00:02:35,030 --> 00:02:39,830](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m35s)
Monte Carlo algorithm to find the area

63
[00:02:37,370 --> 00:02:42,620](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m37s)
of the circle with one three or seven

64
[00:02:39,830 --> 00:02:44,900](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m39s)
points the approximate area is quite 4

65
[00:02:42,620 --> 00:02:46,820](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m42s)
but as we increase the total number of

66
[00:02:44,900 --> 00:02:49,130](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m44s)
points to thousands upon thousands

67
[00:02:46,820 --> 00:02:52,000](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m46s)
eventually the approximate area becomes

68
[00:02:49,130 --> 00:02:54,350](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m49s)
incredibly close to that of a circle as

69
[00:02:52,000 --> 00:02:56,959](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m52s)
indicated by the low percent error at

70
[00:02:54,350 --> 00:02:59,360](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m54s)
the bottom of the screen and that was

71
[00:02:56,959 --> 00:03:02,060](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m56s)
our first real Monte Carlo simulation

72
[00:02:59,360 --> 00:03:03,590](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h2m59s)
but the true power of the Monte Carlo

73
[00:03:02,060 --> 00:03:06,170](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m2s)
algorithm comes from the fact that we

74
[00:03:03,590 --> 00:03:09,260](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m3s)
can now integrate somewhat arbitrary and

75
[00:03:06,170 --> 00:03:11,600](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m6s)
misbehaved functions for example the bat

76
[00:03:09,260 --> 00:03:13,610](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m9s)
symbol now here things were done a

77
[00:03:11,600 --> 00:03:16,760](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m11s)
little bit differently instead of an

78
[00:03:13,610 --> 00:03:19,489](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m13s)
exterior square we use an exterior over

79
[00:03:16,760 --> 00:03:21,380](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m16s)
and the interior is quite obviously the

80
[00:03:19,489 --> 00:03:23,030](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m19s)
Batman curve for which there will be a

81
[00:03:21,380 --> 00:03:25,340](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m21s)
link in the description for more

82
[00:03:23,030 --> 00:03:27,980](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m23s)
information and there you have it the

83
[00:03:25,340 --> 00:03:33,830](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m25s)
Monte Carlo algorithm arbitrary shapes

84
[00:03:27,980 --> 00:03:37,180](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m27s)
random numbers real results thanks for

85
[00:03:33,830 --> 00:03:37,180](https://www.youtube.com/watch?v=AyBNnkYrSWY#t=0h3m33s)
watching and I'll see you next time

