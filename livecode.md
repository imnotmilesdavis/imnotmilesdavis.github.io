# Midterm Live Code

**dreamcorp. live **

## code

```javascript
//music by miles david (dreamcorp.)
// a piece in multiple parts
//visuals by khoparzi
// licensed with CC BY-NC-SA 4.0 https://creativecommons.org/licenses/by-nc-sa/4.0/
// Aqautic blubs
// https://khoparzi.com

//pitch envelope lead
//$: freq(100,200,250,300).cpm(25).s("sawtooth")
//.penv("<.5 0 7 -2>*2").vib("4:.1")
// $: freq(200,400,500,600).cpm(25).s("sawtooth")
// .penv("<.5 0 7 -2>*2").vib("4:.1")

//arp bullshit
$: freq(1210,1204,1200,1100,1000,900,800,400).cpm(50).s("square")
//.penv("7")
//.lpf(sine.range(500,300).fast(16))
//.release(.5)
//.lpenv(perlin.range(1,8).slow(2))
//.ftype('24db')
//.juxBy(.5,rev)
//.phaser("<1 2 4 8>")
//.room(0.5)
//.rlp(10000)
//.rdim(8000)
//.gain(.09).fast(2)



// epiano melody
//$: freq("<800 750 500>").cpm(50).s("<gm_epiano2>/64")
//.room(8.5)
//.rlp(10000)
//.distort(5)
//.lpf("<100>")
//.gain(.3)
//.hpf("400")

//harmony
//$: freq("<1200 1100 750>").cpm(50).s("<gm_shakuhachi>/64")
//.room(8.5)
//.rlp(10000)
//.distort(5)
//.lpf("<100>")
//.gain(.2)


// //euclid filter pattern
$: freq("<[200,400,450,500,550,600,602,605]>").cpm(50).s("<sawtooth>/64")
.penv("7")
.lpf(sine.range(300,700).slow(16))
.release(.5)
.lpenv(perlin.range(1,8).slow(2))
.ftype('24db')
.juxBy(.5,rev)
.gain(.3)



//delay shit
// $: freq(200,400,450,500,550,600,602,605).cpm(50).s("<sawtooth>/64")
// .penv("7")
// .lpf(sine.range(300,700).slow(16))
// .release(.5)
// .lpenv(perlin.range(1,8).slow(2))
// .ftype('24db')
// .juxBy(.5,rev)
// .gain(.1)

// strudel

// //house tune
// $: note("<[e2,g3,a3,d4,f#4,a4] [c#3,b3,d4,e4,f#4,a4] [c3,b3,d4,e4,f#4,a4] [a2,g3,a3,d4,f#4]>").s("gm_epiano1").euclid(7,16).crush("<16 8 7 6 5>").gain(.3)._pianoroll()

// $: note("<[e2,g3,a3,d4,f#4,a4] [c#3,b3,d4,e4,f#4,a4] [c3,b3,d4,e4,f#4,a4] [a2,g3,a3,d4,f#4]>").s("gm_pad_warm").gain(.3).lpf("400").hpf("300")._pianoroll().gain(.05)

// $: note("<[e4,g5,a5,d6,f#6,a6] [c#4,b4,d5,e5,f#5,a5] [c4,b4,d5,e5,f#5,a5] [a3,g4,a4,d5,f#5]>").s("gm_blown_bottle").euclid(3,8)
//   ._pianoroll()
// .lpf("<200 400 500 700 800 1000 2000 4000>").lpq("<0 5 10 15 20 25>")
// .penv("1")
// .gain(.3)


// $: note("<[e1*4]  [c#2*4] [c2*4] [a1*4]>").s("gm_slap_bass_2")._scope()
// $: note("b5 a5 f#5 b4").fast(4).decay(.05).delay("7").lpf("<200 500 700 900>").gain(.05)
// $: note("f#4 e4 c#4 e4").fast(4).decay(.05).delay("7").lpf("<200 500 700 900>").gain(.05)


// $: note("a5").s("gm_synth_strings_2")
// .room(5)
// .rsize(5)
// .gain("<.03 .02 .01 .001*4>")

// $: s("<bd sd>, ~ oh, ~ hh ~ hh").fast(4)

await initHydra()
gradient(0.25)
.add(noise(), ()=>Math.cos(time))
.modulateRotate(src(o0).rotate(0, -0.52), 0.2).mult(shape(360), 0.8)
.repeat(10,5).mult(shape(360).scale(()=>Math.sin(time)), 0.8).rotate(0, 0.2)
.diff(src(o0).rotate(0, -0.2), 0.2)
.out()

// licensed with CC BY-NC-SA 4.0 https://creativecommons.org/licenses/by-nc-sa/4.0/
// Aqautic blubs
// By Khoparzi
// https://khoparzi.com
```





## EXPLANATION

For my live coding midterm I wanted to experiment with a couple different kinds of music. For this specific piece I arranged two songs I completely composed in Strudel.

The first song is an ambient tune that uses numerical frequencies instead of classic note names like A,B,C,D,etc. Outside of my livecoding work I really love to compose in weird tunings like 432,450, or whatever the max/min a synth will let me go, so I figured I would bring that supercharged approach to Strudel. I started with a fast arpegiator that cycles through 8 frequencies very quickly with a pitch envelope, low pass filter, phaser, and reverb that gives it a sort of dreamy feeling. From there I built couple of differernt leads and accompanying harmonies using E Pianos and Sawtooth waves with pitch envelopes. As you can see, I did get a little bit carried away with the pitch envelope but I found that it had an interesting effect when paired with distortion and reverb, so I had some fun there. For this tune, because of all the reverb tails and distortion I added on many of the layers, gain staging was on my mind quite a bit, as the composition would frequently clip. Besides gain staging, for all the leads and harmonies I roughly approximated pitches that would fit and had to go through quite a bit of trial and error to find the notes I was looking for in my head, but they generally all ended up in the project. My one philosophy was to make sure everything was not super exact, because why not. If I'm not playing with actual precise note names, it shouldn't be exact.

For the second tune, I tried to make a Justice like song with euclidian patterns and some large chords with big extensions. I had a little bit of trouble with chord stacking. After the creator of strudel came to class and showed some beautiful chord arrays, I attempted to make some as well but was not as successful. I had to do a quick and dirty solution with the chords, by spelling out each individual note in <> signs so they would trigger together. I did use the Euclid function to create the rhytmic pattern of the first layer (7.8) and used it again to create another layer that would kind of complent the first pattern (3,8). I was attempting to create a call and response of sorts so there weren't big empty chunks of song just sitting unused. I did get a slap bass sound to play quarter notes and used the strudel default drums because I somehow was not able to get the TR909 to sound good.

As for Hydra, I was trying to build a compelling visual performance but was really struggling so I used code form Khoparzi on the Hydra site.

It actually works really well with the music so it was a great discovery.
The music was 100% original by me. I used Strudel documentation quite heavily to make sure I was getting syntax and objects correct but no code was copied directly from the documentation.

## Citations

// licensed with CC BY-NC-SA 4.0 https://creativecommons.org/licenses/by-nc-sa/4.0/
// Aqautic blubs
// By Khoparzi
// https://khoparzi.com

https://strudel.cc/workshop/getting-started/
