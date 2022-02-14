Week 4's goals consisted of solidifying my choice og game to modify. This involved browsing for new candidate games, briefly playing those I was unfamiliar with, and (mostly) reading documentation regarding the source code or modding APIs of the game. 
<br> 
<br>
<i>Week 4 Timeline</i>: 
<br>

Saturday, Feb 12th: 
<ul>
<li><b>8:00-9:00pm</b>: Browse <a href="https://en.wikipedia.org/wiki/List_of_open-source_video_games">open source game listings</a> for candidate games</li>
</ul>
<br>
Sunday, Feb 13th: 
<ul>
<li><b>12:30-1:30pm</b>: Continue Browsing for candidate games</li>
<li><b>2:00-2:30pm</b>: Download, install and run Factorio - identify game critical information and how it is communicated</li>
<li><b>2:30-3:00pm</b>: Lunch</li>
<li><b>3:00-4:30pm</b>: Read/Understand the <a href="https://www.lua.org/manual/5.4/">Lua Documentation</a></li>
<li><b>4:30-5:30pm</b>: Skim the <a href="https://lua-api.factorio.com/next/">Factorio Modding API</a></li>
<li><b>5:30-7:30pm</b>: Download and review <a href="https://mods.factorio.com/">existing Factorio Mods</a> for examples </li>
<li><b>7:30-10:00pm</b>: Work through implementation of basic modding components, experiment with the system to gain familiarity <br>  Read about <a href ="https://github.com/festvox/flite">festival lite (FLITE)</a>, CMU's Speech Synthesis System, download and compile source</li>
 <li><b>Direction Shift</b></li>
<li><b>10:00:11:59pm</b>: Download, setup environment for <a href="https://github.com/00-Evan/shattered-pixel-dungeon">Shattered Pixel Dungeon</a> open source game</li>
</ul>
<br>
Monday, Feb 14th: 
<ul>
<li><b>12:00-1:00am</b>: Download, setup environment for <a href="https://github.com/00-Evan/shattered-pixel-dungeon">Shattered Pixel Dungeon</a> open source game</li>
<li><b>1:00-1:30am</b>: 1am Snack Break</li>
<li><b>1:30-2:30am</b>: Read about <a href="https://freetts.sourceforge.io/">Java FreeTTS</a> experiment with integrating into Shattered Pixel Dungeon Mod</li>
<li><b>11:00-11:59am</b>:Experiment with integrating FreeTTS into Shattered Pixel Dungeon Mod</li>
</ul>


<br>
<br>
Admittedly, this project is off to a slower start than I would like. As shown above, much of my work this week involved identifying candidate games to modify, reading documentation, doing some experimenting, and then ultimately changing directions when I discovered a roadblock that I had forgotten to consider (In this case, I had failed to consider that the developers of Factorio would place heavy restrictions on what your lua scripts in your custom mod can access, which, in hindsight, should have been obvious) - ultimately resulting in a lot of wasted time. I believe now that I have at least solidified the candidate game that I wish to modify for the remainder of this program - Shattered Pixel Dungeon. This game is an open source rogue-like RPG in which the player descends layers of a dungeon, while collecting items and slaying monsters. The game currently has little in the way of accessibility features for the visually impaired, and the game does not seem to work well with Android's "Talkback" functionality, as the buttons in the game UI become un-interactable, meaning players cannot even get past the primary menu screen. 

Despite these issues, I feel that the game has a lot of potential. Almost every in-game event has some sort of text prompt included with it (see the image below), and players interact with the game only through screen taps (rather than virtual joysticks, buttons, etc). The game also has a sort of turn-based feel, where enemies only move if the player moves, and combat happens by trading actions between the player and the enemy. I believe that with some work, all of the game-critical information for Shattered-Pixel-Dungeon can be communicated audially, and I plan to spend the remainder of this project implementing an interface that allows players to retireve the game information they want, and input a desired action. 

<img style="width:100%" src="https://github.com/atjohans/Project-Apricate/blob/gh-pages/assets/images/shatteredPixelSampleScreen.JPG?raw=true">
