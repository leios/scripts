1
[00:00:00,030 --> 00:00:04,560](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m0s)
if you drop a ball from five meters how

2
[00:00:01,979 --> 00:00:06,180](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m1s)
long does it take to hit the ground this

3
[00:00:04,560 --> 00:00:08,370](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m4s)
is one of my favorite questions to ask

4
[00:00:06,180 --> 00:00:10,710](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m6s)
beginner programmers because it has an

5
[00:00:08,370 --> 00:00:13,139](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m8s)
analytical solution let's start with the

6
[00:00:10,710 --> 00:00:15,929](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m10s)
kinematic equation x equals X naught

7
[00:00:13,139 --> 00:00:19,080](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m13s)
plus V naught T plus 1/2 a t-square plus

8
[00:00:15,929 --> 00:00:21,600](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m15s)
1/6 BT cubed and higher-order terms if

9
[00:00:19,080 --> 00:00:23,400](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m19s)
we assume that our initial velocity is 0

10
[00:00:21,600 --> 00:00:25,080](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m21s)
that no one cares about our V term

11
[00:00:23,400 --> 00:00:27,930](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m23s)
because it's a jerk our final position

12
[00:00:25,080 --> 00:00:29,460](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m25s)
is 0 our initial position is 5 and that

13
[00:00:27,930 --> 00:00:31,980](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m27s)
we have an acceleration that is roughly

14
[00:00:29,460 --> 00:00:33,390](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m29s)
negative 10 meters per second squared we

15
[00:00:31,980 --> 00:00:35,640](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m31s)
can solve for T and find that it's

16
[00:00:33,390 --> 00:00:37,380](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m33s)
roughly 1 second because of how

17
[00:00:35,640 --> 00:00:39,000](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m35s)
straightforward this is whenever I have

18
[00:00:37,380 --> 00:00:41,489](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m37s)
a new algorithm to solve Newton's

19
[00:00:39,000 --> 00:00:44,190](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m39s)
equations of motion this is my favorite

20
[00:00:41,489 --> 00:00:46,140](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m41s)
test case that said we don't really need

21
[00:00:44,190 --> 00:00:47,610](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m44s)
anything special to figure out how long

22
[00:00:46,140 --> 00:00:49,520](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m46s)
it takes for a ball to hit the ground

23
[00:00:47,610 --> 00:00:53,340](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m47s)
when dropped under constant acceleration

24
[00:00:49,520 --> 00:00:55,050](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m49s)
however what if our acceleration is no

25
[00:00:53,340 --> 00:00:56,960](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m53s)
longer constant but instead a function

26
[00:00:55,050 --> 00:00:59,670](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m55s)
of position which is a function of time

27
[00:00:56,960 --> 00:01:01,079](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m56s)
imagine for example an asteroid moving

28
[00:00:59,670 --> 00:01:03,420](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h0m59s)
through multiple planets gravitational

29
[00:01:01,079 --> 00:01:05,369](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m1s)
field well in this case we're going to

30
[00:01:03,420 --> 00:01:07,200](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m3s)
have to rethink how we implement this in

31
[00:01:05,369 --> 00:01:09,180](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m5s)
code and here's where for lay

32
[00:01:07,200 --> 00:01:11,220](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m7s)
integration comes in we want to find the

33
[00:01:09,180 --> 00:01:13,380](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m9s)
trajectory of some object influenced by

34
[00:01:11,220 --> 00:01:15,000](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m11s)
some force field so we start with the

35
[00:01:13,380 --> 00:01:17,270](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m13s)
object's position and try to find its

36
[00:01:15,000 --> 00:01:19,080](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m15s)
new position one time step in the future

37
[00:01:17,270 --> 00:01:21,119](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m17s)
obviously this follows from the

38
[00:01:19,080 --> 00:01:23,460](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m19s)
kinematic equation the trick here is

39
[00:01:21,119 --> 00:01:25,320](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m21s)
that we also take one time step back in

40
[00:01:23,460 --> 00:01:26,939](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m23s)
the time step back we see that both the

41
[00:01:25,320 --> 00:01:28,409](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m25s)
velocity and jerk terms are negative

42
[00:01:26,939 --> 00:01:30,299](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m26s)
which is incredibly important because

43
[00:01:28,409 --> 00:01:31,979](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m28s)
when we add them together these terms

44
[00:01:30,299 --> 00:01:34,350](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m30s)
will cancel out leaving us with an error

45
[00:01:31,979 --> 00:01:36,180](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m31s)
term of delta T to the fourth which is

46
[00:01:34,350 --> 00:01:37,860](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m34s)
pretty good but what if we actually need

47
[00:01:36,180 --> 00:01:39,960](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m36s)
that velocity for something like maybe

48
[00:01:37,860 --> 00:01:42,060](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m37s)
calculating the kinetic energy well

49
[00:01:39,960 --> 00:01:43,590](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m39s)
never fear stormer is here he said that

50
[00:01:42,060 --> 00:01:45,630](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m42s)
we could calculate the velocity of any

51
[00:01:43,590 --> 00:01:47,520](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m43s)
object simply by taking its position one

52
[00:01:45,630 --> 00:01:49,920](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m45s)
time step forward and its position one

53
[00:01:47,520 --> 00:01:52,770](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m47s)
time step back and dividing by 2 delta T

54
[00:01:49,920 --> 00:01:54,329](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m49s)
which sounds great except let's go back

55
[00:01:52,770 --> 00:01:55,770](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m52s)
to the case of an asteroid moving

56
[00:01:54,329 --> 00:01:58,140](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m54s)
through the gravitational field of

57
[00:01:55,770 --> 00:01:59,939](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m55s)
multiple planets here it's obvious that

58
[00:01:58,140 --> 00:02:02,250](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m58s)
the initial velocity of the asteroid

59
[00:01:59,939 --> 00:02:03,990](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h1m59s)
actually impacts its trajectory don't

60
[00:02:02,250 --> 00:02:05,219](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m2s)
worry those crafty computational

61
[00:02:03,990 --> 00:02:07,140](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m3s)
physicists thought of something for this

62
[00:02:05,219 --> 00:02:08,550](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m5s)
- it's called the velocity for lay

63
[00:02:07,140 --> 00:02:10,349](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m7s)
algorithm where they basically said

64
[00:02:08,550 --> 00:02:12,720](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m8s)
screw it we're just gonna use a

65
[00:02:10,349 --> 00:02:13,390](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m10s)
kinematic equation every time step it's

66
[00:02:12,720 --> 00:02:14,260](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m12s)
a

67
[00:02:13,390 --> 00:02:16,090](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m13s)
exactly what you think it would be

68
[00:02:14,260 --> 00:02:18,280](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m14s)
there's more information about the furl

69
[00:02:16,090 --> 00:02:19,959](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m16s)
a storm overlay and velocity for lay

70
[00:02:18,280 --> 00:02:21,550](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m18s)
algorithms on the arcane algorithm

71
[00:02:19,959 --> 00:02:23,500](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m19s)
archive right now so feel free to check

72
[00:02:21,550 --> 00:02:25,390](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m21s)
it out but here's where I drop the ball

73
[00:02:23,500 --> 00:02:26,770](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m23s)
and you pick it up so if you want to

74
[00:02:25,390 --> 00:02:28,450](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m25s)
help out feel free to write some code

75
[00:02:26,770 --> 00:02:29,920](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m26s)
that drops the ball from five meters and

76
[00:02:28,450 --> 00:02:32,800](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m28s)
shows that it hits the ground in about

77
[00:02:29,920 --> 00:02:34,450](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m29s)
one second submit the code in any way

78
[00:02:32,800 --> 00:02:36,010](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m32s)
you want be a pull request Twitter even

79
[00:02:34,450 --> 00:02:37,480](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m34s)
in the comments section below and I'll

80
[00:02:36,010 --> 00:02:39,190](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m36s)
take the cleanest implementation of

81
[00:02:37,480 --> 00:02:41,680](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m37s)
every language submitted and put it into

82
[00:02:39,190 --> 00:02:43,390](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m39s)
the algorithm archive outside of that

83
[00:02:41,680 --> 00:02:44,260](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m41s)
thank you so much for watching and I

84
[00:02:43,390 --> 00:02:47,040](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m43s)
will see you next time

85
[00:02:44,260 --> 00:02:47,040](https://www.youtube.com/watch?v=g55QvpAev0I#t=0h2m44s)
doodles

