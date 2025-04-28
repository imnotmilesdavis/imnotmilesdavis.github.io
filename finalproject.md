** Miles' Final Project **

## What I did

I tried to make something that resembles music the least. I wanted to play with a lot of kind of ridiculous distortion and noise to see what kind of dumb stuff I could do with it. A lot of the performance I wanted to play with the "fast 4" "slow 4" type of arguments because it really influences how the delay reacts and also can play with a lot of arrangement ideas. The one idea I try to play with a lot is using gain to fade in and fade out elements.

## What Worked

Honestly I don't have a lot to say for this part. Everything in this code works as far as my testing goes.
A lot of what I have to say is what didn't work.... Se below.  

## What Didn't Work

There weren't necessarily things that didn't work, but things I couldn't figure out.
I had some significant problems trying to add memory to the SuperCollider server because of some crashing issues.
I was also having some issues with certain TidalCycles functions just because of the absolutely atrocious documentation.
I love Strudel so much because of the incredible documentation. I feel like I can pretty accurately understand what is happening
and learn very quickly, but with TidalCycles, so much of the documentation is non existent or broken I struggle pretty hard.
As well, sometimes I'll try something in the code that they've posted and it will just not work. Never quite sure why but I feel like there's either something outdated about the documentation or just non-functional with my software. It's weird. These problems led me to really downsize my project,
and do something a lot simpler that I know would work consistently rather than doing a more expansive project that would be more comprehensive of the
skills I've learned in the class. Also superdirt is killing me with the synths. Some of them just don't work.

## External Code

Nothing external. Just referencing documentation for functions. Nothing copied directly.








```
setcps 80

d1 $ slow 1 $ s "armora" <| n (run 3)
#vowel "a e i o u"
#triode ("<1 3 5 7 9>")
#lbrick("<0 0.1 0.2 0.3 0.4 0.5 0.6>")
#binshift ("2")
# djf("<0 0.1 0.2 0.3 0.4 0.5 0.6 0.7>")

d1 $ slow 4 $ n ("c e f g a b" |+ "<'maj 'min 'six 'min6 'ninesus4>")
# s "supersquare"
# decay "[1 2]/4"
# gain("0")

d2 $ s "ravemono" <| n (run 4)
# crush("<1 8 2 0 4 0 0 6 5>")
# ring("<0 1 3 5 7 9>")
#djf("<0 0.1 0.2 0.3 0.4 0.5 0.6 0.7>")
# gain("0")

d3 $ fast 4 $ s "hh"
# gain("1.5")
# distort ("<1 4 6 7 8 9 0 1>")
# gain("0")

d6 $ slow 4 $ s "dr_few" <| n (run 8)
# gain("0")
# distort (range 1 7 $ sine)

d7 $ sound "arpy*4"
# speed (rand + 7)
# distort (range 1 10 $ sine)
# crush (range 1 16 $ sine)
# gain ("0")

d1 $ slow 3 $ n ("d f a b d e" |+ "<'maj 'min 'six 'min6 'ninesus4>")
# s "supersaw"
# vowel "a e i o u"
# decay "[1 2]/4"
#lbrick("<0 0.1 0.2 0.3 0.4 0.5 0.6>")
# delay("0.5")
# gain("1")

d3 $ slow 16 $ s "<dr_few>" <| n (run 1)
# crush (range 1 16 $ sine)
# distort ("4")
# delay("0.5")
# gain("1")

hush
```
