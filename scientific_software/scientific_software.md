# The problem with scientific software development

Note: all **bolded sections** will be in voice-over with drawings

## Scientific software
When I started this youtube channel a few years ago, I had a rather ambitious goal in mind: to gather a community and research using the lessons learned from open source software development.
The problem is that until recently, I didn't feel competent enough to try anything, but now that I'm nearing the end of my PhD, I feel we can start doing cool research together.
**This can only happen if I am 100% honest with you about the research I have been doing until now, and this video intends to set the stage for more technical discussions in the future.**
**Basically, over the past 7 or 8 years, I have had the privilege of researching by developing scientific software for various types of simulations in plasma physics, warm dense matter, and superfluids.**
**I would like to talk about each of these in the near future, but for now I figure the best place to start is at the start by talking about...**
**The problem with scientific software development... (in 2019)**

To be clear, none of the software I have written has been particularly *popular*.
At best, they've been used by dozens of people.
As such, if you have more or different experience, please feel free to say so in the comment section below.

**First, let me broadly define _scientific software_ as any software created for the specific purpose of enabling researchers to perform their research.**
**This ranges from research code, written for one task and thrown away into the dark depths of Dropbox, to robust software developed by using proper software development principles and used by researchers all over the world.**
**No matter what type of research is being done, software has radically changed the landscape of academia.**

That said, it is currently unclear how scientific software should be written and who should be writing it.
It is clear that to write proper scientific code, you need domain knowledge in the area you are working in.
You cannot expect to write a fancy quantum physics solver with no knowledge of quantum physics.

On the other hand, if you have no knowledge of software development, you will write some pretty terrible code.
Proper scientific software development should be a balancing act between science and software, and it should be supported by researchers as a way to do better research.

**The problem is that modern academia is an incredibly competitive environment that heavily relies on publishing highly cited academic articles.**
**If you don't publish often, your career will perish, which is one reason why (in many disciplines) so few PhD's end up becoming tenured professors.**
**It is really difficult to make it as an academic at all, and researchers end up working incredibly long hours just to keep themselves afloat.**

Until very recently, scientific software was not considered publishable, and thus any researcher writing scientific software would have to develop *on top of* an already impossible work schedule.
Simply put, researchers working to develop good, clean scientific software would be working against the system not with it.
As much as researchers realize the need for well-written, robust scientific software, they most certainly have little incentive to write it.

On the other hand, companies have no incentive tailor their software for the needs of specific research communities.
For the most part, if researchers in a specific field want scientific software to be written, they just ask untrained grad students or post-docs to write it, which obviously creates poor quality software and dubious results.

**If scientists are in the business of creating correct, replicable science, then the software used to generate those results *must* be considered as a necessary part of scientific process.**
**After all, how can we trust a study if it relies entirely on poorly written and buggy code?**

In my opinion, if scientific progress relies on software, that software should be written in a clear and open way and reviewed just like the rest of the scientific literature.
In addition, it should be citable so it can contribute towards a researcher's career development.
**This is why we recently published our primary codebase, GPUE, in the Journal of Open Source Software, which does precisely that.**
**The "paper" is basically an abstract that links to the code, but for now, providing an open review of software in an academic setting is a big step forward that we would like to support.**

**For the record, there are also several universities around the world that are creating research software engineering sections to aid researchers with the development of good scientific software; however, these groups are not often comprised of researchers or individuals wanting to pursue the traditional academic track to become professors.**
**Rather, they are often former academics who realize the current system requires better software development practices.**
**Research software engineers have often made the conscious choice to quit research and instead support it from the outside -- which is a wonderful and admirable thing to do, but still a step away from where most PhD students want to end up.**

**As it stands, it is difficult to be both a scientific software developer and an academic, and there is a big question about whether scientific software is novel enough to be published in the first place.**
**After all, it's just a mix of known methods and software development principles. Is that novel?**
**I would argue that yes, it is.**
**Most research is just a mix of known methods.**
**In my opinion, if new software allows for new research to be done, the software _is_ novel and should be published.**
Sure, some research software may not be as important as other software, but all research is that way.
I figure we can just let the citation count dictate how impactful the software is.

**Another big problem is that computation doesn't really fit the current model of theory and experimentation that many scientists know and love, but we are in a new era.**
If computation is already a necessary component of research, we need to make room for it.
**There's no reason to force research into ancient paradigms that no longer fit.** (draw x and walk away)

I genuinely believe that researchers should do whatever possible to engage the public with their research, so I will be making videos soon about various research topics, most of which involve GPUE, the codebase I briefly mentioned before.
I have also started to do GPUE development streams on twitch when possible, so please feel free to tune in then and ask questions or even help out with the development!
I have one final project left in my PhD and I would love to be able to do this project in as open a way as possible as a test for how we can do open research in the future.
I am very interested to hear what you have to say about the topic of scientific software development, so please feel free to talk in the comment section, on discord, or on twitch!
Thanks again for watching and I'll see you next time! Toodles!
