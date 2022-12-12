+++
title = "Set up Dour-Handed with Active Effects "
date = 2022-12-10T11:42:13+01:00
publishdate = 2022-12-10
categories = ['Tor2e', 'Tutorials', 'ActiveEffect', 'TipsNTricks']
categories_weight = 42
slug = 'dour-handed-virtue'
tags = ['tor2e-system', 'tutorials', 'tipsntricks']
tags_weight = 21
draft = false
weight = 2
+++
Dour-Handed is a starting virtue common to all the culture.  
It gives 2 bonuses
 * +1  [damage to Heavy Blow]({{< relref "#heavy-blow-damage-bonus">}})
 * +1 to feat die for each [Pierce]({{< relref "#pierce-feat-die-bonus">}}) (combat special damage for swords, bows and spears)

Pay attention that in the Alpha release of the pdf rule it was like that, the pierce bonus wasn't present !

**Warning :**  
**This tutorial is compatible with Tor2e v2.0.7 and more.**

## Create the Virtue {#create-base-virtue}

First step create the **Dour-Handed virtue** with value and description. No Active Effect yet. Wait for next steps.

{{< youtube id="UaPzRxkxcvU?start=0&end=47" autoplay="false" title="Creating a standard Virtue.">}}


## Heavy Blow Damage Bonus {#heavy-blow-damage-bonus}

To setup this bonus, you need to add an **Active Effect** to the virtue **Dour-Handed**.  
First, open the Dour-Handed item, go to the **Effects tab** and click on '+'.  
You are about to create a new AE for this Virtue.  
Choose a label to explain what it is for, change the icon for an appropriate one.  

Very Important !! Verify that the **"Effect suspended" is unchecked** and **"Transfer Effect to Actor" is checked**.

After this check, you have to go to **Effects Tab**. In this tab, you will add the dynamic part of the AE; What it has to do !  

**Click "+" :**
* choose from the Attribute Key list : **Heavy Blow Damage**
* Mode should be Add
* Effect Value 1

{{< youtube id="UaPzRxkxcvU?start=47&end=90" autoplay="false" title="Adding +1 to Heavy blow.">}}

This video shows how to do it.

## Pierce feat die bonus {#pierce-feat-die-bonus}

To setup this bonus, you need to add a new **Active Effect** to the virtue **Dour-Handed**. At this point, you should already have 1 AE.
First, open the Dour-Handed item, go to the **Effects tab** and click on '+'.  
You are about to create a second AE for this Virtue.  
Choose a label to explain what it is for, change the icon for an appropriate one.  

Very Important !! Verify that the **"Effect suspended" is unchecked** and **"Transfer Effect to Actor" is checked**.

After this check, you have to go to **Effects Tab**. In this tab, you will add the dynamic part of the AE; What it has to do !  

**Click "+" :**
* choose from the Attribute Key list : **Pierce**
* Mode should be Add
* Effect Value 1

{{< youtube id="UaPzRxkxcvU?start=90&end=137" autoplay="false" title="Adding +1 to feat die for a pierce.">}}

This video shows how to do it.

### Important

For system development purpose, I don't add +1 to feat die but instead I decrease the edge threshold to pass to trigger a Piercing Blow.

## Conclusion {#skill-value-modification}

To create a Dour-Handed virtue with full automation, you have to keep in mind that you need 3 steps :
* [Create a Virtue]({{< relref "#create-base-virtue">}}) 
* Add [Heavy Blow bonus]({{< relref "#heavy-blow-damage-bonus">}}) 
* Add [Pierce bonus]({{< relref "#pierce-feat-die-bonus">}})   

Feel free to play around with the AE, it is a great opportunity of automation but keep in mind it is still a WIP feature of Foundry VTT.