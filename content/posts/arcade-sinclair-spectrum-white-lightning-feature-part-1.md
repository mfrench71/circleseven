---
title: "'Arcade' - Sinclair Spectrum White Lightning Feature - Part 1"
date: 2018-03-09T16:03:33+01:00
draft: false
description: 
author: Matthew French
categories:
- Projects
- Retro Computing
- Sinclair ZX Spectrum
tags:
- Retro Computing
- Sinclair ZX Spectrum
featured_image: white-lightning
---

This is part one an a series of Spectrum White Lightning articles originally written in the late 1980s (when I was a teenager) for inclusion in our ZX Spectrum fanzine, 'Arcade'. Having re-read my scribblings almost 30 years later, I don't pretend to understand any of it. It might be useful. It might not. If you do find it useful or, at least, interesting, please leave a comment below.

<!--more-->

From the user manual:

_"White Lightning_ is a high level development system for the Spectrum 48K. It is aimed primarily at the user who has commercial games writing in mind and has the patience to learn a sizeable new language. It is not a games designer and stunning results probably won't be produced overnight, but it does have the power and flexibility to produce software of a commercial standard (with a little perseverance!). "

For some further context for this article, please see ['Arcade' - A Sinclair ZX Spectrum Fanzine]({{< relref "arcade-a-sinclair-zx-spectrum-fanzine" >}}).

---

## White Lightning Feature

This feature is to help owners of White Lightning to get good, fast results from the package and to produce small routines to incorporate into larger Forth/BASIC programs to create 'arcade' quality games. I have included notes on the programs to help [Laser BASIC](http://www.worldofspectrum.org/infoseekid.cgi?id=0008327) owners convert to their language.

The first routine you may recognise as a part of the demonstration.

```
0: DELAY 500 0 DO NOOP LOOP;
1: SET COL! ROW! SPN! PUTBLS DELAY;
2: SET1 45 10 10 SET;
3: SET2 46 10 10 SET;
4: SET3 47 10 10 SET;
5: SET4 48 10 10 SET;
6: GO 40 0 DO SET1 SET2 SET3 SET4 LOOP;
```

After that, type `6 LOAD` and then `GO`.

**Notes on conversion:**

Line 0: defines a word called `DELAY` which does a no-operation (does nothing) (NOOP) loop 0 - 500 to act as a pause.

Line 1: sets up the parameters of the column, row, and sprite number. It also includes `PUTBLS` which block-moves sprite data from sprite to screen, and the pause in `DELAY`. This line saves typing because you can now enter the values as in lines 2, 3, 4, and 5.

Lines 2 - 5: puts column, row, and sprite number values into line 1 parameters and also executes `PUTBLS` and `DELAY`.

Line 6: executes all definitions 40 times.

The routine can be sped up or slowed down by changing the value of `DELAY` in line 0.

The routine can be lengthened or shortened by changing the value of the loop in line 6.

Next month: improvements on this routine and something new (I hope!).

Send any routines to me at my usual place of residence (not Adam's!)

Matthew F.

---

## The Originals