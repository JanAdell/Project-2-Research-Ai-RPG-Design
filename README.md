# Project 2 Research: AI RPG Design

I am [Jan Adell Mill](https://www.linkedin.com/in/jan-adell-41a5341a3/), student of the [Bachelor’s Degree in Video Games by UPC at CITM](https://www.citm.upc.edu/ing/estudis/graus-videojocs/). 

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

AI is, in general, an element used in videogames in order for game entities to accomplish functions in a more human-like manner. NPC's actions, being allied, enemy or neutral, are all controlled by AI. 

However, as we will see in this document, AI is an element not only used to give a sense of realism to entities and characters in our RPG games, but a game feature which, when used properly, can be useful to enhance the experience in certain manners game developers see fit.

<a name="rpg"></a>
# RPG Games

Role Playing Games (RPG in short) are a genre of videogame based on having the player participate in a story, in which they progress, grow and become more powerful as time goes on and they advance further into the narrative. 

RPGs have been defining the videogame industry from it's very core since the very beggining, serving as examples for many other genres on how to apply certain features and mechanics, mainly progression and character growth. It's important to keep that in mind as we speak of AI, since, as the player grows, we need the environment around him to do as well. 

AI in RPGs is an important factor due to one main reason (which doesn't always apply): The amount of NPCs we find in them. From regular NPCs we find at towns or taberns, to allies or enemies in battle, all of their actions are controlled by AI created by the developers.

Not only that, but since RPGs have a vast amount of subgenres, and within them playability is usually different in a fundamental level, we have to design our AI so it fits within the game. 

<a name="aides"></a>
# AI Design

AI Design is used, in general, to try and boost the immersive capabilities of a game in order to bring the player to feel or live the narrative and universe in a more geniune manner. This is attempted to do by making responsive AI which brings life to the game, and gives it a more organic feeling. NPCs in cities talking and reacting as the player passes by, enemies with multiple patterns or unpredicability and companions which support the player through the game are all ways in which AI can help accomplish this previous mentioned organic feeling.

AI Design is partically important in RPG games, since as they're usually based on progression and narrative, we need the AI to grow in parallel with the player.

## Different kinds of AI

AI in videogames comes in many different forms. While it can certainly be programmed as to act purely as human-like as possible, AI is a tool for developers to make the player and the world interact in a more immersive manner, making it versatile when it comes to possible paths to take when implementing it. 

* **Non-Adaptative AI**

AI which has a defined set of rules, being more or less complex, by which it acts and reacts to whatever is happening. 

This kind of AI is probably the most used nowadays, since it allows the designers to control NPCs actions within expected parameters, thus avoiding possible problems by being able to forcibly define how the entity acts. 

* **Traits**

A concept mainly popularized by The Sims, this is based on having various Non-Adaptative patterns of behaviour in an entity (sometimes placed randomly) in order to create a form of Non-Adaptative AI which feels more random and natural, also allowing for the creation of characters with more defined personalities. 

* **Adaptative AI**

A type of AI which learns through data in order to optimize and adapt itself. Nowadays it's mainly used in MMORPG games in order to teach NPCs certain player-related actions which are hard to define by the developers inside an AI system. 

In the future, this kind of AI might be used to create more personal experiences catered to each individual player, allowing the AI to recognize patterns within a players playstyle and then interacting with him in a suitable manner. 

Even though we have the technology to allow the AI to learn, this method will, most likely, still take a few years to become something we see in our RPG games, since developers have few tools to manage all the possible interactions created from learning, as well as few ways to regulate such way of learning. 

### Concerns within AI Designing

Our main concern when designing AI is that the AI we designed is not correctly fullfilling it's role. For example, if we have an enemy NPC which is designed to be fairly easy, but a majority of players are deeming it a hard, our AI is not working as intended. There are also problems related to the code defining the AI, mainly when relating to pathing, but those are normally outside design capabilities.

## Enemy AI

Enemy AI or enemy NPCs are probably were we will find the most freedom when it comes to designing, since many things can be expressed depending on how it is done. 

First and foremost, designing and balancing en enemy in an RPG is subjective, since there can be many factors that define said balancing process. When designing any kind of enemy in general, several key points can be made to use as guidelines during the process.

* **The mood**: The mood refers to the feeling we want to give off by certain behaviours by the AI. Normally in accordance to the general mood of the game. A good example of implementations based in mood can be found in the Souls franchise, where enemies, as soon as they notice the player, start the slow burn pursuit towards them.

* **The difficulty**: Difficulty refers to how, through stat tweaks and behaviour design, we can make an enemy more or less hard to deal from the player's perspective. A pretty good example of this implementation can be found in **Monster Hunter: World - Iceborne**, where a same monster in different difficulty categories (Low Rank, High Rank and Master Rank) has substancial fluctuations in both damage output, effective health and behaviour patterns (being easily angered as rank gets higher). This also feeds into the proposition of the AI growing as the player does, since the player unlocks higher play ranks as he moves forward through the story.

* **The behaviours**: We refer to behaviour when talking about how the AI reacts. Inicial raction time, as well as actions taken in response to external changes, are actions defined in an NPCs behaviour, and a core part of the concept we know as AI. A good example of behaviour which is easy to notice takes place in the **Pokémon** franchise, where enemies will use healing items or abilities as they detect their Pokémon loosing health.

* **The purpose**: We refer to purpose in AI the same way we would refer to any other game feature. We ask ourselves why do we need it, and what objective do us, as the developer, wish to accomplish with it, as well as what results we want to get from the player encountering it.

A clear example of purpose within an NPCs can be found in Claptrap, from the **Borderland** series. From the moment he's introduced in the tutorial of the first game, we can feel what the experience will be about. Over the top, roudy, sensless action. 

## Allied AI

Allied AI is what designers usually use to support the player through their playthrorughs. Usually used in ARPG style games, it's centered around NPCs serving as stress relief for the player, something the enemies can focus for a while.

Allied AI is fundamentally designed to be underpowered, so as not to overshadow the player, and also quite sturdy, so it can take a good beating when being focused. 

Allied AI can be useful in many aspects:

* **Company in solace**: AI and allied NPCs can be a big help when dealing with solo experiences. Either because some players prefer some kind of company through their playthroughs, and that company given by a single NPC can be conforting to them, or because they may not feel confident enough to go into the experience alone. 

This factor can also backfire, creating controversial entities which end up being loved and hated at the same time with the community, but this only happens in rare cases, in which, narratively or personalyty-wise, the NPC might feel urksome to the players. 

Claptrap -mentioned before- or Atreus from **God of War 4** could be good examples.

* **Auxiliar teammate**: As stated in the previous points, players might not feel confortable facing a challenge alone, so giving them extra bodies, even though those of allied NPCs, can be a good way of distributing the pressure.

**Skyrim** NPCs which accompany the player in quests or allied units the player has recruited in the **Mass Effect** franchise could fall into this category.

* **A good companion**: If the NPC is narratively important enough, and is well designed so as to be likeable by the player, it is possible to reach a point where players might feel emotionally attached to it. This can be an important factor, since attachment directly correlates to immersion -and importance given by the player- which is one of the main objectives of AI in general. 

A good example of such an NPc is Princess Zelda from the **Zelda** franchise. 

## AI which doesn't partake in the action

All the NPCs we see in cities, towns and gathering hubs in our RPG games, walking around, doing their own thing, talking, are also entites controlled by AI.

<a name="aiplay"></a>
# AI and the player

We, as designers and developers, want the player to end up seeing NPCs (as much as possible) as relatable, personality filled entities. This is usually a task accomplished by the joint effort of writers and designers, so as to bring a believable character to life, and then entrusting programmers and animators to put together an entity which moves and feels like something which could be real, or could, at least, exist in a world similar to that we're experiencing in the game.

<a name="airpg"></a>
# AI in RPG Games

Now that we've clearly defined all the pillars, our main focus is, how is -and how should be- AI designed when handling an RPG game?

* **Progression**: We need our AI to grow as the player does. By that we're not speaking of heightening its stats, but rather changing behavioral traits in order to become more and more of a challenge for the player.

* **Power and difficulty**

## Turn based RPGs: CRPGs, SRPGs and JRPGs

In turn based RPG games we have mainly neutral NPCs or enemy ones. 

## Real Time RPGs: ARPGs, Looter-Shooters, etc.

* **Delay and patterns**

* **Reaction time**

## What we want from the AI: Designing our goals



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

### Project Website Link

If you're reading this document from outside the dedicated Github website, the following link will grant you access to it.

> [AI in RPG games Design](https://janadell.github.io/Project-2-Research-Ai-RPG-Design/#intr)
