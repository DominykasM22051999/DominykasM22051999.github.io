---
layout: post
title:  "The Yellow Mellow Fellow Project"
date:   2021-06-14 08:48:32 +0000
---
### <center><u>Overview</u></center>
<center><IMG SRC="{{ site.baseurl }}/assets/Pacman.gif"></center>

This project is based on the original Pac-Man with a personal touch which was done as part of assessment for module CSC2034.
The base of the scene and logic of the game was provided by the University as part of introductory material to games engineering and Unity.
Tasks and extensions were set as part of assessment to expand upon the game. 

**Workflows used**: Git and Agile. **Technologies used**: C#, Unity Game Engine.

***Note**: Due to the project being part of my degree assessment code is not available publicly.*

Grade achieved: 80%

#### <u>Basic functionality of Pac-Man</u>
As part of the project we were required to have the basic functionalities of Pac-Man such as:
- Ability of Fellow to move in any direction and collect pellets.
- Have four different ghosts (Chaser, Random, Lazy, Seeker) with different 'personalities' chasing Fellow.
- Fellow to have three lives.
- Ability to teleport after the Ghost or Fellow enter the tunnel.
- Have a UI so the user knows their current score, lives, level, and high score.

#### <u>Additional features added:</u>
- Four additional power ups: double points, extra life, slow, extra speed.
- Two game modes - Classic/Arcade. Classic containing two of the four power ups and Arcade containing all four power ups per level and the Fellow and Ghosts receiving a speed up of x2.5.
- High score system - The current score of the player is compared with the high score if they achieve a higher score they will be prompted with an UI to input their name which is then saved in a text file. The high scores can be displayed to the user at the main menu.
- Animation - I wanted to explore how animations work and managed to create a simple 'bounce' animation of the Fellow. The animation seen above is always displayed at the start of every game.
- Added personal visual style to the game - making it look like a maze using the objects downloaded from different creators in the Unity Asset Store.
- Path finding - Explored path finding algorithms. Chaser to constantly head to the Fellow's current position. Random’s logic consists of getting the Fellow’s position and selecting a location that is 4 units greater in the x-axis. This means it might be ahead or behind of the Fellow resulting in occasional block of the Fellow’s path. Seeker’s logic and design is like of a heat seeking missile; it initially picks a random destination until it detects the Fellow. Finally, Lazy is the slowest of the four ghosts and is always the last to leave the ghost house as it only moves when the level is greater than 2, and the Fellow consumes 60 or more pellets in the level.
- Level system - bringing a challenge to the user. The level up simply restarts the level with the Ghost and Fellow receiving a little speed boost from the previous level and the fourth ghost start to roam the maze from level 2.


#### <u>Testing strategy</u>
The testing strategy undertaken was more of a black box approach throughout the duration of the project. After implementing a major feature, I would manually test input scenarios to see whether the output was as expected. If a bug was found, the approach was to fix it right away before moving onto a new feature. In addition, a lot of bugs and fixes were discovered by using this approach making this stage of development interesting. I have also produced a testing document for the version that was released for submission, which gave me a good understanding of the features and tasks that worked as expected and whether I met the required task and extension criteria.

#### <u>References and Credits</u> 
Please view the following <a href="/assets/References.pdf" target="_blank">PDF file</a> for the full reference list of project.