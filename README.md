# Etherlords II map
During our childhood, my brother and me played a lot of Etherlords I+II.
We recently rediscovered the game and decided to develop our own map.
The map started out as a small project for ourselves, so we kept the in-game text in our native language - German. It's not a big deal if you do not speak German: all important (=non-story) dialogues are described in the all-caps section `MUST-READ FOR NON-GERMAN SPEAKERS` (at the bottom). If you do not speak German, you should definitely read this section before you start playing.

Our idea was to offer more power to the players - e.g., higher levels, some spells from other races, and more artifacts than usually available in the mainline campaign; at the same time, we wanted the map to contain challenging and unique fights.
**The campaign has to played on hard difficulty. Monsters will have no spells on easy and medium difficulty!**

We hope you enjoy our map as much as we do. We appreciate any kind of feedback :)

## TL;DR: Features of the map
Here are some information about the map:
- story roughly similar to the Etherlords II campaign, but in a single map
- around 100 monsters, probably a few more
- without "Learning" proficiency, you can reach level 17 before fighting the final boss
- playable with all 4 races. Till around lvl 6, every class has its own starting area, afterwards they use the same paths
 - when playing with a certain race (e.g., kinets), you will mostly find spells from that race, but - depending on your current location - may occasionally find spells from other races
- randomized loot: upon defeating monsters, you will be rewarded with some new spells, which are drawn randomly from a predefined pool
  - each spell can drop at most 3 times, if you want a fourth copy, you will have to buy it in a shop
  - there are two loot system implementations. Upon starting the mission, the game will prompt you to choose one of them (see Loot system choice)
- unique fights due to shrine effects - throughout the map, you will encounter some of the combat-influencing shrines from the Etherlords II campaign (e.g., the aviak shrine gave +2 might, restless and beserk ability to each aviak). Those shrines will affect you only for one fight (and are usually beneficial for the monster guarding the shrine). You cannot get them permanently
- up to a certain point (lvl 14ish), monsters behave as you expect them to (typical spells, and only spells from their own race). Around level 14, however, you will trigger paleness. Monsters in pale areas may be more unfair and use spells from multiple races
- artefacts - as you progress through the game, you will obtain most of the classical artefacts. Choosing the "Artificer" proficiency on leveling may be well worth it
- the final boss has two different decks. Each time you attack him, he will randomly choose one of it. Beating one of the decks is sufficient to win the mission; however, if you like challenges, try to find a deck that can defeat both decks of the final boss without changing any spells. Even harder, try to use only the spells of your race (no pale spells either). We had a hard time, but it can be done!

## Installation
The installation is really easy.
Open your Etherlords II folder (we use version 1.03, but others should work as well).
It contains a folder `Maps`, which again contains a folder `Custom`.
Download all the [files](archive/master.zip) and put them into the `Maps\Custom` folder (all of them).
Afterwards, you can play the mission by selecting Single->Mission->New and then choosing the variant you want to play.

If you have any troubles with the installation, don't hesitate to contact me or make an [issue](https://github.com/aloeser/Etherlords2Map/issues).


# Some thoughts on game design
In general, this map is supposed to be hard.
We want to encourage the player to think about how to defeat a monster, and to come up with a play style that is effective against that certain monster.

At the same time, we want our map to be playable with all 4 races.
Achieving a good balancing for a single race is hard enough.
Achieving a good balancing for all 4 races (they will fight the same monsters from level 6 onwards) is almost impossible.
Consequently, some monsters may be quite hard with, e.g., kinets, but really easy with, e.g., all the chaot's creature killing spells.
During playtesting, I managed to defeat each monster with each race while only using spells of my own race (i.e., simulating no lucky spell drops from other races), so I believe that the monsters should not be too hard. (Not winning in first attempt does not make a monster hard :D)

## Reason for allowing only hard mode
Our mission **can only be played in hard mode**, but not easy or medium mode.
**Monsters on easy or medium mode will have no spells**.

The main reason for this decision is that we wanted to add a lot of monsters, while keeping the player on a reasonably low level.
Keeping the player on a low level requires low level monsters (usually around 1-2 levels below you).
At the same time, we do not want the player to get ethers (much) faster than the monster, rather the other way round; nor do we want the player to have (significantly) more health than the monster.
We believe that playing in hard mode is a good way to combine those requirements:
We can give monsters a high health to compensate for their lower level, and boost their ether generation via difficulty (on easy mode, monsters do not get ether as fast, I believe).

## Further development
At the moment, we consider the map as finished and do not plan further development, except of fixing potential bugs.

If you want to translate the map to some other language, please contact me before you start.
At the moment, all dialogue strings are hardcoded in German at the place they are used at, i.e., if someone wants to change the language, you will have to touch hundreds of lines throughout the entire script.
I consider that somewhat ugly, but sufficient if there is only one language in the map.
If someone wants to translate the map, I'll build an internationalization system, so that multiple languages can coexist and you can choose your language in game.
It's not hard, but without knowing if anyone will ever translate or even play this map, the refactoring effort seems not worth it to me.


# Acknowledgements
I would like to thank Sebastian 'The Argh' Mordziol, the creator of the [Ether Planes website](http://etherplanes.net), for providing an online reference of the spells and their codes.
Setting up the available loot would have been much more painful without this reference.

Further, I would like to thank @Bonesnake for providing the [Roguelike map](https://github.com/Bonesnake/etherlordsII-roguelike-map).
When I found the map, I was amazed by the possibilities it showcases, such as random loot generation, changing the available shops, etc.
Seeing this map motivated me to do some experiments with the scripting myself.
While only very few elements of the roguelike map are contained in the current version of our map, it was definitely an inspiration for me and made it easier to get into Etherlords' scripting API.


# Known technical issues
To the best of my knowledge, the map contains no game-crashing bugs.

Occasionally, after activating paleness (which will happen at some point in the story), I have encountered a visual bug where the ground tiles are black rather than having their actual texture.
Sometimes, saving and reloading the game helps.
I do not know where this bug came from, nor how to reliably fix it.
It might be a general bug in Etherlords, and not specific to the map, but I can't say for sure.

## Bug reporting
If you should encounter a bug, be sure to make an [issue](https://github.com/aloeser/Etherlords2Map/issues).
I'll try to fix it as fast as I can.

If it's crashing with a "script error" (it should not, but who knows..), it would be great if you could upload/paste the `script_err_log.txt` file found in your Etherlords II folder.
It contains a stack trace, which will help me locate the error.


# MUST-READ FOR NON-GERMAN SPEAKERS
While the scripting of the campaign is done in English, all (story) dialogues and player interactions are written in German.
The following sections provide an overview of all important dialogues.

## Loot system choice
When you start the mission, you will be asked to choose which loot system you want to use.
In general, the loot (spells) are not fixed per monster, but rather drawn randomly from a predefined pool of spells.
There are two versions of the loot system:

- The classical version draws a certain number of spells. Press "yes" if you want to play with the classical system
- The choice version gives you the following choice after each fight: It presents you with a set of spells that you would get as loot. You can choose to accept those (pressing "yes" at the dialogues after a fight), or you can choose to reject them. If you reject them, the system will select some (probably) different spells, which may suit you better, or not. When you reject, there is also a small chance to receive less spells than before. When you did not receive a spell from another race, you cannot receive it by rejecting the loot either. Press "no" if you want to play with the choice version

## One-way teleporters
When using teleporters, some dialogue may pop up.
This dialogue informs you that you cannot return if you use the teleporter, i.e., that the teleporter is one-way.
Press "yes" to use it, and "no" to cancel.

## Lottery system
As you progress you will encounter traders.
They offer you some kind of lottery system: You can pay their price to obtain a spell from another race (randomly drawn from a predefined list).
You can buy at most 3 spells (or later: one artifact) per trader.
The second purchase will be twice, the third thrice as expensive as the first spell.
If you attempt to buy more than 3 spells, you will only get a sold-out message.
If you cannot afford a spell due to lacking resources, the trader will tell you which resources you lack.

In the later parts of the game (lvl 15ish), there also is a trader that sells artefacts instead of spells.

## Paleness / Colorlessness
At some point in the story line (lvl 14ish), the antagonist will unleash paleness.
The disturbances of the ether streams might make the monsters you encounter more dangerous, e.g., by allowing them to use spells from different races (which does happen before, but way less frequently).

## Story
**This paragraph contains spoilers about the story. Do not read it if you do not want to be spoilered.**


In general, the story is heavily inspired by the Etherlords II campaign.
Our mission is not really a prequel or sequel, but rather parallel to the campaign.
In the campaign, each race has a certain holy shrine - e.g., the vitals have the source of life.
At the beginning of our mission, you will witness someone stealing the shrine.
You decide to chase the thief.
Unfortunately for you, the thief can open (and close) gates at will, while you have to find the corresponding key first.
From time to time, you will catch up to the thief, and he'll run away, again.
At some point, you will recognize the antagonist as the White Lord.
If you become too strong, the White Lord will unleash paleness to weaken you.
The paleness will stay for the rest of the mission, but you will occasionally have access to ether nodes that restore you to full health.
After defeating the White Lord for the first time, you realize that all you saw and defeated was his projection, as he is hiding in the outer planes.
You win the mission if you can beat him in the outer planes.

