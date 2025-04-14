## What I Did

I made the most repulsive patch ever.... By Choice.
I crashed out trying to make something truly musical sounding in Tidal cycles and decided to haphazardly throw a bunch of kicks together, vocal samples, and drums to make something horrible. I got really excited with the crush function and added that to about everything and made sure the intensity would fluctuate throughout the cycle. I also distorted pretty much everything. On one of the kicks I had the playback speed randomized so it would provide the illusion of melody. I really just tried to make something horrible. When I live code it I have some other things I do with the cycles per second and other things to make it even worse.

## What Worked and Did not

What is in my code is really what worked. Functionally everything works as expected and without question. However, the things that didn't work are not in the code because I couldn't figure them out. I referenced the documentation a lot in this code but lost the part about using "fast" or "slow" functions and was having some syntax problems. I'm also having some problems pulling samples and finding a database for what samples I already have and also don't have. Some way to find that information would be great.

```
setcps(160)
d1 $ sound "[[bd ~ bd] !bd sn:5] [bd! sn:3] [hh~*7]" # crush "4 6 7 4" # gain "10" # pan "1 2 1 1 1 2 2 2"
d2 $ sound "hardkick*18" # crush "4 8"
d3 $ sound "numbers:1 numbers:2 numbers:3 numbers:4" # pan "0 0.5 1" # distort "1 2 4 6 8 9 10" # pan "2 2 2 2 1 1 1 1"
d4 $ sometimes (# speed "32 2 5 8") $ sound "hardkick*8"
d5 $ speed "32 2 5 8") # sound "arpy(12,1,2,3,4,5,9,11)" # n(irand 32)
hush
```
