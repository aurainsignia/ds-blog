---
title: 'Starting Development & Progress'
date: '2025-07-03T01:31:56.041Z'
author: Aura Insignia
summary: "Dead Reckoning's first development steps."
draft: false
---

{{< center caption="Average session of s&box development" >}}
![s&box Meme](/images/article2/s&boxmeme.gif)
{{< /center >}}

## Introduction

It's been a long time since the last article. In this post, I want to bring everyone up to speed with how development has been going and explain how certain systems are being implemented in the game.

## Development Progress

This section will be somewhat technical. In summary, the core gameplay loop has been finished and I'm now focusing on finishing the player HUD systems. Though, I am a bit unsatisfied with the current speed of development. Those uninterested in the process details may continue to [→ Development Reflections So Far](#development-reflections-so-far).

### Round Manager

In general, learning C# style, features, and the s&box engine has been less stressful thanks to ChatGPT (o4-mini-high) and support from the [s&box discord](https://discord.gg/4uBn2StNkV). ChatGPT is also pretty great at pointing you in the right direction if you're stuck thinking about how to do something in a particular way. For example, using a state machine implementation as the algorithm for the round manager logic was an idea suggested by ChatGPT. This seems like an obvious solution in hindsight, but I'm pretty inexperienced with system design, so it wasn't immediately obvious to me. 

{{< center caption="A snippet of code logic showing off the state machine of the Round Manager component." >}}
![Missing ](/images/article2/roundmanagerlogic.PNG)
{{< /center >}}

The only other interesting thing about making the Round Manager was probably making the state timer. I wanted to make sure that the timer was based off of the passing of ingame time on the server rather than real time. It's important to make sure the timer is in sync with the game server's state so server lag doesn't desync the timer and gamestate. This was implemented by taking desired timer duration and subtracting the time between server frames from it every frame. Implementing it this way, while not as simple as using a native system timer, allows the timer to stay in sync with the game as it naturally experiences computational hiccups.

{{< center caption="The state timer algorithm." >}}
![Missing ](/images/article2/statetimer.png)
{{< /center >}}

### HUD Manager

Once I started working on the HUD, I ran into my first real system design challenges: how do I transfer data between these systems and how do I enforce their initialization order? I need to get information from the round manager to draw onto the player's HUD, like the current wave and wave timer. But, I also need to make sure that the Round Manager is initialized *before* the HUD manager tries to grab data from it, or else we'll run into null pointer errors. I ended up solving this by reimplementing Round Manager as a singleton with a static reference.

{{< center caption="The RoundManager singleton implementation." >}}
![Missing ](/images/article2/debugging%20singleton%20null%20ptr/image.png)
{{< /center >}}

Solving this system design problem also taught me a bit about how dependency management is accomplished in s&box. In a nutshell, s&box uses a hierarchy of **GameObjectSystems**, **GameObjects** and **Components** that are a part of the game's **Scene** (map).

```
Scene
├─ GameObjectSystems (global singletons)
└─ GameObjects
   └─ Components
```

  **GameObjects** are data structures for objects in the scene and **Components** are behaviors and/or data that can be attached to them. **GameObjectSystems** are instantiated on your game's initialization and act as global singleton GameObjects. Since my implementation of `RoundManager` is a Component (needed for the `Component.Task.Frame` function), it needed to be attached to an object to be accessible. Once I understood these hierarchical patterns, I was able to properly implement HUDManager's access of the RoundManager's component data via attaching it to the game manager (a GameObjectSystem) and grabbing it as a globally visible field.

{{< center caption="Attaching the RoundManager component to the game's manager." >}}
![Missing ](/images/article2/debugging%20singleton%20null%20ptr/connectedcomponent.png)
{{< /center >}}

{{< center caption="RoundManager.Instance is now accessible by HUDManager, hoorah!" >}}
![Missing ](/images/article2/debugging%20singleton%20null%20ptr/image2.png)
{{< /center >}}

### Development Reflections So Far

I've had about two months of development time now and I still haven't really covered much ground yet. The main reason is because I've spent a large portion of that time learning about the new tools and technologies that I'm working with. Hopefully as I become more familiar with them, my productivity should also increase correspondingly.

It's also worth noting I spent about two weeks of that time playing the [Apogea](https://www.apogea.online/) playtest. I am not affiliated with them in any way, but I had a lot of fun and highly recommend it for anyone looking for a hardcore MMORPG experience that isn't modern profit-driven slop. 


## Conclusions and Discord Server Reminder

If you're wondering where you can get the most up to date information about this game, we have a community discord server that I post news announcements to. [You can join through this link](https://discord.gg/xcP27ZPbt2). **Please be aware that this is an 18+ discord server and minor persons are not permitted. Do not request to join the server if you are a minor.**

In the future, I will be opening up a suggestions channel where server members can submit their feedback and suggestions to improve the game.

The next article I publish will most likely be a roadmap that will be periodically updated and serve as a visual guide to the current status of game's development. This roadmap will be linked in the discord for future reference and will also be pinned on the blog's homepage.