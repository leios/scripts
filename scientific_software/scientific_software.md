# The problem with scientific software development

Note: all **bolded sections** will be in voice-over with drawings

## Scientific software vs research code
When I started this youtube channel a few years ago, I had a rather ambitious goal in mind: to gather a community and research using the lessons learned from open source software development.
This can only happen if I am 100% honest with you about the research I have been doing and this video intends to set the stage for more technical discussions in the future.
Basically, over the past 7 or 8 years, I have had the privilege of researching by developing scientific software for various types of simulations in plasma physics, warm dense matter, and superfluids.
I figure the best place to start is at the start by talking about...
**The problem with scientific software development... (in 2019)**

To be clear, none of the software I have written has been particularly *popular*. At best, they've been used by dozens of people.
As such, if you have more or different experience, please feel free to chat in the comment section.

First, let me broadly define *scientific software* as any software created for the specific purpose of enabling scientists to perform their research.
This ranges from research code, written for one task and thrown away into the dark depths of Dropbox, to robust software used by scientists all over the world to perform specific tasks.
No matter what type of research is being done, software has radically changed the landscape of academia.

That said, it is currently unclear how scientific software should be written and who should be writing it.
It is clear that to write proper scientific code, you need domain knowledge in the area you are working in.
You cannot expect to write a fancy quantum physics solver with no knowledge of quantum physics.

On the other hand, if you have no knowledge of software development, you will write some pretty terrible code.
I don't mean to brag, but I have certainly had scientists brag to me about how they use Dropbox as version control.
It's honestly quite horrifying at times.

Proper scientific software development should be a balancing act between science and software, and it should be supported by researchers as a way to do better research.

The problem is that modern academia is an incredibly competative environment that heavily relies on publishing highly cited academic articles.
If you don't publish often, your career will perish.
Because of this, it is incredibly difficult to make it as an academic at all, and researchers end up working incredibly long hours just to keep themselves afloat.

On top of this, until very recently scientific software has not been considered publishable, and thus any researcher doing scientific software development would have to do develop *on top of* an already impossible work schedule.
Simply put, researchers working to develop good, clean scientific software would be working against the system.

As much as researchers realize the need to well-written, robust scientific software, they most certainly do not want to write it.
On the other hand, they also don't want to pay for it.

Though certain companies, like nvidia, mathworks, and wolfram research have managed to write quality software that researchers all around the world use and pay for, they are the exception, not the rule.
They also work on general-purpose software that can be used for a wide variety of problems to maximize their userbase.
For the most part, if researchers in a specific field want scientific software to be written, they just ask untrained grad students or post-docs to write it, which obviously creates poor quality software and dubious results.

The julia programming language is a rather interesting exception. The language is 100% open-source, is used by researchers all over the world, and has been written by researchers who are trying to radically change the field of scientific computing.
It would be nice to see more large-scale software research projects like julia to appear in the future, but I don't expect them any time soon.

In the end, the problem is that scientists don't care about software. They just care about the end result...
but if scientists are in the business of creating correct, replicable results, then the software used to generate those results *must* be considered as a necessary part of scientific process.
After all, how can we trust a study if it relies entirely on poorly written and buggy code?

In my opinion, if scientific progress relies on software, that software should be written in a clear and open way and reviewed just like the rest of the scientific literature, which is why we recently published our primary codebase, GPUE in the Journal of Open Source Software, which reviews research software and publishes it in a citable journal for the future.
It's basically just an abstract that links to the code.
We're working on new publications with some novel features and applications of the software.
For now, providing an open review of software in an academic setting is a big step forward that we would like to support.

In addition, there are several universities around the world that are creating research software engineering sections to aid researchers with the development of good scientific software; however, these units are not often comprised of researchers or people wanting to continue along the traditional academic track to become professors.
Rather, they are former academics who realized the current academic system is deficient and requires better software development practices.
They have often made the conscious choice to quit research and instead support it from the outside -- which is still a wonderful and admirable thing to do, but still a step away from where most PhD students want to end up.

As it stands, it is difficult to be both a scientific software developer and an academic, and although that is changing, we are far from "professor of scientific computing" being a common title in academia.

I genuinely believe that researchers should do whatever possible to engage the public with their researsh, so I will be making videos soon about various research topics, most of which involve this codebase, and I have started to do GPUE development streams on twitch when possible, so please feel free to tune in then and ask questions or talk about the future of scientific software development.
