---
title: Dev Blog No. 0
date: "2025-05-10T18:46:31+00:00"
author: Aura Insignia
description: The first development blog post.
draft: false
---

## Introductions

Hello everyone. This is the first article of a new development blog I'm starting to publish status updates about the game I'm developing, Dead Reckoning. This first post will be longer than most and serve more as an initial informational source, covering:

- what Duskwave Studios is
- what Dead Reckoning is
- some information about my background
- currently planned features for the prototype
- currently planned features for the full release
- the development timeline
- various screenshots
- miscellaneous information

In the future, you can expect posts to be shorter than this one. Additionally, I plan to eventually use this website for publishing other DR-related news like event dates and descriptions, patch notes of major updates to the gamemode, continual Q&A, and more. But for now, it'll just be a blog for anyone who is interested in following along the initial development progress of Dead Reckoning.

---

## Introducing Duskwave Studios

![logo](/images/logo.png)

*I'll probably be cleaning up this logo at some point...*

Duskwave Studios is the name of the organization and development team for my game, Dead Reckoning. It currently consists solely of myself. However, if enough interest in the game exists, I plan on opening the project up for collaboration with other developers and community members sometime in the future.

Additionally, there's an invite-only discord server where you can find more information about the game and socialize with community members. At the time of posting this first article, the server is open to those who might be interested in playing dead reckoning. The invite link can be found [here](https://discord.gg/MrP5nTvjC3). *Also, please be made aware that this is an 18+ server and minors are not permitted.*

---
## A Successor to Zombie Survival: Dead Reckoning

![cat](/images/cat.jpg)

*I don't have a picture of what the game will look like yet, so have a picture of this cat instead.*

Dead Reckoning will be an FPS RPG based on the [Zombie Survival](https://github.com/JetBoom/zombiesurvival) gamemode from Garry's Mod 10 using Source 2 in [s&box](https://sbox.game/news/) and redesigned to include my own ideas. You can think of it as a spirital sucessor to that gamemode but under a different developer and a newer platform.

### The Basic Game Loop

The basic game loop will be mostly the same as the original, so those who played that can skip this section. 

Like the original, it will consist of rounds between two teams fighting: Humans and Zombies. At the start of the round, you spawn on the Human team in one of many maps with resources scattered all around. You will have a small time period to gather resources and build barricades on the map to defend teleporters before many waves of zombies start spawning. Humans must purchase various weapons and upgrades with points gained from killing zombies and surviving in order to fend off the increasingly difficult waves. If you can survive until the end of the last wave, you can take the teleporter with any other survivors to escape from the zombies and win the round.

Alternatively, humans who die will succumb to the infection and become zombies. Zombies must kill all players on the human team by breaking their barricades and mauling them to death. Zombies have many class mutations to choose from that unlock as the waves progress. If the zombies manage to kill every human before the end of the last wave, then the zombie team wins.


### Direction Changes

Unlike the original, I plan on having this game scaled from the get-go. There should never be less than 20 zombies that the human team is fighting (except for edge cases like there being less than 5 players on the server). Zombie bots will fill in the places of missing zombie players and will be added or removed dynamically as players join to avoid shifting the advantage too much towards the zombie team. This doesn't mean there will be a constant number of zombies on the zombie team, but rather a variable *minimum* number. This avoids needing to balance around small zombie team rounds and helps make the gameplay more engaging.

Additionally, I want the game to support all styles of play. In the original, you could get away with casually playing the game, but could often die from various mechanics if you weren't careful. So you either had to lock in or risk dying and waiting until the round ended for another chance to play as human. I don't want to lose that sense of risk with DR, it's important and has its place. However, there will be features in this game that will be fun for both casual *and* hardcore styles of gameplay. There's already a lot of info here, so I'm going to elaborate more on what I mean by this in future blog posts.


---
## The Development Timeline and Release Schedule

![garrymoment](/images/garrymoment.png)

*The woes of s&box development.*

There will be two milestones of development: establishing a prototype and then the full release of the game. The prototype will be a skeleton version with only the essential basic systems implemented for internal testing, although I may open up a closed testing period to the community at some point for help and feedback. After the prototype has been tested and polished, I will move on to develop the full release version of the game, which will have all of the planned features fully implemented.

In a nutshell, this is going to be one of those "it takes as long as it takes" projects. I work fulltime and plan on spending only some weekends and some weekday evenings working on this. That, and s&box seems to release many updates that require its gamemodes to be refactored (see the above image). With these things in mind, unofficially, I'm aiming to have the prototype finished within a year and then the full release within one year of that. These are not guarantees, only goals. There's simply too many unknowns to give a truly accurate estimate. Just keep in mind, one way or another we'll get there. And then we'll have a fun, non-shit game we can play together.

---
## Planned Features

![youtrack](/images/youtrack-board.png)

*A preview of the currently sparse project board.*

Dead Reckoning is going to have all of the core features of the original game with additional features and systems added by myself, with some of the more mundane mechanics reworked. While I don't have any concept art available yet since it is still very early in development, I will be sharing early screenshots of features in development in following blog posts in the coming months, as well as elaborating on what each of them do. Many will be very similar or the same as their equivalent systems in Zombie Survival.
### Prototype's Features
- Ingame Wikipedia
- Barricade System
- Teleporter System
- Player Chat, Voice Chat, Sound Emotes, and Emojis
- Human (Level) Skill Tree
- Human Round Loadouts
    - Perks, Trade-offs, and Sacrifices System
    - Starting Items
- Tier-based Shop System (Humans)
    - Weapons
        - Melee, Shotguns, SMGs, ARs, Snipers, Explosives, Projectiles
    - Tools
        - Hammers, Medical Kits, Repair Fields, Shields, Turrets
    - Throwables
        - Grenades, Throwing Knives, Concussion Grenades
- Zombie Bots (AI)
- Wave-based Zombie Classes
- Zombie Upgrades Shop
- Baseline Cosmetics System
- Currency System
- Knockback System
- Status Effects
- Scoreboard
- Player Profiles
    - Sprays
    - Game Settings
    - Tracked Player Statistics
- Award System
- 10 Maps
### Full Release's Features
- Optional Newbie Tutorial
- Dynamic Difficulty System
- Dance Emotes
- Bonus & Super Bonus System
- Minigame System
    - Fishing
    - Mining
- Secret Shop
- Zombie Bosses
- Additional Zombie Classes
- Additional Human Tools and Weapons
- Optional Wave Intermission Objectives
- Censorship Policy Settings
    - NSFW
    - SFW
    - Streamer Mode
- Player Leaderboard
- Announcer Voices
- Cooldown Area
- Other Experimental Ideas

Besides these features, the gamemode itself will need to be created. Many less-interesting things not mentioned here will also be included like the player HUD, the game loop, inventory system, and other fundamental modules of the game. Additionally, more features will be planned and added along the way as well.

---
## About Me

{{< youtube o3dFsUpNt5U >}}

*Some footage of me playing [Midnight Zombie Survival](https://midnight.cat/) (low population)*

For those who don't know me, I am a long time player and fan of the original game, Zombie Survival hosted on NoxiousNet way back in the mid 2000's. I have over 10k hours spent playing ZS and spend most of my free time gaming. My development skills come from my education (computer science degree) and career working full time as a software developer (not in the gaming industry). This project is going to be my first time delving into game development though, and I plan on taking my time and doing it right.
#### Development Motivations
As for why I'm making it, there are several reasons.

1. The modern gaming industry is becoming shit and prioritizing capitalization over quality.
2. The gameplay of classic Zombie Survival is becoming stale and oudated compared to modern games.
3. I want a new game to play that's just as fun or better than ZS.
4. I want the game's community to not be burdened by poor management.

Developing the game myself fixes all of these issues and also satisfies a long-term goal I have had since being a teenager. It just makes sense.

---
## Miscellaneous Information
Below are some other pieces of information that I couldn't find a good fit for in the other sections.
#### Licensing Restrictons
Unlike the original, Dead Reckoning will not be able to use the assets from various source games, including the main one, Half-Life 2. The original game had Half-Life 2 assets available for developers to use due to the unique licensing contract Valve has with Garry for Garry's Mod. However, S&box lacks that contract, so Dead Reckoning will need to have its assets sourced from other avenues. Whatever assets I end up using, I will try my best to keep them as similar as possible to the original ones used in Zombie Survival while still following the law.
#### What is a "Duskwave"?
In short, a single wave of "dusk" can be observed carpetting the planet during solar eclipses, which, historically, are thought to symbolize major changes  . Basically, the idea is that Duskwave Studios is a symbol of change, with its games contrasting against the many mediocre publishings of the modern gaming industry.

---
## Final Notes

I'm looking forward to watching the community grow as development inches towards the first milestone. I hope I can build a game that we can all enjoy and that provides a modern, high-quality gaming experience. Otherwise, that concludes this first post. I apologize if it's a bit disorganized, wordy, etc. I'm hoping I get better at writing these as I make more of them.

I'll be seeing you guys in the discord and on zombie survival. 
![snake](/images/respects.jpg)
See you next post!

*Do you have questions? Feel free to ask them in our discord! I'll be curating an FAQ from them that will be in the next post.*