# Project 2 Research: AI RPG Design

I am [Jan Adell Mill](https://www.linkedin.com/in/jan-adell-mill-41a5341a3/), student of the [Bachelor’s Degree in Video Games by UPC at CITM](https://www.citm.upc.edu/ing/estudis/graus-videojocs/). 

In this research document I'll be taking a dive into the design of AI in RPG games (as well as some general analysis) in order to define the guidelines in which we, as developers, want to implement the AI in our game so as to make the most use of it.

This content is generated for the second year’s subject Project 2, under supervision of lecturer [Marc Garrigó](https://www.linkedin.com/in/mgarrigo/).

# Summary

[Introduction](#intr)

[RPG Games](#rpg)

[AI Design](#aides)

[AI and the Player](#aiplay)

[AI in RPG Games](#airpg)

[Thoughts and Concluding Statement](#resum)

[Sources](#sources)

<a name="intr"></a>
# Introduction

AI is, in general, an element used in videogames in order for game entities to accomplish functions in a more human-like manner, or more precisely, a manner which makes it seem like they're alive (since not every NPC is a human or supposed to act human-like). NPC's actions, being allied, enemy or neutral, are all controlled by AI. 

However, as we will see in this document, AI is an element not only used to give a sense of realism to entities and characters in our RPG games, but a game feature which, when used properly, can be useful to enhance the experience in certain manners game developers see fit.

<a name="rpg"></a>
# RPG Games

Role Playing Games (RPG in short) are a genre of videogame based on having the player participate in a story, in which they progress, grow and become more powerful as time goes on and they advance further into the narrative. 

RPGs have been defining the videogame industry from it's very core since the very beggining, serving as examples for many other genres on how to apply certain features and mechanics, mainly progression and character growth. It's important to keep that in mind as we speak of AI, since, as the player grows, we need the environment around them to do as well. 

AI in RPGs is an important factor due to one main reason (which doesn't always apply): The amount of NPCs we find in them. From regular NPCs we find at towns or taberns, to allies or enemies in battle, all of their actions are controlled by AI created by the developers.

Not only that, but since RPGs have a vast amount of subgenres, and within them playability is usually different in a fundamental level, we have to design our AI so it fits within the game. 

![Octopath Traveler Combat](https://raw.githubusercontent.com/JanAdell/Project-2-Research-Ai-RPG-Design/master/Research%20References/Website/octopathbattle.gif)
> Octopath Traveler

<a name="aides"></a>
# AI Design

AI Design is used, in general, to try and boost the immersive capabilities of a game in order to bring the player to feel or live the narrative and universe in a more geniune manner. This is attempted to do by making responsive AI which brings life to the game, and gives it a more organic feeling. NPCs in cities talking and reacting as the player passes by, enemies with multiple patterns or unpredicability and companions which support the player through the game are all ways in which AI can help accomplish this previous mentioned organic feeling.

AI Design is partically important in RPG games, since as they're usually based on progression and narrative, we need the AI to grow in parallel to the player. 

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/GrotesqueKaleidoscopicIndianspinyloach-size_restricted.gif?raw=true)
> Monster Hunter: World - Iceborne. A palico reacting to their hunter being staggered by helping them.

## Different kinds of AI

AI in videogames comes in many different forms. While it can certainly be programmed as to act purely as human-like as possible, AI is a tool for developers to make the player and the world interact in a more immersive manner, making it versatile when it comes to possible paths to take when implementing it. 

* **Non-Adaptive AI**

AI which has a defined set of rules, being more or less complex, by which it acts and reacts to whatever is happening. 

This kind of AI is probably the most used nowadays, since it allows the designers to control NPCs actions within expected parameters, thus avoiding possible problems by being able to forcibly define how the entity acts. 

* **Traits**

A concept mainly popularized by The Sims, this is based on having various Non-Adaptive patterns of behaviour in an entity (sometimes placed randomly) in order to create a form of Non-Adaptive AI which feels more random and natural, also allowing for the creation of characters with more defined personalities. 

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/sims.gif?raw=true)
> Sims Medieval, a game which took the Sims 3 system and made it an RPG

* **Adaptive AI**

A type of AI which learns through data in order to optimize and adapt itself. Nowadays it's mainly used in MMORPG games in order to teach NPCs certain player-related actions which are hard to define by the developers inside an AI system. 

In the future, this kind of AI might be used to create more personal experiences catered to each individual player, allowing the AI to recognize patterns within a players playstyle and then interacting with them in a suitable manner. 

Even though we have the technology to allow the AI to learn, this method will, most likely, still take a few years to become something we see in our RPG games, since developers have few tools to manage all the possible interactions created from learning, as well as few ways to regulate such way of learning. 

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/wf.gif?raw=true)
> Warframe taught AI how to wallrun from player collected data (figure shows regular gameplay)

### Concerns within AI Designing

Our main concern when designing AI is that the AI we designed is not correctly fullfilling it's role. For example, if we have an enemy NPC which is designed to be fairly easy, but a majority of players are deeming it a hard, our AI is not working as intended. There are also problems related to the code defining the AI, mainly when relating to pathing, but those are normally outside design capabilities.

## Enemy AI

Enemy AI or enemy NPCs are probably were we will find the most freedom when it comes to designing, since many things can be expressed depending on how it is done. 

First and foremost, designing and balancing en enemy in an RPG is subjective, since there can be many factors that define said balancing process. When designing any kind of enemy in general, several key points can be made to use as guidelines during the process.

* **The mood**: The mood refers to the feeling we want to give off by certain behaviours by the AI. Normally in accordance to the general mood of the game. A good example of implementations based in mood can be found in the **Souls** franchise, where enemies, as soon as they notice the player, start the slow burn pursuit towards them.

![](https://raw.githubusercontent.com/JanAdell/Project-2-Research-Ai-RPG-Design/master/Research%20References/Website/PowerlessLeanAlpaca-size_restricted.gif)
> Dark Souls

* **The difficulty**: Difficulty refers to how, through stat tweaks and behaviour design, we can make an enemy more or less hard to deal from the player's perspective. A pretty good example of this implementation can be found in **Monster Hunter: World - Iceborne**, where a same monster in different difficulty categories (Low Rank, High Rank and Master Rank) has substancial fluctuations in both damage output, effective health and behaviour patterns (being easily angered as rank gets higher). This also feeds into the proposition of the AI growing as the player does, since the player unlocks higher play ranks as he moves forward through the story.

Even though making an AI difficult can feel rewarding to some players, we should always remain in a terrain which involves no frustration for whoever is facing it.

* **The behaviours**: We refer to behaviour when talking about how the AI reacts. Inicial raction time, as well as actions taken in response to external changes, are actions defined in an NPCs behaviour, and a core part of the concept we know as AI. A good example of behaviour which is easy to notice takes place in the **Pokémon** franchise, where enemies will use healing items or abilities as they detect their Pokémon loosing health.

![](https://raw.githubusercontent.com/JanAdell/Project-2-Research-Ai-RPG-Design/master/Research%20References/Website/giphy.gif)
> Pokémon Red

* **The purpose**: We refer to purpose in AI the same way we would refer to any other game feature. We ask ourselves why do we need it, and what objective do us, as the developer, wish to accomplish with it, as well as what results we want to get from the player encountering it.

A clear example of purpose within an NPCs can be found in Claptrap, from the **Borderland** series. From the moment he's introduced in the tutorial of the first game, we can feel what the experience will be about. Over the top, roudy, sensless action. His mannerism, his movement, his way to speak, and this belief is further complimented when advancing throughout the game.

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/giphy%20(1).gif?raw=true)
> Claptrap from the Borderlands franchise


## Allied AI

Allied AI is what designers usually use to support the player through their playthrorughs. Usually used in ARPG style games, it's centered around NPCs serving as stress relief for the player, something the enemies can focus for a while.

Allied AI is fundamentally designed to be underpowered, so as not to overshadow the player, and also quite sturdy, so it can take a good beating when being focused. 

Allied AI can be useful in many aspects:

* **Company in solace**: AI and allied NPCs can be a big help when dealing with solo experiences. Either because some players prefer some kind of company through their playthroughs, and that company given by a single NPC can be conforting to them, or because they may not feel confident enough to go into the experience alone. 

This factor can also backfire, creating controversial entities which end up being loved and hated at the same time with the community, but this only happens in rare cases, in which, narratively or personalyty-wise, the NPC might feel urksome to the players. 

Claptrap -mentioned before- or Atreus from **God of War 4** could be good examples.

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/tenor.gif?raw=true)
> Kratos (the character the player plays as) and Atreus (his son) from God of War 4

* **Auxiliar teammate**: As stated in the previous points, players might not feel confortable facing a challenge alone, so giving them extra bodies, even though those of allied NPCs, can be a good way of distributing the pressure.

**Skyrim** NPCs which accompany the player in quests or allied units the player has recruited in the **Mass Effect** franchise could fall into this category.

* **A cherished friend**: If the NPC is narratively important enough, and is well designed so as to be likeable by the player, it is possible to reach a point where players might feel emotionally attached to it. This can be an important factor, since attachment directly correlates to immersion -and importance given by the player- which is one of the main objectives of AI in general. 

A good example of such an NPC is Princess Zelda from the **Legend of Zelda** franchise. 

![](https://raw.githubusercontent.com/JanAdell/Project-2-Research-Ai-RPG-Design/master/Research%20References/Website/da79770ce00594feff473b7f2cf31936.gif)
> Zelda and Link, The Legend of Zelda: Breath of the Wild

<a name="aiplay"></a>
# AI and the player

We, as designers and developers, want the player to end up seeing NPCs (as much as possible) as relatable, personality filled entities. This is usually a task accomplished by the joint effort of writers and designers, so as to bring a believable character to life, and then entrusting programmers and animators to put together an entity which moves and feels like something which could be real, or could, at least, exist in a world similar to that we're experiencing in the game.

<a name="airpg"></a>
# AI in RPG Games

Now that we've clearly defined all the pillars, our main focus is, how is -and how should be- AI designed when handling an RPG game?

* **Progression**: We need our AI to grow as the player does. By that we're not speaking of heightening its stats, but rather changing behavioral traits in order to become more and more of a challenge for the player.

* **Power and difficulty**: Having in mind the player's progress, and the design estimates at which the enemy NPCs should be, we have to be careful not to arrive at a result we don't want. Of course, we might want an overwhelming enemy which on top of hightened stats has fast reacting behaviour and unpredictable movement. That's usually not the case however, and we have to take into close consideration how we balance each of these aspects.


## Neutral NPCs

Neutral NPCs are mainly those who roam the cities and hubs and those the player interacts with in order to further the sotry. These NPCs' AI is mainly designed to follow certain patters inside their area of action in order to create environments for the player to get immersed with.

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/WalkingTown_FullScreen.gif?raw=true)
> Moonlighter

## Turn based RPGs: CRPGs, SRPGs and JRPGs

In turn based RPG games we usually have no allied units, since most of the allied characters are usually controled by the player themselves. This style of gameplay also makes for a relatively linear enemy AI behaviour process, making them easier to design compared to games where real time actions are involved. Typically, this kind of AI only changes when regarding different entities, but remains untouched for the same kind of enemy throughout the game, and is mainly balanced through stat changes and possibility to miss values. 

* **Typical Behaviour**: Enemy AI in turn based RPG usually bases itself off of linear default actions until certain actions are needed. To put it simply, it works in a reactionary manner. For example, using healing spells or items when their health is low, or faster attacks when the enemy's health is low in an attempt to finish the job. AI in this kind of game is usually predictable, and poses a threat to the player in regards to stats of the entity alone, which is usually a bit overblown in order to not be too bland of a challenge. 


## Real Time RPGs: ARPGs, Looter-Shooters, etc.

RPG games which use real time elements usually require of much heavier AI work compared to turn based ones, since the AI has to be considering how to act or react to constant real time events.

* **Reaction time**: Reaction time refers to how long do we make our AI take before it "realises" it has seen the player. It is important to note that the longer we make this time, the more margin we will give the player to act on this window. A reaction time which is too short might become frustrating, while one which is too long might become staggering.

* **Delay and patterns**: Patterns are a core of the gameplay when it comes to AI for melee combat RPG games. This allows for a variety of attacks -which the players usually learn eventually- which can be delievered in different fashion, depending also if certain conditions are met. 

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/ZigzagValuableAsiansmallclawedotter-size_restricted.gif?raw=true)
> Shara Ishvalda from Monster Hunter: World - Iceborne. Notice the reaction time to switch focus from one target to another, and the delay before the attack goes off.

Delay refers to how long it takes for an AI to attack the player. This is an important point in shooter-based RPGs, because the NPCs can reach the player easily, so we need to delay their attacks in order to offer the player the chance to shoot first, while the AI is catching up to them with their attack. This is something that can be seen clearly in **Rainbow Six Siege**, which is not an RPG game but offers a training mode against the AI.

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/6Ly36g.gif?raw=true)
> Rainbow Six Siege. Note the shots barely missing.

It is important to note that in Action RPGs delay is also applied but in a different manner, usually having enemy NPCs cast static spells or do long animations, so the player can react properly to them, or showing the player a trace of where the attack will be. 


## What we want from the AI: Designing our goals

AI is, at the end of the day, one more feature our game might or might not use. And it has many different purposes.

If we want an overwhelming experience, challenging the player at every turn, we can create AI that together with balancing, feels challenging and hard. Or the opposite, were we want to create a mild and fun experience, so we put our efforts into enemies which are fun to fight. If we want immersion we can create a highly narrative experience, and with it elaborate NPCs which the player can get attached to. We can also use AI to simply add some flavour to our game, adding life to the streets of our world.

In the end, AI is not only about giving human-like capabilities to in-game entities, but to bring an idea to life, by bringing to life the characters in our games.

![](https://github.com/JanAdell/Project-2-Research-Ai-RPG-Design/blob/master/Research%20References/Website/doggo_min.gif?raw=true)
> AI can be used to enhance even minimal elements.

<a name="resum"></a>
# Thoughts and Concluding Statement

AI is still unexplored land when it comes to being procedural. Be it centered around RPGs or not, AI nowadays only fills a stand in role for entities in a world, and even though we have the technology to create AI which caters to the player, we don't know yet how to manage it's limits properly so as to create a process which is optimal.

However, AI as we've known it until now is, in it's own way, something praiseworthy, because just like in a movie we might like characters because of their personalities or certain traits, in videogames we've accomplished during the years the merging of narrative, design, art and code in order to create characters the players could get attached to, in order to give the player enemies which felt real to face, in order to create boiling environments overflowing with life.

So as long as we keep pushing games with RPG elements, creating games with heavy narratives or games with high player involvement, we ourselves will have to keep striving to create more realistic and believable AI, until the day the AI itself can learn how to become it. 

<a name="sources"></a>
# Sources

## Websites

> [Player-centered game AI from a flow perspective](https://www.sciencedirect.com/science/article/pii/S1875952117300095#s0105)

> [Artificial Intelligence in Videogames](https://towardsdatascience.com/artificial-intelligence-in-video-games-3e2566d59c22)

> [Rapid and Reliable Adaptation of Video Game AI](https://www.researchgate.net/publication/224570972_Rapid_and_Reliable_Adaptation_of_Video_Game_AI)

## Videos

> [GDC: The Simplest AI Trick in the Book](https://www.youtube.com/watch?v=iVBCBcEANBc)

> [GDC: Tales from the Trenches: AI Disaster Stories](https://www.youtube.com/watch?v=__5whYgSTV0)

> [GDC: AI Wish List: What Do Designers Want out of AI?](https://www.youtube.com/watch?v=fSjlHvdq7SM)

> [GDC: Behavior is Brittle: Testing Game AI](https://www.youtube.com/watch?v=RO2CKsl2OmI)

> [Can You Beat Skyrim as a Level 1?](https://www.youtube.com/watch?v=KAmdYAvCQzA)

### Project Website Link

If you're reading this document from outside the dedicated Github website, the following link will grant you access to it.

> [AI in RPG games Design](https://janadell.github.io/Project-2-Research-Ai-RPG-Design/)
