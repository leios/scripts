1. Gompertz–Makeham law of mortality
2. What is the average age of death?
3. The paper found that right and left-handed people die at different ages and that lefties die at a younger age, but why is that?
4. Why? Because left-handed scissors?
5. Assuming that the proportion of right and left-handed people are the same throughout time, then both should have the same mean age of death, but they don't so...

At some point, nearly every person has probably asked themselves the question: "When will I die?"

No matter what sketchy online quizzes might tell you, there is no way for anyone to really know ahead of time, but we can *estimate* how likely people are to die at any age.
Roughly speaking, we could guess that the likelyhood of dying at any age exponentially increases as you get older.
Of course, there should be a small correction for small children who are much more likely to die than anyone over the age of 5.
Putting these together, we get a well-known curve known as the Gompertz-Makeham law of mortality.

Again, each individual point on this graph represents the probability to die at that particular age.
In other words, if you were to take a snapshot of all the people who died in the year 1990, for example, you would expect to find a distribution that looks like this.
Even though it's unlikely for people to die when they are younger, it is still entirely possible and definitely happens.
Even though it's incredibly unlikely for people to live past the age of 100... Again, it happens.

So from this curve, we can calculate the average age of death by summing up all the ages of death multiplied by the probability to die at that age and then dividing the total sum by the oldest person to have most recently died.
Accoring to the Gompertz-Makeham law, this age will be roughly XXX
Accoring to a study of everyone who died in 1990, the average age of death was roughly YYY, which was pretty close; however, that same study found something rather interesting: The approximate age of death for left handed people was ZZZ, which is less than that for right-handed people at WWW.

So what gives? Are left-handed people actually dying at a younger age?

Well, kinda.

When looking at this plot, it seems clear that the only way for left-handed people to die at a younger age is if their mortality law is shifted a bit, maybe like this...

So now we are left with the obvious question: what could cause a shift in this probability curve?

Before continuing, I think it's useful to pause for a second and think about why the average age of death for left-handed people might be overall younger than that for right-handed people.

As you think about it, I want to highlight a number of things it's *not.*
These are all suggestions given by twitch chat when I asked them the same question
1. It's not because left-handed people are using right-handed equipment.
2. It's not because the left hand is closer to the heart, causing people to over-use that side and cause more strain
3. It's also not because of mental stress due to using the left hand in a right-handed world or...
4. due to lead poisoning because left-handed people rub their hands over papers as they write. By the way, I'm right-handed and do this too, so it's not exclusively a left-handed trait.
5. Importantly, it's also not due to errors in reporting of the data. In the year 1990, left-handed people *did* die at a younger age than right-handed people.

It's actually (somewhat surprisingly) the same reason the average walking speed in cities is higher than in rural areas.

Ok, so let's go back to the plot.

Looking at this, we need to find some way of generating the proper left-handed mortality law, which is not particularly obvious...
but seeing as how the new law is shifted a little to the left, I suppose we can assume that there is another probability function interfering with our results that is probably exponentially decaying to some asymptote.

When adding the normal mortality law with this new function, we see a curve much like the one we need for the left-handed mortality law...

So what exactly is exponentially decaying and also affecting every left-handed person?

Well, the probability to be left-handed.

Simply put, older generations of left-handed people were taught to be right-handed, so it is significantly less likely for left-handed people to be older.
Even though left-handers make up 10% of the population on average, this does not mean that it is constant over time.

Therefore, even though people are way more likely to die when they are older, it's also less likely that they are left-handed, therefore causing an overal shift of the plot to the left.

So, even though left-handed people did die at a younger age in 1990, that doesn't mean that the average life-expectancy for left-handed people is lower.
It just means we need to be a little more cautious with how we interpret results.