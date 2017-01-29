---
categories:
- Item
date: 2017-01-30T01:44:19+08:00

title: Rail Configurator
url: rail_configurator
---

A Rail Configurator is the 'wrench' of Signals. It can be used to do various Signals-related tasks.

# Configuring cart schedules

By right-clicking a cart with a Rail Configurator in your hand you can configure which destinations the cart should go to. For more info, see: [Station Markers](/station_marker).

# Configuring filter behaviour

Right-click any inventory that is adjacent to a Station Marker to configure its filter behaviour. For more info, see: [Station Markers](/station_marker).

# Visualizing network info

When you hold a Rail Configurator in your hand, any [Station Markers](/station_marker) having the same name will be connected with green lines. Additionally, when you sneak-right click, white lines indicate [Block Signals](/block_signal) that are connected.

# Debugging: Clearing a rail network cache

To make Signal routing perform well, data about the rail network is saved (cached) by Signals. This prevents recalculating important information. A problem that might occur with this is that this information is not properly updated when it should. This would be a bug, information should update properly.

However, if you suspect a system not working while it should, try sneak-right clicking a Rail Configurator. This will clear this cached data of the world you are currently in, and might solve your issue. This could cause a lag spike with big networks, as data will need to be reacquired.