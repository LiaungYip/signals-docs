---
categories:
- Block
date: 2017-01-30T01:45:21+08:00

title: Cart Hopper
url: cart_hopper
---

A cart hopper acts as a Hopper, specifically aimed at working with carts. It has filtering capabilities as well.

# Basic usage

![](/img/cart_hopper.png)

Look at the screenshot below for an example set-up.

The hopper will try to transfer any item from the input inventory into the Chest Cart, provided that the Chest Cart is right under the Cart Hopper. You can transfer items from a Cart to another inventory by placing the Cart Hopper below a piece of track, and putting the inventory below the Cart Hopper.

# Filtering 

Optionally you can attach inventories to the sides of the Cart Hopper, which act as filter. By default the items in the input inventory need to match any item of the filter inventories to be transfered. This can be configured by right-clicking the inventory with a Rail Configurator.

# Redstone behaviour

You can change when carts are allowed to continue on their way by right-clicking the Cart Hopper. You can toggle between the following modes:

 * No activity - Emits a redstone signal as soon as items stop transfering.
 * Never - Never emit a redstone signal.
 * Cart full - Emits a redstone signal as soon as the cart's inventory is full.
 * Cart empty - Emits a redstone signal as soon as the cart's inventory is empty.

# Targeting a Cart Engine inventory

A Cart Hopper is a perfect way to manage fuel you want to insert into a Cart's Cart Engine. By right-clicking the Cart Hopper and toggling the interaction behaviour to 'Cart Engine', items will only be transfered between the inventory and the Cart Engine.