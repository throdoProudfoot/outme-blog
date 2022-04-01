+++
title = "How to setup 1-hand and 2-hands weapons"
date = 2022-03-31T11:42:13+01:00
publishdate = 2022-03-31
categories = ['Tor2e', 'Tutorials', 'Personal Characters', 'TipsNTricks']
categories_weight = 42
slug = 'one-hand-two-hands-weapons'
tags = ['tor2e-system', 'tutorials', 'tipsntricks', 'pcs']
tags_weight = 21
draft = false
weight = 2
+++
A quick blog post today about a question I often see on discord, facebook, ...

> How do I setup weapon that can be used in one hand or two hands like longswords or spears.

The main problem is the difference between stats when you use the weapon with one hand or two hands. And the system doesn't have any way to have different stats in the same weapon depending on how mane hands you use.  
You have to find a workaround

## Setting up the system to handle weapon usable both in one-hand and two-hands {#setup}

It is quite easy to setup TOR for one hand/two hands weapon like spears. you have to use 2 items (one for one hand and the other for two hands) and the trick is to change the load of one of the 2 items to 0 in the character sheet.

{{< youtube id="R_Qo5MKbs2U" autoplay="false" title="Setting up TOR system for one hand/two hands weapons.">}}

### Note

The best way is to change the load of the item in the sheet as Foundry VTT does copy of the item when you drop the item in a sheet so the original item is not updated. This way you always the right stat for the reference item and you only change the instance of the item in the sheet.

## Conclusion {#conclusion}

To have a really neat and clean way to handle this feature in TOR would mean a lot of code and complexity, it would be over engineering to do it so I chose not to do so and use this workaround. 