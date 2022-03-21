<h1>Project Week 7</h1>

<i>Week 7 Timeline</i>: 
<br>

Saturday, Mar 19th: 
<ul>
  <li><b>5:30pm</b>: Start working for the day</li>
  <li><b>5:30-6:30pm</b>: Experiment with methods to make speech recognition mapping to game controls more "intelligent" and more intuitive for players</li>
</ul>
<br>

Sunday, Mar 20th: 
<ul>
  <li><b>10:30am</b>: Start working for the day</li>
  <li><b>10:30-1:30pm</b>: Experiment with methods to make speech recognition mapping to game controls more "intelligent" and more intuitive for players</li>
  <li><b>1:30-3:00pm</b>: Read <a href="https://www.degruyter.com/document/doi/10.1515/comp-2020-0125/html?lang=en">Natural mapping between voice commands and APIs</a> by Matúš Sulír and Jaroslav Porubän</li>
  <li><b>3:00-3:30pm</b>: Begin building text processor and command mapper classes</li>
  <li><b>3:30-5:00pm</b>: Break </li>
  <li><b>5:00-9:30pm</b>: Finish implementing text processor class</li>
  <li><b>9:30-11:30pm</b>: Break</li>
   <li><b>11:30-11:59pm</b>: Work on system that maps processed command input to game actions</li>
</ul>
<br>
Monday, Mar 21st: 
<ul>
  <li><b>12:00am</b>: Start working for the day</li>
  <li><b>12:00am-2:30pm</b>: Work on system that maps processed command input to game actions</li>
  <li><b>11:00am-1:00pm</b>: Implement system that attempts to determine direction of game object from player voice command</li>
   <li><b>3:00pm-4:00pm</b>: Run through a few game scenarios, attempt to find bugs or areas where the voice recognition mapping does not do well</li>
 </ul>
 <br>
 <br>
 
 <p>
 As seen from above, most of this weeks work involved finding a way to map a relatively large possible input space (user voice commands) to a finite set of game actions. Even as the developer, who had hardcoded in many actions from week 6, I found it extremely frustrating when the game ignored my command because a single word was misinterpreted or the voice recognition system thought I said "too" instead of "two", or maybe I said "northeastern" instead of "northeast". A solution to this problem took some experiementation. My initial thought was just to enumerate many of the common synonyms for a given command and hashmap them to the intended command. While fairly straightforward, some more thought made me realize just how infeasible this was, as <i>Shattered Pixel Dungeon</i>  -  while a small mobile game - has quite a lot of variety in enemies, terrain types, item types, etc. Additionally, there are a number of synonyms for every given command, especially if we take into account words containing suffixes (walk<i>ing</i> vs walk, etc). Thus, I attempted to come up with a solution that would allow me to enumerate as few hardcoded phrase-to-command mappings as possible. 
<br>
  <br>
 To deal with some of these issues, a textprocessor class was built with the intention of tokenizing and standardizing input commands. The text processor takes the entire spoken phrase, and breaks it up by spaces into individual "tokens". The tokens are converted to their lowercase counterparts, and are passed through a <a href="https://en.wikipedia.org/wiki/Stemming">Porter Stemming algorithm</a> with the intention of standardizing words with the same root. Contractions are expanded ("aren't" -> "are", "not"), stopwords ("i","am","is",etc) are removed, written numbers are swapped with their numeric counterparts (i.e. "ten" -> "10"), etc. After all this we are left with a stripped down input phrase that is far far easier to manage. After this processing, the number of synonyms we need to enumerate are much fewer, and I was able to enumerate several common pairs for the key input words. These synonym swaps are made, giving us the final set of processed tokens for a given command. 
  <br>
  <br>
To map these tokens to an actual command, a simple token-presence system was used. In the base game for <i>Shattered Pixel Dungeon</i> the user communicates almost all of their intent via touch. The user can look at each game tile, and the game assumes some information based on where they touched. Did the player click on an empty tile with nothing else around? The game assumes (usually correctly) that the player wanted to move to that tile. Was a non-empty tile with an enemy on it clicked? The game assumes the player wishes to attack the enemy. Each touch on the screen can have 1 of three major actions (in most cases): move to tapped tile, move to adjacent tile and attack enemy at tile, interact with item on tile. Consequently, I was able to map any given voice command to one of these three major actions. By scanning the token list and looking for the presence of a keyword, such as "move" or "attack", I built a system that makes the same assumptions inputted voice commands as the base game makes about touch commands. Additional information about direction, itemtype, etc is obtained after determining the core game action by scanning the remainder of the tokens. 
  
<br>
  <br>
From this weeks work, I was able to obtain the same amount of in-game "expressive power" through voice commands as the default game controls. This means that the game is essentially playable entirely via voice controls. This upcoming week will focus on game information, and communicating necessary game events to the player in a more intuitive and immersive way - a key portion of this will be creating a system that allows the player to know the command was communicated and completed without simply repeating it (as is the current state). The hope is to use sound effects and environmental sounds to communicate what is currently being communicated through voice - I expect that this will take a great deal of trial and error.  Assuming this is accomplished by next week, the remaining 2-3 weeks of this project will be focused on fine tuning via playtests. 

<br>
  <br>
  

View an example of how different command phrasings can still be understood, and an example of how users can specify direction <a href = "https://drive.google.com/file/d/1CcGDGjsLst1NuLBMsOg7GgH2T_R3Zd1w/view?usp=sharing">here</a> 
  <br>
  <br>
View an example of how my intention can still be understood even when I hesitate/stutter <a href ="https://drive.google.com/file/d/1CiL9KYj2Bu1NGUwQkAwcXxTbybObTujq/view?usp=sharing">here</a>
  
  
  
  

