<h1>Project Week 9</h1>

<i>Week 9 Timeline</i>: 
<br>

Thursday, Mar 31st: 
<ul>
  <li><b>9:00am</b>: Start working for the day</li>
  <li><b>9:00am-9:50am</b>Speak with representative from <a href="https://www.mytruesound.com/">MyTrueSound</a> </li>
  <li><b>3:00pm-6:00pm</b>Add swipe to move functionality to streamline player movement</li>
  <li><b>8:30pm-10:00pm</b>Refine swipe to move, fix bug with grabbing item that caused player to enter the "unready" state permanently</li>
 
</ul>
<br>
Saturday, Apr 2nd: 
<ul>
  <li><b>11:00pm</b>: Start working for the day</li>
  <li><b>11:00-11:59pm</b>: Fix swipe to move to allow players to move to visited tiles outside of FOV (this is allowed in the base game)</li>
</ul>
<br>
Sunday, Apr 3rd: 
<ul>
  <li><b>12:00am</b>: Start working for the day</li>
  <li><b>12:00am-3:30am</b>: Alter swipe to move, map UI interface (inventory, journal) to voice commands</li>
  <li><b>5:00pm-6:30pm</b>: Add support for different inventory commands (drop, throw, info)</li>
  <li><b>9:00pm-11:59pm</b>: Add support for different inventory commands (drop, throw, info)</li>
</ul>
<br>
Monday, Apr 4th: 
<ul>
  <li><b>12:00am</b>: Start working for the day</li>
  <li><b>12:00am-1:30am</b>: Add support for different inventory commands (drop, throw, info)</li>
  <li><b>12:30pm-4:30pm</b>: Refine command detection system to take a "best match" approach, rather than just defaulting to the first instance mentioned, code readability/performance improvements</li>
 </ul>

 <br>
 <br>
 
 After several playthroughs this week using the voice interface, it became apparent that some quality of gameplay improvements needed to be made. The relatively low accuracy of phone TTS engines made voice-to-move commands 
 rather frustrating. Thus, a "swipe to move" command was added to help minimize the number of voice commands the player has to use. I found that this speeds up gameplay <b>significantly</b> and allows for a level-runthrough 
 at a speed comparable to the base game. Along these same lines, I went back and improved my command mapping system in order to take a "best match" approach, rather 
 than just defaulting to the first instance of a gameobject mentioned in a command. Thus, if the player says "stone of aggression", rather than simply "stone", the game
 is able to differentiate and find the best match that is present in the game, rather than just grabbing the first gameobject with the word "stone" available. This has greatly improved the accuracy 
 of the voice command system. Additionally, other gameplay commands were mapped to voice input, and the player can now equip items, unequip items, throw potions, drop items, eat food, drink potions, rest, search, 
 and more. Virtually all of the player commands available through the base game are now available through voice. Below, a comparison of the base game playthrough, and a playthrough using the voice commands can be seen. 

<br>
<br> 
View a runthrough of the base game <a href = "https://drive.google.com/file/d/1G2RLCPzW5O4GYaL6r_g1ElElxxEI7o3V/view?usp=sharing">here</a>
<br>
View a (mostly) visual-less runthrough of the game <a href="https://drive.google.com/file/d/1G3kWPCpQ3XD8_gg4XeJ7EkbLkHpr_ZwE/view?usp=sharing">here</a>. In a few occassions, such as when resting, I was forced to look at the screen to verify that the command went through. This indicates that the in-game feedback for some commands needs some work, and this will be prioritized in the upcoming week.
