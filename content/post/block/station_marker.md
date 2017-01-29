---
categories:
- Block
date: 2017-01-30T01:45:33+08:00

title: Station Marker
url: station_marker
---

A Station Marker is a block that is usually placed adjacent to a rail, and serves as a destination for carts to route to. By right-clicking a Station Marker you can rename the destination.

If you give multiple Station Markers the same name, carts that are going to this destination have multiple options. When you're holding a Rail Configurator in your hand this is visualized with a green line.

Note that when a cart has multiple options to go to, it will try to go to the closest Station Marker. If there is a red signal in the way to this marker, it will try to go a valid Station Marker that green signals.

# Configuring a cart schedule

Right-click any cart with a Rail Configurator. A window will be shown in which you can configure the schedule of the cart. You can enter multiple names of Station Markers in the world. The cart will then sequentially try to visit these stations. The station the cart is currently heading to is marked green.

# Advanced Routing: Items

By having a destination in the cart's schedule named 'ITEM', the cart will be routed depending on the contents of the cart (only applicable for carts that have an inventory).

Any inventory adjacent to a Station Marker will act as a filter. If any of the items in the cart match any of the items in the adjacent inventory, the cart is allowed to route to this Station Marker. Particles will show when this is the case.

You can configure options about this filtering by right clicking the adjacent inventory with a Rail Configurator. The options available are:

 1. Whitelist/blacklist 

    When whitelist, one of the items in this inventory needs to match one of the items in the cart. When blacklist, none of the items in the inventory are allowed to match.
  
 2. Check damage 
 
    With this you can specify whether or not differently damaged items should be considered as the same, or not.

 3. Check NBT 

    With this you can specify whether or not items with different enchantments should be considered as the same (for example), or not.

 4. Check Ore Dictionary 
 
    With this you can specify whether or not Copper Ingots from different mods should be considered as the same (for example), or not.

 5. Check Mod similarity 
 
    When enabled, carts will be able to route to this Station Marker if one of the items in the cart was added by the same mod as one of the items in this inventory.

Also note that all Station Markers with the same name will share their inventory behaviour. For example, it is possible to have a Station Marker not connected to a rail, with a Chest adjacent to it, just to provide filtering for a equally named Station Marker that is connected to a rail.

# Advanced Routing: Regular expressions

When configuring a schedule for carts, you can simply individually enter the names of Station Markers. However, it is possible to do more advanced things, as in fact, the destination is treated as a [regular expression](http://www.regular-expressions.info/).

Don't worry if this is too complicated. Down below are a few common examples you might want to use:

    leftStation|rightStation 

Either a Station Marker named 'leftStation' or one named 'rightStation' is allowed to be routed to. Note that the '|' is a piping charactor, not a colon.

    Station.* 

Any Station Marker where its name begins with 'Station' can be routed to.

    .*Station 

Any Station Marker where its name ends with 'Station' can be routed to.
