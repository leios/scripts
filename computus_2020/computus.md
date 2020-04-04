Easter will be April 12, 2020, the Sunday after this video is posted.
If you happen to be watching this in the future, Easter will also be held on
1. the 4th of April 2021
2. the 17th of April 2022, or the
3. the 9th of April 2023

In fact, here is a plot of all the dates of Easter for the next 100 years.
If you squint your eyes a bit, you might see some semblance of a pattern, but to be completely honest, the only real connection between these dates seems to be that they are within roughly a month from each other.

So what gives? Why is Easter hopping around so much?

The short answer is that Easter is always held the Sunday after the first full moon of spring -- also called the paschal full moon.
This is actually a surprisingly complicated calculation that pushed the boundary of human knowledge for centuries, if not millennia.

It is such a complicated calculation that it even stumped mathematical superheroes like Frederick Gauss.
THE Frederick Gauss.

If you don't know who this guy is, he is known for a huge number of different mathematical ideas like
1. Gauss's law
2. The Gaussian distribution
3. The Cooley-Tukey (FFT) method (which he created centuries before Cooley and Tukey did)
4. So much more.

Even so, he had somewhat significant trouble calculating the date of Easter.
His first algorithm was published in 1800, but was corrected a handful of times from there until 1816 when one of his students figured it all out.
The legend goes that Gauss did not actually know his real birthday, but was told that it was a week before Ascension day on a Wednesday in 1777.
After using his method to calculate Easter, he then used it again to calculate his own birthday.

If you are interested in implementing Gauss's Easter algorithm for yourself, feel free to head on over to the Algorithm Archive at the end of this video, where we show the mathematical underbelly of the method.
Here, I simply want to impress upon you how deceptively challenging this problem is.

In essence, the method is split into 2 steps:
1. Finding the full moon after March 21st, designated as the first day of spring by the Pope
2. Finding the following Sunday

Let's start with the full moon bit.
This involves keeping track of two incredibly different calendar systems, the solar calendar (also called the Gregorian calendar after Pope Gregory XIII) and the lunar calendar.

Most people know the Gregorian calendar fairly well.
It's what we use every day.
There are 365 days a year, split into 12 months.
The justification for this is that it takes 365 days for the Earth to revolve around the Sun.

This is *mostly* correct, but there's a small hitch.
It actually takes roughly 365.2425 days to revolve around the sun, which is why every 4 years (including 2020), we add a day to the calendar on February 29th.
These days are called leap days.
With this change, the calendar system would have 365.25 days on average, to get the extra bit of precision, we actually do *not* celebrate leap days when the year is a multiple of 100, unless it is a multiple of 400.
This is why a leap day was celebrated in 2020 and 2000, but not 1900.

Now onto the lunar calendar.
It takes roughly 27.5 days for the Moon to revolve around the Earth; however, lunar phases are closer to 29.5 days apart.
This is because the moon is revolving around the Earth, which is also revolving around the Sun.
To get the same lunar phase, the Moon needs to be in the same position relative to the line between the Sun and Earth.
This is called a synodic month.

Unfortunately, the lunar and Gregorian calendars do not properly line up every year.
If we keep track of the revolutions of the Earth and Moon in space, marking their initial positions, and then again after 12 lunar months and 12 Gregorian months, you will find that the lunar calendar is about 11 days behind the solar one.
In addition, the lunar phase will be completely different than it was on the same day a year before.

It will actually take 19 years for the lunar phase to re-synchronize to be in the same phase on the same day.
This 19 year cycle is known as the Metonic cycle.

At this point, we have all the necessary pieces to the puzzle to find the first full moon of spring.
We would need to figure out where we are on the Metonic cycle and offset ourselves accordingly and all the explicit expressions can be found in the AAA.

All that's left is determining the next Sunday, which is a bit more straightforward than the previous calculation once you realize a simple trait of the Gregorian calendar: days of the week shift by one each year, with exception of leap years.

For example, January 1st 2017 was a Sunday, January 1st 2018 was a Monday, and January 1st 2019 was a Tuesday, 2020 was Wednesday, and 2021 will be a Friday, skipping 2 days because 2020 was a leap year.

Taking all this into account, as long as we knew the date of Easter some time in the past, we can create an offset for that year and then add these corrections to find the next Sunday, and again, please head on over to the AAA for exact mathematical expressions.

I guess if there is any point to this video, it's that calendar systems are tricky -- primarily because they need to match some kind of physical event, such as the movement of celestial bodies.
Transforming between calendar systems is even more difficult, as it requires understanding intricate details all systems involved.

Sure, this algorithm can be easily implemented on a calculator, but it is no doubt worth celebrating for its ingenuity at the time of creation.

[Show d and e when appropriate, but hand wave terms a bit]