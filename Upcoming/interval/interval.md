Hello wonderful people of the internet, *this* is my twitch stream and *that* is a push-up counter.
Basically, every time I get an error like this one, I add a push-up to the counter and do all of them at the top of the hour before getting back to programming.
[Now, I know what you are going to ask, "Is this a good idea?"]
[No. It's not, but I did it anyway and here's why]

You know that feeling when you alarm goes off, but you are not fully awake so you decide to close your eyes for another second or two with the hopes of magically feeling fully rested when you open them back up again?
In that moment, when you close your eyes, you completely lose track of time. When they open back up again, it could be anywhere from 10 seconds to 2 hours later.
[That is how I have felt for the past 12 months, and I had no idea how to fix it until I managed to book a lane at my local pool]

See, when swimming, I am always racing against the clock. Here, I am doing a 50 yard butterfly on a 45 second interval. Even though it only takes me about 30 seconds to get to the wall, I wait until the interval is up to go again.
Now, pushing off that wall is *hard*. 15 seconds is *not* enough time to be fully rested, but that is the nature of interval training.
It allows you to push your body further than normal by giving yourself a little rest as a reward for swimming fast.

[So then I thought, "Why not just do this all the time?"]

[So for the past month, I have been doing just that.]
Every working hour, I choose a specific task to complete within the next 60 minutes, and if I finish it early, I can rest a bit on YouTube, twitter, or Reddit.
The point is to pace myself, but also complete clear objectives, and in this way, I've actually been a bunch more productive.

Still, starting every hour is hard, just like it's hard to push off the wall or get out of bed.
But I found that 5 minute exercises at the top of ever hour provide that kick of motivation that I needed.

I did this for about a month, 5 minutes of exercise, a project, and rest ever hour, and honestly, I started to feel much better.
So much better, that I actually wanted to stream again for the first time in a few months.

At the same time, I wanted to keep my interval training up, so I came up with the push-up counter idea.
My plan was to use the push-ups as my 5-minute exercise every hour.

[But here's where the story actually gets kinda interesting.
See, as I was discussing my new interval lifestyle, the obvious question came up about how I choose what exercise to do.
And then pinkemma in chat suggested I choose the next exercise with some sort of AI.

We kinda agreed that AI might be overkill, but I then remembered back to my supercomputing days...
One common way to ensure that tasks are run efficiently on a cluster is with a method known as priority scheduling.]
Here, each task is given a priority and if multiple tasks are queued at the same time, the one with the highest priority is selected first.
Now, the priority here can be determined based on a number of factors, like runtime, the funding of the project, what hardware the code needs, etc.

[Obviously, if we are scheduling 5 minute exercises every hour, we do not really need to worry about the same things as large supercomputers do, but the idea of providing each exercise some priority is a good way to ensure we get a full-body workout every day.]

So we created 4 exercise groups:
* Legs
* Core
* Arms
* Mobility

We then sorted all exercises we could think of into these groups.
Crunches went in core. Squats went in legs. Dips went in arms, etc.

To start, we give each exercise and each set of exercises a random priority before sorting them.
Then, we choose the exercise with the highest priority from the group with the highest priority before resetting both to zero and increasing the priorities of all exercises with a random number.
This effectively allows us to cycle between all exercises with some small random variation.

For example, if we chose squats as our exercise, the legs group would then be sent at the end of the queue, and squats, in particular, would then be sent to the end of the legs group.
Now, the next exercise will almost certainly not be legs and the next time we choose a leg exercise, it will almost certainly not be squats.

To beta-test the software, we did a work-out on twitch where chat was able to increase and decrease the difficulty of the next exercise, add push-ups, and shuffle all exercises, if they wanted.
Because the exercises cycled between different muscle groups and were randomly initialized, no one knew what the next exercise would be until it was chosen.
Honestly, it was the most fun workout I think I have ever had, and I will probably be doing it again on weekends in the future, so feel free to stop by if this sounds interesting to you!

Honestly, though, that's about all there is to it.
5 minutes of exercise and a 55 minutes of a combined project and rest every working hour.
The (admittedly quite buggy) code is available at SwoLeios.jl (thanks to Foldster for the name).
If people are interested, I am happy to work with it and turn it into something more people could use, maybe even making an app or something like that.

[Now, real talk. I am not saying that the SwoLeios workout program will end your depression.
I'm also not saying it will make you swole.

All I'm saying is that interval training my life really helped *me* get back on track to start making things again.
That said, I've always loved working out, so a little physical exercise is really motivating for me.
I think the takeaway here should not be that you should be doing more physical exercise.
Rather, I think it should be that creating small, but meaningful and achievable goals is one way to start moving towards wherever you want to go.
Also, there's something to be said about doing something incredibly stupid like a push-up counter to shake things up and find the initial burst of creativity.

Anyway, that's all I have for now. If you like this content and want to see it continue in the future, please consider supporting me on either patreon or github sponsors.]
Also: thanks to those who have already chosen to support me on patreon, like mossy and valentin... And Valentin, don't worry. I'll probably be using some of your code in an upcoming video. 
