---
title: "'Arcade' - Sinclair Spectrum White Lightning Feature - Part 3"
date: 2018-05-24T19:55:29+01:00
draft: false
description: 
author: Matthew French
categories:
tags:
- Retro Computing
- Sinclair ZX Spectrum
- Programming
featured_image: white-lightning
---

This is the third (and final) part in a series of Spectrum White Lightning articles originally written in the late 1980s (when I was a teenager) for inclusion in our ZX Spectrum fanzine, 'Arcade'. Having re-read my scribblings almost 30 years later, I don't pretend to understand any of it. It might be useful. It might not. If you do find it useful or, at least, interesting, please leave a comment below.

<!--more-->

#### From the User Manual

_"White Lightning_ is a high level development system for the Spectrum 48K. It is aimed primarily at the user who has commercial games writing in mind and has the patience to learn a sizeable new language. It is not a games designer and stunning results probably won't be produced overnight, but it does have the power and flexibility to produce software of a commercial standard (with a little perseverance!). "

Read [part one]({{< relref "arcade-sinclair-spectrum-white-lightning-feature-part-1" >}}) and [part two]({{< relref "arcade-sinclair-spectrum-white-lightning-feature-part-2" >}}).

For some further context for this article, please see ['Arcade' - A Sinclair ZX Spectrum Fanzine]({{< relref "arcade-a-sinclair-zx-spectrum-fanzine" >}}).

---

#### White Lightning Feature

Last month we had a program that scrolled a landscape left and right. This month we have a window scrolling in eight possible directions under keyboard control. (Phew! Advanced stuff, eh?)

Type the following proggy into screen 6:

```
0: SET 0 COL! 10 ROW! 20 LEN! 5 HGT;
1: UP 1 NPX! WCRV;
2: DOWN -1 NPX! WCRV;
3: LEFT WRL4V; : RIGHT WRR4V;
4: KEYS 7 1 KB IF LEFT ENDIF 8 1 KB IF DOWN ENDIF;
5: KEY2 1 1 KB IF LEFT ENDIF 1 2 KB IF RIGHT ENDIF;
6: TEST SET BEGIN KEYS KEY2 8 2 KB UNTIL;
```

That's all it is. Imagine trying to do that in BASIC.

ENTER and SPACE for left and right. CAPS SHIFT and Z for up and down. SYMBOL SHIFT exits.

If you want to use your own keys, then here are the keyboard numbers (what a service!)

{{< post-image image="white-lightning-3-keyboard.jpg" width="300" caption="" >}}

#### Notes on Conversion

Line 0: sets up the dimensions and positions of the window.

Line 1: defines UP. NPX is the number of pixels and WCRV is scrolling the window vertically with wrap.

Line 2: defines DOWN. As UP but -1 NPX indicates a downward scroll.

Line 3: defines LEFT and RIGHT. WRL4V and WRR4V are commands to scroll the window left and right by 4 pixels with wrap.

Lines 4 and 5: polls the keyboard.

Line 6: executes the program until SYMBOL SHIFT is pressed.

Next month: Who knows, I certainly don't. Something good as usual.

Matthew F.

---

#### The Originals

{{< post-image image="white-lightning-3-original-1.jpg" width="300" caption="" >}}
{{< post-image image="white-lightning-3-original-2.jpg" width="300" caption="" >}}