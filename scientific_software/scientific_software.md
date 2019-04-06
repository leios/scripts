# The problem with scientific computing

Note: all **bolded sections** will be in voice-over with drawings

## Scientific software vs research code
Over the past 7 or 8 years, I have had the privilege of doing research by transforming research code into scientific software, and I would like to talk about...
**The problem with scientific software development... (in 2019)**

To be clear, none of the software I have written has been particularly *popular*. At best, they've been used by dozens of people. As such, if you have more or different experience, please feel free to chat in the comment section.
**Let's start by drawing a thin line between research code and scientific software**

Research code is primarily written for a small subset of problems within the researcher's field of interest.
**Simply put: a problem appears and code is written to solve that problem. The code is then stored in the researcher's dank Dropbox dungeon for all eternity.**

On the other hand, scientific software is designed to solve a multitude of problems after several researchers have indicated a need.
Often times, scientific software is a language or library that is fundamental to writing code for research, but sometimes it is a stand-alone package for genome sequencing or modeling experimental systems.
**Here, problems arise in research, and software is developed and extended to solve more problems in a similar area**
Scientific software has a development cycle where more problems create more robust software, but it comes with the cost of development time and maintanence, which most researchers don't have.

But this brings up some rather interesting question: what kinds of software do researchers actually need?
To answer this, we need to know what research code actually looks like... And I'll be honest: it isn't pretty.

## Research code
**When software developers look at research code, they often identify  a few primary problems:
1. The code is not following any standard software development principles
2. There is no apparent use of version control
3. There is rarely any testing the results of the code.**

There are other issues with research code, but I would like to attack each of these one-by-one.
Keep in mind that the following arguments are from a software development stand-point and might seem a bit harsh to researchers.
In addition, it is entirely possible to write clean and efficient research code.
If you are a researcher who does your best to write clean, testable code under version control, this is obviously not discussing your code, in particular; however, I would bet you have a researcher-buddy that trusts their completely unreadable, segfaulty code on dropbox with their life.

**The truth is that most scientists were not trained to write code, and because of robust scientific software that has been developed for years,**

- **their code is not often long enough to warrant crazy amounts of development time. [No formal training]**
- **Scientists are paid to publish papers, not write code. [Publish or Perish]**
- **They do not often care about how clean their code looks, so long as it gets the job done. [Limited use]**

Simply put: scientists write code that works, not code that looks good.
More than that, they want their answer as quickly as possible, which means they need to minimize runtime and development time.
Short, dirty code does this and allows scientists to focus on what they actually care about: their research

**Version control is a sticky point for me.
I feel that most scientists should want to keep track of modifications in their code such that they can keep their lab notebooks easier; however, the argument often goes the other way around.**

- **Researchers often argue against version control because they are already keeping a lab notebook, so the revision history is not as important. [Lab notebooks exist]**
- **Researchers often feel that learning a complicated version control system would only hinder their progress [git is hard]**
- **And (the kicker), most researchers "already have dropbox for file sharing [Dropbox counts as version control, right?]**

*astonishment*. Honestly, that last point irks me a lot.

**Finally, testing.
Science is in the business of making sure it's results are correct.
If research code is producing the wrong results, there is a big, big problem that needs to be fixed immediately.
That said, most researchers ignore explicit tests on their research code because**

- **they are working off of sufficiently advanced scientific software that they trust already and their code is not long enough to warrant testing or inhibits their ability to write clean code [matlab use]**
- **Their *test* is the end-result against their own physical intuition. As long as they can argue that their solution *should* be correct with the appropriate theory to back those claims up, no further testing is required [physical intuition as a unit test]**

As someone who writes scientific software, I can guarantee that a few tests here and there have saved my butt...
But maybe that's just because I am a miserable excuse for a physicist whose physical intuition is usually incorrect.

The point is that if you directly address scientists about their code, they will always come up with reasons not to change the status quo.

**As a final note: many researcher do not see writing code as fundamental research and discourage their students from learning proper software development techniques because software does not produce high-impact publications [No publication mechanism for research code]**

Now I want to shift gears to scientific software.
Again, for the purpose of this video, the difference between research code and scientific software is intent.
Scientific software is meant to be *used by* scientists and extends beyond the specific use-cases of research code.

## What makes scientific software difficult to write
**For the most part, scientific software can be split into 3 categories"
1. packages meant for a particular use
2. languages that produce research code**

** Neither category is particularly difficult to understand.
On the one hand you have packages like comsol for physics simulations, igv for genomics, or paraview for visualization.
These packages are meant to keep the researcher as far away from code as possible and often come with graphical or robust command-line interfaces to keep things as simple as possible.**

** On the other hand, you have languages like Fortran, CUDA, matlab, julia, labVIEW, numpy and scipy.
These all allow scientists to write code to solve their problems, but are often specifically meant for number-crunching.
You wouldn't write an OS in Fortran, and there's a reason for that.**

The main problem with scientific software from a software development perspective is that both of these categories require specific domain-knowledge of either computational mathematics, or whatever area your software is directed toward.

**In addition, a lot of scientific software is meant to be run on supercomputers, where there is no graphical interface easily available and the code sometimes takes days or weeks to finish -- all while doing nothing more than crunching numbers. [The supercomputer problem**

Because of this, some standard software development practices should be avoided in scientific software development because they come with unintentional overhead.
Any small delay in function calls could lead to an additional day of runtime, which researchers don't really have time for.

The point is that scientific software is not as easy to write as it might seem, and even if it's not as pretty as it could be, it is meant to be simple, fast, and effective.
Good scientific software does this.

## Some solutions

The fact is that scientific software development is inherently interdisciplinary and requires knowledge of both science and software development.
**It is also unclear who should be writing and maintaining this software.
should it be the researchers or separate software development companies?**

Currently, many important industrial partners are taking up the reign for scientific software development.
**nvidia and intel are creating new devices for computation, mathworks is developing matlab, kitware is producing paraview...**
It is much cheaper for scientists to pay for a software license than a developer... So it makes sense that industries take advantage of this.

If researchers are intended to write good, clean scientific software, then researchers need to start respecting scientific software and citing it in their papers -- otherwise, the scientists developing the software cannot advance in their career.
The problem is that there are few good places to publish and review software, with exception of new initiatives like the journal of open source software, where we published our most recently developed software: GPUE: the graphics processing unit Gross-Pitaevskii equation solver (which we'll certainly talk about more in the future).

In addition, there are large open-source projects like julia that are making impressive strides with a mix of industry funding and academic grants, thus allowing researchers to write the software they need and want.

## Conclusions
I don't often make discussion-y videos like this, but I feel it is important for scientists to talk about the research they do in an open way to as many people as they can... and I intend to do just that, so expect videos on GPU computing, superfluids, chaos, guage fields, compressive sensing, and potentially optimal control or molecular dynamics.

I am also still working on algorithm archive revisions and will let you guys know as new content comes out.
My hope is to make a new video every time a new paper or chapter is published, but there might be some delays here and there... After all, I'm still in the middle of my thesis.

Anyway, we are back to daily streams on twitch from 5-7AM JST every day and we are also doing additional research streams where we talk about GPU computing and superfluids from 9-12 AM JST when I can.
Thanks again for watching and let me know your thoughts in the comment section below!
Peace!