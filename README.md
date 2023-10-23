## Recurva
### An alternate keyboard layout focused on efficiency

![recurva](https://github.com/GalileoBlues/Recurva/assets/105921721/68b5ea2f-6a14-4fe3-82cc-ad4bda2861e5)


Recurva's name originates from the Eucalyptus Recurva, a critically endangered species endemic to only a tiny section of New South Wales, Australia.

The goal with Recurva was to solely focus on the rudimentary statistics that I personally feel are the most important in layout design to achieve the best stats that would still be usable. The main stats I considered were:
- Same Finger Bigrams - SFBs (two letters pressed in a row with the same finger).
- Same Finger Skipgrams - SFS (two letters pressed on the same finger but with one letter separating the two).
- Hand balance stays somewhat equal (total usage of letters calculated).

### What does Recurva accomplish?

Recurva accomplishes a new local minimum for Same Finger Skipgrams (SFS) using less efficient elements, previously Semimak held the lowest SFS of any english layout using columns such as RL, HNB which perform extremely well in that category.

Before understanding Recurva's niche it's best to examine the commonly used elements, typically layouts that have R on the pinky cannot have RL as a column which isn't the best for SFBs or SFS, even still it fits many more advantageous compositions.

```
SFBs
rl + lr: 0.087%,
hl + lh: 0.017%,
nl + ln: 0.073%,

SFS
rl + lr: 0.377%,
hl + lh: 0.252%,
nl + ln: 0.576%,
```

All statistics presented here use Shai corpus unless specified.

Looking at these stats you could conclude that HL is better than RL but as mentioned before compositionally this is rarely true because R is much more un-agreeable as a letter in comparison with H. R's most common partners that make sense from as SFB standpoint create a lot of SFS unfortunately which means it often gets put by itself on the pinky homerow or in combination with RL.

Why is this important? because L is just as un-agreeable as R and also causes trouble for the composition, it has the highest number of repeats of any letter (ll: 0.713%) and only goes with the letters i've shown above and the letter M (SFBs: ml + lm: 0.028%, SFS: ml + lm: 0.298%)

## Analysis of Whorf and Semimak

Before we get to the differences between Recurva and layouts like Whorf and Semimak we need to talk about what separates Whorf and Semimak apart:
```
whorf                          semimak_jq
f l h d m  v w o u ,           f l h v z  ' w u o y
s r n t k  g y a e i           s r n t k  c d e a i
x j b z q  p c ' ; .           x j b m q  p g , . /
Sfb:               0.605%      Sfb:               0.798%
Sfs:               6.049%      Sfs:               5.688%
Scissors           0.817%      Scissors:          0.955%
Lsbs               1.988%      Lsbs:              2.122%

Inrolls:           22.39%      Inrolls:           20.24%
Outrolls:          22.48%      Outrolls:          22.18%
Total Rolls:       44.88%      Total Rolls:       42.42%
Onehands:          1.681%      Onehands:          1.862%

Total Alternates:  38.47%      Total Alternates:  40.32%
Total Redirects:   6.293%      Total Redirects:   6.461%
```
One of the main reasons Semimak(jq) performs better on SFS is because `IY` performs better than `CY` and the rest of the index column, while this does decrease SFS dramatically (for this level of optimisation) it sacrifices being able to place every piece of punctuation with the vowels like with Whorf's vowel block. Because of this Semimak_jq specifically places comma below `E` and apostrophe with the index column which creates quite a few SFBs.
```
Semimak's Y interactions:

SFBs
iy + yi: 0.039% - y/ + /y: 0.001% - total of 0.040%

SFS
iy + yi: 0.257% - y/ + /y: 0.005% - total of 0.262%


Whorf's Y interactions:

SFBs
cy + yc: 0.042% - yg + gy: 0.024% - yw + wy: 0.011%
yv + vy: 0.006% - py + yp: 0.035% - total of 0.217%

SFS
cy + yc: 0.085% - yg + gy: 0.060% - yw + wy: 0.176%
yv + vy: 0.015% - py + yp: 0.118% - total of 0.427%

Y interaction delta:

SFBs
Whorf's O.217% - Semimak's 0.040% = 0.177%

SFS
Whorf's 0.427% - Semimak's 0.262% = O.165%


Semimak's E interactions:

SFBs
e, + ,e: 0.190% - eu + ue: 0.148% - u, + ,u: 0.006% - total of 0.344%

SFS
e, + ,e: 0.256% - eu + ue: 0.655% - u, + ,u: 0.044% - total of 0.955%

Whorf's E interactions:

SFBs
e; + ;e: 0.005% - eu + ue: 0.148% - u; + ;u: 0.000% - total of 0.153%

SFS
e; + ;e: 0.021% - eu + ue: 0.655% - u; + ;u: 0.002% - total of 0.678%

E interaction delta:

SFBs
Semimak's 0.344% - Whorf's 0.153% = 0.191%

SFS
Semimak's 0.955% - Whorf's 0.678% = 0.277%
```

This doesn't even account for other corpora where `IY` scales much better than any other interaction with `Y` such as monkeytype's 10k and 450k (relevance to real-world application is up for debate).

Another reason for Whorf having more SFS is because of the position of `D`, on Whorf this is placed on the `T` index where it generates more SFS than the `DC` index Semimak opts for but also saves SFBs because of the accumulative conflicts that all the letters on Semimak's index, especially apostrophe.

Now finally we come to Recurva, Recurva uses RN and LHM instead of RL and HNB which are both used on Whorf and Semimak to achieve their extremely impressive SFB and SFS stats respectively. In the very specific combination of letters that completes Recurva it has worse elements that creates a better stats than Semimak on almost all fronts except for usage of less domininant fingers.

```
Recurva's RN:           Semimak's RL:
rn + nr: 0.191%         rl + lr: 0.073%
rn + nr (SFS): 0.941%   rl + lr (SFS): 0.546%

recurva                        semimak_jq
f r d p v  q j u o y           f l h v z  ' w u o y
s n t c b  . h e a i           s r n t k  c d e a i
z x k g w  m l ; ' ,           x j b m q  p g , . /
Sfb:               0.767%      Sfb:               0.798%
Dsfb:              5.624%      Dsfb:              5.688%
Scissors           0.641%      Scissors:          0.955%
Lsbs               1.540%      Lsbs:              2.122%

Inrolls:           22.80%      Inrolls:           20.24%
Outrolls:          25.16%      Outrolls:          22.18%
Total Rolls:       47.96%      Total Rolls:       42.42%
Onehands:          2.145%      Onehands:          1.862%

Total Alternates:  35.64%      Total Alternates:  40.32%
Total Redirects:   5.393%      Total Redirects:   6.461%
```

So how does Recurva use worse parts to create a better whole? The main innovation is using `H` as the index on the vowel hand, this can only be done by mutating the `RL, HNB` columns into `RN, LHM`. As mentioned earlier `HL` is typically worse for the composition because `RL` gets rid of two very unagreeable letters without a huge difference to the main stats. In this very specific scenario because we've opted for Semimak style vowels we can place period on that column while still having less SFBs and SFS than Semimak's `DC` index.

Because of the columns we've chosen most of the SFBs generated in the layout come almost entirely from `UE`, `OA`, `RN`, `Y,`, and the accumulative period SFBs with the `H` elements.

If you're confused about any explanations here I encourage you to visit the Keyboard Layout Doc: https://bit.ly/keyboard-layouts-doc, it has a wealth of knowledge to read through if theory of layout composition ever interests you.

## Variations

Recurva has a couple variations adaptated for columnar stagger keyboards, these don't change any stats except for Lateral Stretch Bigrams:

```
recurva-colstag                recurva-colstag2
f r d p v  q m u o y           f r d p v  q l u o y
s n t c b  . h e a i           s n t c b  m h e a i
z x k g w  j l ; ' ,           z x k g w  j . ; ' ,
```
There won't be any downloads for these variations as it's pretty much assumed that if you have a columnar staggered keyboard it will most likely be programmable.

## History

Recurva was found accidently while exploring different composition's on Oxey's Layout Playground - an interactive website that allows you to swap letters in a layout and see the result in real time - https://o-x-e-y.github.io/layouts/playground/index.html.

I had been trying to make `RN, LHM` as a composition work since the start of 2023 in january after I completed Gallium, Richard Davidson (https://github.com/rdavison creator of Graphite) and I collaborated on a layout that used `R` on the pinky and `LHM` after I commented on how technically `HL` was better to `RL` in isolation, that layout resulted in Ruthenium which doesn't really accomplish anything significant other than existing as a somewhat new combination and some decent stats. Although I didn't look at it again until recently, it bears a striking resemblance to Recurva in a few ways and definitely reinforced the idea

```
ruthenium
w d l f x  q b u o y
r t h s g  . n e a i
j k m c v  z p ' , ;
Sfb:  0.916%
Dsfb: 6.596%
Scissors: 0.750%
Lsbs: 0.784%

Inrolls: 27.387%
Outrolls: 17.568%
Total Rolls: 44.955%
Onehands: 2.873%

Total Alternates: 38.197%
Total Redirects: 4.799%
```

After Ruthenium I experimented many times with `LHM` as a column. I partially wanted to try `RN` as a replacement to `RL, HNB` as it made the most sense when mutating those columns but also because I admired the structure of Clemenpine's Pine layout - https://github.com/ClemenPine/pine-layout which exhibits `RN` on the left middle finger. To my knowledge the first layout to actually use `RN` and `LHM` together was Halmak.

After a couple months of sporadically trying the combination, in March I got inspired to experiment with the combination while trying semimak vowels at the same time.

```
tungsten                       argon
f r d w v  z l u o y           f r l d w  z v u o y
s n t c p  k h e a i           s n h c g  k t e a i
j x m g b  q , ; . '           x / m p b  j q , . '
Sfb:               0.784%      Sfb:               0.879%
Dsfb:              5.868%      Dsfb:              5.722%
Scissors           0.650%      Scissors:          0.921%
Lsbs               0.895%      Lsbs:              1.500%

Inrolls:           22.04%      Inrolls:           19.90%
Outrolls:          23.48%      Outrolls:          20.50%
Total Rolls:       45.52%      Total Rolls:       40.40%
Onehands:          1.877%      Onehands:          1.530%

Total Alternates:  39.30%      Total Alternates:  42.24%
Total Redirects:   4.343%      Total Redirects:   6.755%

sulfur                         cobalt
f n d l j  ' w o u y           f d l g v  z , u o y
s r t h m  p c a e i           s t h c w  q n e a i
z x b k v  q g . ; ,           j k m p b  x r ; ' .
Sfb:               0.783%      Sfb:               0.835%
Dsfb:              6.149%      Dsfb:              5.784%
Scissors           0.848%      Scissors:          0.961%
Lsbs               1.225%      Lsbs:              1.162%

Inrolls:           26.44%      Inrolls:           31.96%
Outrolls:          16.73%      Outrolls:          18.01%
Total Rolls:       43.17%      Total Rolls:       49.98%
Onehands:          1.315%      Onehands:          3.191%

Total Alternates:  41.38%      Total Alternates:  30.54%
Total Redirects:   5.146%      Total Redirects:   7.309%

```

Ultimately all of these are archival layouts as Recurva accomplishes what they didn't, some of these layouts come close to Semimak's stats but none exceed its superb stats.

3 months later (July) and curious once again about the composition I tried it again but in conjunction with Whorf style vowels.

```
pycnantha
f r d p v  z q o u ,
s n t c y  k h a e i
x j b g w  m l ' ; .
Sfb:  0.709%
Dsfb: 6.048%
Scissors: 0.451%
Lsbs: 1.643%

Inrolls: 22.737%
Outrolls: 25.499%
Total Rolls: 48.237%
Onehands: 1.297%

Total Alternates: 35.722%
Total Redirects: 5.854%
```

Pycnantha's goal was to lower scissors coming from Whorf and to emulate features I favour from Oxey's Sturdy - https://o-x-e-y.github.io/layouts/sturdy/index.html while keeping the stats very close to Whorf. Pycnantha is only a few swaps from Recurva but it would be 2 months before I discovered it as I was hesitant to try Semimak style vowels again and assumed I could not achieve a better result.

The modification into Recurva is quite simple, in this composition `K` creates SFBs with the `H` index that cannot be avoided because the only other place `K` can go is with `T` which already has two letters in its column, the prime candidate to place elsewhere is `B` because its stats when paired in `C` indexes are very good but the issue is that that column is full and no other exchanges can take place.

Recurva only works because it removes the Letter `Y` from the `C` index and allows to you swap `B` into the `C` index and thus place the `K` into the `T` column.


