<i>Week 11 Timeline</i>: 
<br>

Saturday, Apr 16th: 
<ul>
  <li><b>1:00pm</b>: Start working for the day</li>
  <li><b>1:00pm-5:30pm</b>: Revise project presentation. Brainstorm methods for implementing a audio-based version of the in-game map</li>
 <li><b>7:30pm-1:00am</b>: Base game does not restore room connection data on game load, therefore we lose information about what rooms are connected when reloading a level - brainstorm how to fix this</li>
 
</ul>
<br>
Sunday, Apr 17th: 
<ul>
  <li><b>8:00pm</b>: Start working for the day</li>
  <li><b>8:00-1:30am</b>: Create system that gives rooms a unique ID on instantiation and stores list of connected room UID's. Save this list of UIDs on game save. Use list of connections to implement map command to give player idea of where they are.</li>
</ul>
<br>
Monday, Apr 18th: 
<ul>
  <li><b>11:00am</b>: Start working for the day</li>
   <li><b>8:00-1:30am</b>: Create system that gives rooms a unique ID on instantiation and stores list of connected room UID's. Save this list of UIDs on game save. Use list of connections to implement map command to give player idea of where they are.</li>

</ul>
<br>
Monday, Apr 11th: 
<ul>
  <li><b>11:00am</b>: Start working for the day</li>
  <li><b>11:00am-3:30am</b>: Continue modifying map command. Integrate "look doors" to make more intuitive.</li>

 </ul>

 <br>
 <br>
 
 <p> The main issue I kept running into with the game was getting lost and not knowing what outes were available to me without the game's visual component. To attempt to fix this, a map command was implemented that tells the player what room they are in, and what rooms are immediately connected (that have already been explored) to the room. This provides the user with a method of differentiating between different types of rooms, and helps the determine what paths are available. This ended up taking significantly longer to implement than I initially thought that it would, as the base-game did not save room-connections when reloading the game, meaning the map would break if a player left and reloaded a level. A system needed to be built that allowed room connections to persist after exiting the game. </p>
 
