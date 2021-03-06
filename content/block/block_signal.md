---
categories:
- Block
date: 2017-01-30T01:45:16+08:00

title: Block Signal
menu:
  main:
    parent: 'Blocks'
---

A Block Signal is a block used to control rail traffic on a rail network. If you are familiar with either OpenTTD or Factorio rail signaling, you will know how this works.

In the screenshot below a simple system is shown with three Block Signals:

![](/img/block_signal.png)

These block signals divide the track into three different 'block sections'. These are marked with different colors of wool. Signals make sure that only one cart is allowed on a section at a time. The signal will only turn green when the next section is free.

In the situation in the screenshot you can see that the cart in the top is held by the signal, because another cart is still on the red section (note that the carts are traveling counter-clockwise).

When signals are green, they emit a redstone signal. This usually can be used to activate powered rails right next to the signal.

When signals turn green, they additionally give a nudge to carts next to the signal. This nudge reaches up to 5 rails in front of the signal. This is however limited to the track type used next to the Block Signal. To make it more clear, in above screenshot, the nudge will only be applied to carts on the powered tracks next to the signal, it will not reach to the normal tracks before that.

The purpose of the nudge is to make the cart go when standing still on powered rails.