+++
title = "Active Effect for Piercing Blow"
date = 2022-01-10T11:42:13+01:00
publishdate = 2022-01-10
categories = ['Tor2e', 'Tutorials', 'ActiveEffect', 'TipsNTricks']
categories_weight = 42
slug = 'fell-active-effect'
tags = ['tor2e-system', 'tutorials', 'tipsntricks']
tags_weight = 21
draft = false
weight = 2
+++
Lots of systems, having an item (magical or not) can modify the characteristics of a Hero or an Adversary. In Foundry VTT, it is possible to have this automation using Active Effect. In this article I will show you how to automate the modification of the Piercing Blow modification using a Fell Weapon (Reward).  
I will tell you how to do it, how it is working and also what is the limitation (TOR2e system).

## Attacking with a standard simple weapon {#standard-weapon-attack}

With this weapon, no active effect, you can see that the piercing blow threshold is 10 (which is the standard value). No modification at all whatsoever.

{{< youtube id="eWvb6psgYDk?start=0&end=39" autoplay="false" title="Standard Piercing blow with a simple spear, no active effect.">}}

With a standard weapon equipped, the system will try to beat 10 on the feat die to trigger a piercing blow.

## Attacking with a fell weapon {#fell-weapon-attack}

A fell weapon (one of the reward available to player in the Core Rules), this weapon has a special capacity, it triggers a piercing blow on a 9+ (9, 10 and Gandalf Rune for Character and Sauron Eye for Adversary) instead of 10.

{{< youtube id="eWvb6psgYDk?start=40&end=124" autoplay="false" title="Piercing blow with a fell spear, one active effect.">}}

With a fell weapon equipped (a weapon with an active effect Fell), the system will try to beat 9 on the feat die to trigger a piercing blow.

But ... How to create such Active Effect in Tor2e ? (please read next paragraph).

## How to create a Fell Active Effect {#fell-active-effect}

In the video below, you can see how to create such active effect but before, you **have to know** a few things about active effect and Foundry VTT.

### Note

First of all, you have to add the active effect on an item in the **Item Sidebar**, you can't modify an active effect in an item embedded in an actor (actor is the FVTT term for characters, adversaries, npcs, ...).  
Secondly, please notice, active effect are not items you can drag'n drop on an item/actor, you need to add it using the active effect tab in an item sheet.

### Add an active effect to the item

So to add an active effect, you need to go to the sidebar and open the item sheet you want to modify, then you go to the active effect tab in the sheet. In the active effect tab, you have to click on the **"+"** on the sheet.  
A customization popup appears on the screen to set up the active effect data. You will have to fill some of the fields to make it work !

#### Important

To have an active effect active in your sheet, you need to uncheck the **"Effect Suspended"** checkbox. If you forget to uncheck this checkbox, that active effect will have **NO EFFECT** in your actor !  
In fact, this checkbox is used by FVTT to know the effect should be suspended (so not active) or if it should be actve (this is what we want).
This is **mainly the source of error and mistake** when you create your active effect, it is not working.  
Often You forgot to modify the checkbox so it is doing nothing !

### Create an effect in the Active Effect

Once, the item has an active effect and this active effect is not suspended (so it is active), you need to create an effect. To do so, go to the **Effects** tab and add an effect using **"+"** icon. The effect has some data to specify (Attribute Key to modify, Method of modification and Value).

For our Fell Active Effect purpose, you need to choose :

* Attribute Key --> Weapon Piercing Blow
* Change Method --> Downgrade
* Value --> 9

{{< youtube id="eWvb6psgYDk?start=52&end=73" autoplay="false" title="Creating a Fell Active Effect.">}}

Now if you test, you should have the expected result, triggering a piercing blow on 9. But if you look closely, you can see a little issue (see below for explanation).

## Current Tor2e System limitations {#current-tor2e-system-limitations}

If you look at the video until the end, you will notice that if you have an item with a Fell active effect, even if you don't attack with the weapon, or you even don't have the item equipped, the piercing blow threshold is downgrade to 9 which is wrong ! The system shouldn't modify the piercing blow threshold.  
I have a solution to do it correctly, but I haven't coded it yet so ... for now, you need to modify the sheet, deleting the item or keep in mind and compute the proper value of the threshold in your head.

{{< youtube id="GQ88-2Yo-v0?start=133" autoplay="false" title="Fell Active Effect Limitations">}}

## Conclusion {#skill-value-modification}

To create a Fell Active Effect, you have to keep in mind [how to do it correctly]({{< relref "#fell-active-effec">}} and to know some [limitations]({{< relref "#navigating-between-input-fields">}} of the system.  
Walking through the active system attribute key list, you notice there is some attribute you can change, I also will add new later on. You can play with all the attributes but keep in mind it is a WIP feature that will evolve and it is not perfect.
