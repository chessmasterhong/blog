---
layout: project_details
categories:
    - "projects"
title: "Fire Emblem: Chronicles of the Abyss"
url_demo: ""
url_source: ""
thumbnail_style: "background: url(/img/fe1.png) -125px -20px no-repeat content-box; background-size: 200%;"
slides:
    - image: "/img/fe1.png"
      caption: "hello1"
    - image: "/img/fe2.png"
      caption: "hello2"
---


Fire Emblem: Chronicles of the Abyss is a web-based remake of Fire Emblem: Blazing Sword, a turn-based strategy role playing game for the Game Boy Advance, but with a different main character and plot twist. The game was built solely for educational purposes under the City College of New York's chapter of the Association for Computing Machinery's Game Development Student Interest Group. The game was developed in JavaScript utilizing the HTML5 canvas using the [ImpactJS game engine](http://impactjs.com). The main goals of this project are to recreate a game that we enjoyed playing, to create a fully completed, quality game, and to give back to the ImpactJS community by open-sourcing the code so as to assist other developers on how to create similar features in their own game. Furthermore, we wanted to see what ImpactJS was truly capable of and to push the limits of the game engine beyond what we had initially thought was possible.


Background Information
---
The game originally started near mid-November of 2013 under a different name and goal. After my experience with my [last ImpactJS game](/projects/super_mario_world_koopa_krisis), I wanted to take on the challenge of starting my own game. I was in the process of developing a battle system when one of my team members expressed great interest in using the battle system I had developed for a Fire Emblem game. I liked the idea and wanted to further improve my knowledge of the ImpactJS game engine.

From then until early February, I continued working on the battle system to the point where it was feasible to build the game. After many hours of brainstorming and development, this system is now the heart of the game, in which almost all functionalities of the game revolve around. We understood that in order to create a game of this caliber, we would need to devote a great amount of time and dedication. It was at that point where we assembled a team of five members to create the game seen here today.


Features
---
In order to ensure the game completes as planned, careful organization and distribution of tasks were essential. It was not long after the project began did we realize that we had a rapidly growing list of tasks completed and tasks to be assigned. We also found we were having difficulty keeping track of prerequisite tasks that needed to be completed before we could move on to the next set of tasks. As a result, we created a [general roadmap](http://github.com/chessmasterhong/WaterEmblem/blob/master/notes/roadmap.txt), [task dependency tree](http://github.com/chessmasterhong/WaterEmblem/blob/master/notes/task_tree.txt), and [records](http://github.com/chessmasterhong/WaterEmblem/blob/master/notes/records.txt) to keep track and visualize our current development progress. On several occasions, multiple tasks may be required in order to fully complete a feature.

Below outlines the major features we have implemented thus far:

* Battle system
    * Battle grid system
        * Multiple controllable player units
        * Unit pathfinding using A* search algorithm
        * Mouse "point-and-click" movement for unit movement
        * Non-collision nearby unit detection
        * Attackable enemy units, healable player units
        * Camera system to focus on active unit
        * Terrain system
        * Map scripts
        * Map objectives
    * Battle animation system
        * Animation queue for initial, counter, and second attacks
        * Animation handling for normal, magic, and critical attacks

* Character development system
    * Base stats
    * Derived stats
    * Level and experience system
    * Stat growth system

* Items
    * Unit inventory system
    * Unit equipment system
    * Trade system
    * Melee, ranged, and magic weapons
    * Weapon stats system
    * Weapon durability
    * Consumable items
    * Item quantity and usage
    * Enemy item drops

* Graphical user interface (along with all their corresponding functionalities)
    * Mouse-based menu interaction
    * Game settings configuration screen
    * Battle animation screen
    * Dialog screen
    * Stats screen
    * Attack/Heal interface
    * Inventory menu
    * Trade menu
    * Shop screen
    * Character portraits
    * Battle quick-summary


Development
---
It was quickly apparent that development was advancing at a lightning pace. We were adding new functionalities to the game almost every day or two. We would have near daily discussions regarding the features completed, any problems impeding our task, and how to tackle the next task. Whenever we have difficulties trying to solve a problem, we would brainstorm amongst each other on ideas that may be feasible. Sometimes, we would hold peer-coding sessions and receive live feedback on our code. In short, I felt this was
[agile software development](http://en.wikipedia.org/wiki/Agile_software_development) at it's best.

For the first four weeks since our team started, we finished about 98% of our task list which consisted of over 90 tasks. An additional week was spend on testing and bug fixing. After five weeks of development, near the end of March, we presented a fully playable, working demonstration of the game to our fellow peers, students, and faculties at the CCNY ACM Student/Faculty Mixer.

At the time of the Mixer, we had the following statistics:

* 622 commits since the team started (732 commits total)
* 42 pull requests
* Over 7400 lines of handwritten code, after many code refactorings
* Over 800 hours of combined development

According to our GitHub commit punchcard, there was development on the game at almost every time of each day, every day for the five weeks.

![GitHub commit punchcard](/img/fe_mixer_punchcard.png)

Here, shows our daily commit activity for the duration of the project until the Mixer.

![Daily commit activity chart](/img/fe_mixer_commitactivity.png)


My Roles, Experiences, and Challenges
---
I co-led this project alongside with another team member. My primary role was to oversee the technical direction of the game from the code standpoint. I provide feedback as to what tasks are available to work on and what tasks should not be started yet due to lack of code foundations. I also give high-level and low-level approaches and ideas to my team on how to implement certain features of the game.

Due to my initial work on the battle system, I ended up with possession of project's master repository. With this privilege comes responsibility; I also meticulously monitor and review all incoming code from my team members to ensure the code was functional, accomplishes the task given, and that the game remains playable. Consequently, I had to understand and keep up-to-date with the codebase so that in the event any functionality breaks, I would be able to immediately provide fixes where necessary. This ensures that the code and the game was fully working at any given time, which was difficult to do at times considering that adding some new features would inevitably break other existing features.

In addition to monitoring the codebase, I was responsible for performing many of the code refactoring, optimization, and cleanup. With every commit I push to the repository and pull request I receive from my team members, I ensure that the code remains readable, organized, modular, and functional.

Lastly, I actively participate in development. Along with the core battle system, I am also responsible for implementing several major features including, but not limited to:

* [Battle animations queue and sequence](http://github.com/chessmasterhong/WaterEmblem/commit/58059c2cdb2385c612b49766d6f474a27eec340c)
* System for handling close/long-range, [magical, hit/miss, normal, counter, critical, and second attacks](http://github.com/chessmasterhong/WaterEmblem/commit/9d413acb91127663720b9a0cd8ea0157cf4f9374)
* [Mouse "point-and-click" for unit movement and menu interaction](http://github.com/chessmasterhong/WaterEmblem/commits/356453621331844bc4dc2a9079dbf3f09d1fdf6f/lib/game/entities/misc/pointer.js)
* [Enemy artificial intelligence](http://github.com/chessmasterhong/WaterEmblem/commit/596690eac4f2f4ec86c8038193cda7939440cb9c)
* [Non-collision nearby unit detection](http://github.com/chessmasterhong/WaterEmblem/commit/e0f81a3e9fb9b5795b1adb5e51ee31e7ee42fa8c)
* [Multiple controllable player units](http://github.com/chessmasterhong/WaterEmblem/commit/4e44eb76479941b14daf16feda1884cc427b5505)
* Hooking A* pathfinding to [players](http://github.com/chessmasterhong/WaterEmblem/commit/2b5fa18babaf79493736ba7b33887e92c0d58b6f) and [enemies](http://github.com/chessmasterhong/WaterEmblem/commit/39ed6d74b9d6becfc7f64549c36f959f42d35f4e)
* [Trade system](http://github.com/chessmasterhong/WaterEmblem/commit/4f32b84b0c2acf01bd3acbe7c95c23d149c32a57)
* [Terrain system](http://github.com/chessmasterhong/WaterEmblem/commit/8cae76018a4a272b276f801fd8c74f799e350652)

This project has challenged me every step of the way. Nothing was trivial; every task and every feature required careful planning and implementation. Before writing each step of the code, I had to ensure that the code was efficient computation-wise, memory-wise, modular so that we may easily build and scale upon existing functionalities, as well as understandable for my team members.
