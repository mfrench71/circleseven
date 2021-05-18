---
title: "'Arcade' - Sinclair Spectrum White Lightning Feature Part - 2"
date: 2018-03-09T16:20:06+01:00
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
---

This is part two in a series of Spectrum White Lightning articles originally written in the late 1980s (when I was a teenager) for inclusion in our ZX Spectrum fanzine, 'Arcade'. Having re-read my scribblings almost 30 years later, I don't pretend to understand any of it. It might be useful. It might not. If you do find it useful or, at least, interesting, please leave a comment below.

<!--more-->

From the user manual:

_"White Lightning_ is a high level development system for the Spectrum 48K. It is aimed primarily at the user who has commercial games writing in mind and has the patience to learn a sizeable new language. It is not a games designer and stunning results probably won't be produced overnight, but it does have the power and flexibility to produce software of a commercial standard (with a little perseverance!). "

Read [part one](http://www.circleseven.co.uk/2018/03/09/arcade-spectrum-white-lightning-feature-part-1/).

For some further context for these articles, please see ['Arcade' - A Sinclair ZX Spectrum Fanzine](http://www.circleseven.co.uk/2018/03/07/arcade-zx-spectrum-fanzine/).

---

## White Lightning Feature

Yes, I've made it! Never fear! This feature has made it to its next month. Amazing, isn't it? Anyway, with the sprites in memory, type this into screen 6 and then type `6 LOAD` and then `TEST 1` and press 'Enter':

```
0: SET 44 SPN!;
1: LEFT WRR1M PUTBLS;
2: RIGHT WRL1M PUTBLS;
3: TEST 1 1 KB IF LEFT ENDIF 8 1 KB IF RIGHT ENDIF;
4: TEST 1: ATTOFF SET BEGIN TEST 8 2 KB UNTIL;
```

Don't be alarmed if nothing happens, just press 'Caps Shift' or 'Space' and watch..

'Symbol Shift' gets you out.

This routine would be useful if you had a game like [Lunar Jetman](http://www.worldofspectrum.org/infoseekid.cgi?id=0009372) (in my opinion, the most addictive game yet) which had a scrolling landscape rather like the one in this routine.

When you press 'Space', the landscape goes left, and right when you press 'Caps Shift', rather than the expected right for 'Space' and left for 'Caps' because this simulates a character going over the landscape from left to right and so the landscape would go left and vice-versa.

**Notes on conversion:**

Line 0: sets up sprite 44 - the lunar landscape.

Line 1: defines left as WRR1M - scrolling a sprite 1 pixel right with wrap.

Lines 2: as line 1, but scrolls left.

Line 3: tests to see if SPACE or CAPS SHIFT are pressed and executes to words LEFT or RIGHT accordingly.

Line 4: Switches attributes off. Tests to see if SYMBOL SHIFT is pressed and stops if it is, other it executes TEST to continue the routine.

Now the improvements on the program with the ball in last month's issue. For those who didn't get last month's issue (tsk, tsk!), [here's the program again](http://www.circleseven.co.uk/2018/03/09/arcade-spectrum-white-lightning-feature-part-1/).

Change line 0 to:

```
0: DELAY 500 0 DO 0.1 BLEEP NOOP LOOP;
```

OR (not as well!)

Add line 7:

```
7: GO2 GO SET4 SET3 SET2 SET1; -->
```

SCR#7:

```
0: FINAL GO GO2;
```

Type `6 LOAD` then `FINAL`.

---

## The Originals

|                                                                                                                                                                  |                                                                                                                                                                  |                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![](./img/wp-content-uploads-2018-03-IMG_2232-e1520612840652-225x300.jpg)](http://www.circleseven.co.uk/wp-content/uploads/2018/03/IMG_2232-e1520612840652.jpg) | [![](./img/wp-content-uploads-2018-03-IMG_2233-e1520612866457-225x300.jpg)](http://www.circleseven.co.uk/wp-content/uploads/2018/03/IMG_2233-e1520612866457.jpg) | [![](./img/wp-content-uploads-2018-03-IMG_2237-e1520935679827-254x300.jpg)](http://www.circleseven.co.uk/wp-content/uploads/2018/03/IMG_2237-e1520935679827.jpg) |
