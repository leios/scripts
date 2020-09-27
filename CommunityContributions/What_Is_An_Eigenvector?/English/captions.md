1
[00:00:00,030 --> 00:00:03,659](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m0s)
hey guys welcome back to another episode

2
[00:00:02,220 --> 00:00:06,500](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m2s)
today we're going to talk about

3
[00:00:03,659 --> 00:00:09,990](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m3s)
something super important to physicists

4
[00:00:06,500 --> 00:00:12,780](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m6s)
eigenvectors so let's draw an XY axis

5
[00:00:09,990 --> 00:00:15,299](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m9s)
with two points on the axis point a and

6
[00:00:12,780 --> 00:00:18,270](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m12s)
point B point a will be in position

7
[00:00:15,299 --> 00:00:21,660](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m15s)
negative 2 negative 2 while point B will

8
[00:00:18,270 --> 00:00:23,750](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m18s)
be in position 2 2 now clearly we can

9
[00:00:21,660 --> 00:00:26,039](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m21s)
draw an arrow from point A to point B

10
[00:00:23,750 --> 00:00:28,470](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m23s)
indicating in which direction and how

11
[00:00:26,039 --> 00:00:31,050](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m26s)
far we need to move in order to get to

12
[00:00:28,470 --> 00:00:32,759](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m28s)
point B from point A and this

13
[00:00:31,050 --> 00:00:34,610](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m31s)
information can be held in a two

14
[00:00:32,759 --> 00:00:36,930](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m32s)
dimensional vector of four four

15
[00:00:34,610 --> 00:00:39,390](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m34s)
indicating we need to move four points

16
[00:00:36,930 --> 00:00:42,629](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m36s)
to the right and four points up in order

17
[00:00:39,390 --> 00:00:44,550](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m39s)
to get to point B these vectors hold a

18
[00:00:42,629 --> 00:00:46,170](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m42s)
lot of information for physicists

19
[00:00:44,550 --> 00:00:49,200](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m44s)
because I tell both the magnitude and

20
[00:00:46,170 --> 00:00:50,940](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m46s)
direction of any given movement now

21
[00:00:49,200 --> 00:00:51,949](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m49s)
let's take a step back and talk about

22
[00:00:50,940 --> 00:00:54,300](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m50s)
something else

23
[00:00:51,949 --> 00:00:56,489](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m51s)
transformation matrices which are ways

24
[00:00:54,300 --> 00:01:00,960](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m54s)
in which we may manipulate vectors into

25
[00:00:56,489 --> 00:01:03,750](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h0m56s)
something entirely new this is done by

26
[00:01:00,960 --> 00:01:06,330](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m0s)
basic matrix multiplication so let's

27
[00:01:03,750 --> 00:01:11,010](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m3s)
take an arbitrary matrix let's say 1/2 0

28
[00:01:06,330 --> 00:01:14,040](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m6s)
2 1 0 0 0 negative 3 and let's take an

29
[00:01:11,010 --> 00:01:16,799](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m11s)
arbitrary vector of let's say 1 1 1 if

30
[00:01:14,040 --> 00:01:20,460](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m14s)
we multiply the matrix by the vector

31
[00:01:16,799 --> 00:01:23,430](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m16s)
will receive the vector 3 3 negative 3

32
[00:01:20,460 --> 00:01:27,570](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m20s)
which is not necessarily related at all

33
[00:01:23,430 --> 00:01:30,630](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m23s)
to the vector we put in of 1 1 1 however

34
[00:01:27,570 --> 00:01:34,380](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m27s)
let's take another vector of let's say 1

35
[00:01:30,630 --> 00:01:37,439](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m30s)
1 0 after matrix multiplication we find

36
[00:01:34,380 --> 00:01:40,439](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m34s)
the vector 3 3 0 which is just 3 times

37
[00:01:37,439 --> 00:01:42,600](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m37s)
the vector of 1 1 0 that we started with

38
[00:01:40,439 --> 00:01:44,939](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m40s)
in this way you can see that after

39
[00:01:42,600 --> 00:01:47,610](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m42s)
matrix multiplication we get the same

40
[00:01:44,939 --> 00:01:50,130](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m44s)
vector out with some sort of scalar

41
[00:01:47,610 --> 00:01:52,470](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m47s)
value being multiplied by it this

42
[00:01:50,130 --> 00:01:55,500](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m50s)
particular vector is known as an

43
[00:01:52,470 --> 00:01:59,820](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m52s)
eigenvector and the number 3 the scale

44
[00:01:55,500 --> 00:02:01,409](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m55s)
value is the eigenvalue in general i

45
[00:01:59,820 --> 00:02:03,960](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h1m59s)
ghen vectors are any vectors which

46
[00:02:01,409 --> 00:02:07,979](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m1s)
satisfy the following equation some

47
[00:02:03,960 --> 00:02:11,160](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m3s)
given matrix a times V equals lambda V

48
[00:02:07,979 --> 00:02:13,350](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m7s)
where V is the eigenvector and lambda

49
[00:02:11,160 --> 00:02:15,390](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m11s)
is the eigenvalue in this way after

50
[00:02:13,350 --> 00:02:17,460](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m13s)
matrix multiplication we get the same

51
[00:02:15,390 --> 00:02:20,820](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m15s)
vector out that we started with with

52
[00:02:17,460 --> 00:02:22,790](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m17s)
some sort of scalar value lambda now

53
[00:02:20,820 --> 00:02:24,990](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m20s)
that helps us understand things more

54
[00:02:22,790 --> 00:02:27,210](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m22s)
mathematically but what if we want to

55
[00:02:24,990 --> 00:02:29,370](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m24s)
understand them more physically well

56
[00:02:27,210 --> 00:02:31,200](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m27s)
let's imagine we have some sort of

57
[00:02:29,370 --> 00:02:33,720](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m29s)
three-dimensional cube and space

58
[00:02:31,200 --> 00:02:35,550](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m31s)
completely filled with points and let's

59
[00:02:33,720 --> 00:02:38,010](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m33s)
take a transformation matrix and

60
[00:02:35,550 --> 00:02:38,700](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m35s)
multiply it by every single vector in

61
[00:02:38,010 --> 00:02:41,190](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m38s)
the cube

62
[00:02:38,700 --> 00:02:42,900](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m38s)
after matrix multiplication you'll see

63
[00:02:41,190 --> 00:02:45,210](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m41s)
that the cube has become something

64
[00:02:42,900 --> 00:02:47,520](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m42s)
entirely new now let's watch that

65
[00:02:45,210 --> 00:02:49,080](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m45s)
transformation one more time except this

66
[00:02:47,520 --> 00:02:51,270](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m47s)
time we're going to draw a line between

67
[00:02:49,080 --> 00:02:53,280](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m49s)
each individual point and all of its

68
[00:02:51,270 --> 00:02:55,820](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m51s)
nearest neighbors so we have some sort

69
[00:02:53,280 --> 00:02:58,260](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m53s)
of three dimensional grid in space

70
[00:02:55,820 --> 00:03:00,960](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m55s)
during this transformation see if you

71
[00:02:58,260 --> 00:03:04,770](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h2m58s)
can find particularly that only stretch

72
[00:03:00,960 --> 00:03:06,660](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m0s)
and do not at all change direction those

73
[00:03:04,770 --> 00:03:08,820](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m4s)
lines that do not change direction are

74
[00:03:06,660 --> 00:03:10,860](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m6s)
eigenvectors and to really drill this

75
[00:03:08,820 --> 00:03:13,320](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m8s)
point home let's take two arbitrary

76
[00:03:10,860 --> 00:03:15,390](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m10s)
points in space and transform them

77
[00:03:13,320 --> 00:03:17,580](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m13s)
you'll see that these two points in

78
[00:03:15,390 --> 00:03:20,160](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m15s)
space move around all over the place but

79
[00:03:17,580 --> 00:03:22,830](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m17s)
if we take a separate pair of points

80
[00:03:20,160 --> 00:03:25,980](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m20s)
that are along an eigenvector you'll see

81
[00:03:22,830 --> 00:03:28,470](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m22s)
that these two only stretch I suppose

82
[00:03:25,980 --> 00:03:31,050](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m25s)
this is even more obvious if we plot all

83
[00:03:28,470 --> 00:03:33,300](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m28s)
three eigenvectors of this particular

84
[00:03:31,050 --> 00:03:36,360](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m31s)
matrix during the transformation along

85
[00:03:33,300 --> 00:03:38,430](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m33s)
with a random pair of points the random

86
[00:03:36,360 --> 00:03:40,680](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m36s)
pair of point is clearly moving around

87
[00:03:38,430 --> 00:03:44,400](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m38s)
all about while the eigenvectors are

88
[00:03:40,680 --> 00:03:47,070](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m40s)
moving just in and out and that is an

89
[00:03:44,400 --> 00:03:49,709](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m44s)
eigenvector in a nutshell a vector that

90
[00:03:47,070 --> 00:03:49,980](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m47s)
after transformation has not changed at

91
[00:03:49,709 --> 00:03:53,250](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m49s)
all

92
[00:03:49,980 --> 00:03:55,569](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m49s)
except by a scalar value known as the

93
[00:03:53,250 --> 00:03:57,629](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m53s)
eigenvalue

94
[00:03:55,569 --> 00:03:57,629](https://www.youtube.com/watch?v=ue3yoeZvt8E#t=0h3m55s)
you

