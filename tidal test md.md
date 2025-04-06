## What I Did

I tried to make a simple patch with multiple lead sounds that harmonize in odd ways and have a polyrhythmic relationship without having to use any specific polyrhythm specific commands.... Because I don't know how to use them yet.

## What Went Right and Wrong

Well I got the thing to work which was good but I was really struggling to understand some of the syntax of Tidal cycles. I understood Studel very clearly and I think that is partly due to how great the documentation is. I was trying to port some strudel ideas I had over to Tidal but it wasn't exactly working. I utilized some code from the class repo to get me started with the arps and expanded from there. I also used some drum programing from the class repo that I messed around with,
I was successfully able to break Tidal with my last line. The server ran out of memory which I did find funny. Overall not a whole lot to say about this one. Just getting familiar with the toolset.


```
setcps 0.5
d1 $ fast 4 $ note (arp "<converge diverge pinkyup pinkyupdown thumbup thumbupdown>" "<d'major a'major b'minor e'minor>") # s "newnotes" # crush "[ 2 |16 ]"
d2 $ fast 2 $ note (arp "<converge diverge pinkyup pinkyupdown thumbup thumbupdown>" "<a'major e'major e'minor b'minor>") # s "newnotes" # crush "[ 2 |16 ]"
d3 $ slow 3 $ note (arp "<converge diverge pinkyup pinkyupdown thumbup thumbupdown>" "<b'minor b'major d'minor a'minor>") # s "newnotes" # crush "[ 2 |16 ]"
d4 $ fast 2 $ sound "bd!16 sn" # distort "[16 | 4]" # crush "[ 2 |16 ]"
d5 $ fast 80 $ sound "hh!16" # distort "[16 | 4]" # crush "[ 2 |16 ]"

hush

```
