<h1>Project Week 8</h1>

<i>Week 8 Timeline</i>: 
<br>

Saturday, Mar 26th: 
<ul>
  <li><b>2:00pm</b>: Start working for the day</li>
  <li><b>2:00-6:30pm</b>Modify "move" command to be more general</li>
</ul>
<br>

Sunday, Mar 27th: 
<ul>
  <li><b>5:00pm</b>: Start working for the day</li>
  <li><b>5:00-11:00pm</b>: Work on modifying move command to allow user to state a direction, add path option to look command that allows user to see which directions are available, add "double click" to repeat function</li>
</ul>
<br>
Monday, Mar 28th: 
<ul>
  <li><b>12:30am</b>: Start working for the day</li>
  <li><b>12:30am-3:00am</b>: Add grab item action</li>
  <li><b>11:00am-1:00pm</b>: Add system that tells user when enemies appear without prompting</li>
   <li><b>3:30pm-5:00pm</b>: Work on double click to repeat (currently only works for attacking) </li>
 </ul>
 <br>
 <br>

<p>
  
  The primary focus of this week's work was to put in place the system that would communicate all of the game-critical information to the player. In the base game, the player receives almsot all of the game information through visuals, with a few key components being communicated by various sounds. The solution that I came up with allows players to use the keyword "look" to tell the game that they wish to obtain information about the game scene. Players can say "look enemies" or "look items" or even "look doors" and the game will list corresponding information. I find that this system works well and allows me to gain a pretty good understanding of the game scene without using the game's visuals. However, as I play tested with these commands, I noticed that one crucial piece of game information was missing - direction. The system did not list out possible directions that the player could move in, meaning that a lot of guesswork was involved in "exploring" the dungeon and players had to just aimlessly repeat commands until something new happened. My original solution to this was to build a rudimentary pathfinding system that checked for avaialbe tiles in certain directions and listed out paths if tiles were avaialble. For example, if a plyaer said "look routes" and there were free tiles with a route avialable to the west, the game would say "path to the west". This system currently has a few bugs, and the player tends to get stuck in areas like hallways, where the path might turn suddenly. Aside from this issue, most of the major game systems are in place and once a intuitive, and less clunky solution to movement and cpath communication is found, the game will be largely playable via voice commands. 
  
  In addition to what is lsited above, a this week's work also involved polishing up the player input system, and adding a "double click" to repeat system, that allows players to repeat their last command by double clicking, rather than via voice prompt. This makes gameplay much faster and less prone to speech-synthesizer mistakes. 
  
  <p>
