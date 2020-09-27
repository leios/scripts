1
[00:00:00,000 --> 00:00:03,929](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m0s)
a while ago we talked about Fourier

2
[00:00:01,530 --> 00:00:05,970](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m1s)
transforms which basically allow us to

3
[00:00:03,929 --> 00:00:08,340](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m3s)
distinguish exact frequencies of waves

4
[00:00:05,970 --> 00:00:10,380](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m5s)
in real space by moving to frequency

5
[00:00:08,340 --> 00:00:12,030](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m8s)
space I encourage you to check out that

6
[00:00:10,380 --> 00:00:14,309](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m10s)
video if you haven't already the link

7
[00:00:12,030 --> 00:00:16,199](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m12s)
will be in the description the problem

8
[00:00:14,309 --> 00:00:18,330](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m14s)
is that that video left at a bit of a

9
[00:00:16,199 --> 00:00:20,760](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m16s)
cliffhanger we said that nearly all

10
[00:00:18,330 --> 00:00:22,890](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m18s)
Fourier transforms are executed in code

11
[00:00:20,760 --> 00:00:24,779](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m20s)
but even though discrete Fourier

12
[00:00:22,890 --> 00:00:27,990](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m22s)
transforms can be directly implemented

13
[00:00:24,779 --> 00:00:30,390](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m24s)
they are incredibly slow the question

14
[00:00:27,990 --> 00:00:32,850](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m27s)
now is can we make the discrete Fourier

15
[00:00:30,390 --> 00:00:35,790](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m30s)
transform fast and the answer is yes

16
[00:00:32,850 --> 00:00:38,190](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m32s)
with a fast Fourier transform or FFT

17
[00:00:35,790 --> 00:00:40,649](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m35s)
using for example the Cooley Tukey

18
[00:00:38,190 --> 00:00:42,809](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m38s)
algorithm now here's a bit of a problem

19
[00:00:40,649 --> 00:00:45,270](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m40s)
the discrete Fourier transform is

20
[00:00:42,809 --> 00:00:47,960](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m42s)
defined by this formula which requires a

21
[00:00:45,270 --> 00:00:50,219](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m45s)
sum over all real or imaginary space

22
[00:00:47,960 --> 00:00:52,320](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m47s)
this means if we're going to play any

23
[00:00:50,219 --> 00:00:55,890](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m50s)
tricks we have to be careful not to miss

24
[00:00:52,320 --> 00:00:57,719](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m52s)
any elements so here's what we do

25
[00:00:55,890 --> 00:00:59,789](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m55s)
imagine we have an array with eight

26
[00:00:57,719 --> 00:01:01,859](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m57s)
elements in it the first step is to

27
[00:00:59,789 --> 00:01:03,300](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h0m59s)
strategically shuffle our elements and

28
[00:01:01,859 --> 00:01:05,460](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m1s)
this can be done in a number of

29
[00:01:03,300 --> 00:01:07,439](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m3s)
different ways one way is to simply

30
[00:01:05,460 --> 00:01:09,119](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m5s)
recursively split all the even and odd

31
[00:01:07,439 --> 00:01:10,950](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m7s)
elements over and over again and

32
[00:01:09,119 --> 00:01:13,590](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m9s)
concatenate the array at the end

33
[00:01:10,950 --> 00:01:15,689](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m10s)
another method uses bit reverse ordering

34
[00:01:13,590 --> 00:01:17,700](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m13s)
here we write up the bit strings for

35
[00:01:15,689 --> 00:01:19,080](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m15s)
every number and flip them swapping the

36
[00:01:17,700 --> 00:01:21,240](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m17s)
appropriate elements afterwards

37
[00:01:19,080 --> 00:01:22,590](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m19s)
depending on the language one of these

38
[00:01:21,240 --> 00:01:25,770](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m21s)
methods might be easier to implement

39
[00:01:22,590 --> 00:01:27,810](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m22s)
than the other regardless next is the

40
[00:01:25,770 --> 00:01:30,720](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m25s)
tricky part combining all of these

41
[00:01:27,810 --> 00:01:33,240](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m27s)
elements back together to visualize this

42
[00:01:30,720 --> 00:01:35,340](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m30s)
step most people use a butterfly diagram

43
[00:01:33,240 --> 00:01:37,680](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m33s)
which basically shows the flow of data

44
[00:01:35,340 --> 00:01:39,570](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m35s)
with time the idea is somewhat

45
[00:01:37,680 --> 00:01:41,430](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m37s)
straightforward for the first iteration

46
[00:01:39,570 --> 00:01:43,920](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m39s)
we combine pairs of elements together

47
[00:01:41,430 --> 00:01:45,869](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m41s)
the second iteration we combine pairs of

48
[00:01:43,920 --> 00:01:48,540](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m43s)
pairs and in the third iteration we

49
[00:01:45,869 --> 00:01:50,520](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m45s)
combine pairs of pairs of pairs each

50
[00:01:48,540 --> 00:01:52,439](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m48s)
combination is of course called a

51
[00:01:50,520 --> 00:01:55,259](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m50s)
butterfly because it looks like an

52
[00:01:52,439 --> 00:01:57,659](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m52s)
hourglass in addition each butterfly is

53
[00:01:55,259 --> 00:01:59,100](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m55s)
a small discrete Fourier transform that

54
[00:01:57,659 --> 00:02:01,439](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m57s)
avoids unnecessary matrix

55
[00:01:59,100 --> 00:02:03,570](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h1m59s)
multiplications and summations instead

56
[00:02:01,439 --> 00:02:06,299](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m1s)
of eight sums here we only need seven

57
[00:02:03,570 --> 00:02:08,399](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m3s)
weaker butterflies as the system size

58
[00:02:06,299 --> 00:02:10,080](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m6s)
gets larger it becomes less logical to

59
[00:02:08,399 --> 00:02:12,270](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m8s)
even consider using a discrete Fourier

60
[00:02:10,080 --> 00:02:13,090](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m10s)
transform because the FFT will simply be

61
[00:02:12,270 --> 00:02:15,129](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m12s)
much much

62
[00:02:13,090 --> 00:02:16,540](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m13s)
faster now let's look at the simplest

63
[00:02:15,129 --> 00:02:19,269](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m15s)
butterfly and describe what it

64
[00:02:16,540 --> 00:02:21,550](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m16s)
mathematically represents again it's a

65
[00:02:19,269 --> 00:02:23,530](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m19s)
mini discrete Fourier transform so we're

66
[00:02:21,550 --> 00:02:26,910](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m21s)
going to need an array of the e to the 2

67
[00:02:23,530 --> 00:02:29,349](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m23s)
pi K terms which will define as Omega

68
[00:02:26,910 --> 00:02:33,640](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m26s)
quantitatively this butterfly says that

69
[00:02:29,349 --> 00:02:38,080](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m29s)
b0 equals a0 plus Omega naught a 1 and B

70
[00:02:33,640 --> 00:02:40,209](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m33s)
1 equals a0 plus Omega 1 a 1 it seems

71
[00:02:38,080 --> 00:02:42,220](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m38s)
simple enough but there's a trick here

72
[00:02:40,209 --> 00:02:44,590](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m40s)
that nearly everyone plays that took me

73
[00:02:42,220 --> 00:02:46,299](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m42s)
weeks to figure out like I said we're

74
[00:02:44,590 --> 00:02:49,060](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m44s)
going to need an array of these Omega

75
[00:02:46,299 --> 00:02:50,500](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m46s)
values but it turns out that the second

76
[00:02:49,060 --> 00:02:52,390](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m49s)
half of this array will always be equal

77
[00:02:50,500 --> 00:02:55,360](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m50s)
to the negative of the first half of

78
[00:02:52,390 --> 00:02:57,430](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m52s)
this array so we can save Ram by simply

79
[00:02:55,360 --> 00:02:59,799](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m55s)
using half of the array of Omega values

80
[00:02:57,430 --> 00:03:01,870](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m57s)
in this case we simply need to change

81
[00:02:59,799 --> 00:03:04,090](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h2m59s)
Omega 1 to negative Omega naught

82
[00:03:01,870 --> 00:03:06,010](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m1s)
throughout most of the literature you'll

83
[00:03:04,090 --> 00:03:08,049](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m4s)
see this trick played and it's not

84
[00:03:06,010 --> 00:03:10,510](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m6s)
really properly described anywhere so

85
[00:03:08,049 --> 00:03:12,129](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m8s)
here is the butterfly diagram again with

86
[00:03:10,510 --> 00:03:15,459](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m10s)
all the appropriate Omega values placed

87
[00:03:12,129 --> 00:03:18,100](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m12s)
in ultimately the power of the FFT

88
[00:03:15,459 --> 00:03:19,870](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m15s)
cannot be understated it's used in

89
[00:03:18,100 --> 00:03:22,060](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m18s)
pretty much every area of research and

90
[00:03:19,870 --> 00:03:25,870](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m19s)
has made previously impossible problems

91
[00:03:22,060 --> 00:03:27,609](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m22s)
possible as before the Cooley 2 key

92
[00:03:25,870 --> 00:03:28,859](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m25s)
algorithm is up on the algorithm archive

93
[00:03:27,609 --> 00:03:31,359](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m27s)
and is awaiting language-specific

94
[00:03:28,859 --> 00:03:32,500](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m28s)
implementation thanks again to all of

95
[00:03:31,359 --> 00:03:35,769](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m31s)
these people for helping with the

96
[00:03:32,500 --> 00:03:36,910](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m32s)
archive so far also before you go I

97
[00:03:35,769 --> 00:03:39,310](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m35s)
wanted to thank you again for watching

98
[00:03:36,910 --> 00:03:41,139](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m36s)
we recently hit 1 million channel views

99
[00:03:39,310 --> 00:03:45,069](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m39s)
and 2 to the 13 subscribers which is

100
[00:03:41,139 --> 00:03:47,049](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m41s)
absolutely crazy to me seriously you

101
[00:03:45,069 --> 00:03:48,700](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m45s)
guys Rob thank you so much for watching

102
[00:03:47,049 --> 00:03:51,180](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m47s)
and I will see you next time

103
[00:03:48,700 --> 00:03:51,180](https://www.youtube.com/watch?v=XtypWS8HZco#t=0h3m48s)
toodles

