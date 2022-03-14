<h1>Project Week 6</h1>

<i>Week 6 Timeline</i>: 
<br>

Friday, Mar 11th: 
<ul>
  <li><b>3:00pm</b>: Start working for the day</li>
  <li><b>3:00-7:00pm</b>: Integrate speech recognizer into android build of the game & test</li>
</ul>
<br>

Saturday, Mar 12th: 
<ul>
  <li><b>12:30pm</b>: Start working for the day</li>
  <li><b>12:30-1:30pm</b>: Modify event system to integrate speech recognition listening</li>
  <li><b>9:00-11:00pm</b>: Modify event system to integrate speech recognition listening</li>
</ul>
<br>
Sunday, Mar 13th: 
<ul>
  <li><b>11:00pm</b>: Start working for the day</li>
  <li><b>11:00-3:00pm</b>: Begin Altering UI & controls to utilize speech synthesis and speech recognition engines</li>
  <ol>
    <li>Strip out all existing controls</li>
    <li>Add "tap to listen" functionality</li>
    <li>Add command processing system that handles spoken commands</li>
  </ol>
  <li><b>3:00-5:30pm</b>: Solve Android Permission Denied nightmare - still in progress (temporary workaround found)</li>
  <li><b>5:30-11:59pm</b>: Continue translating game controls to voice commands, build on statereader to allow player to retrieve chosen information</li>
  </ul>
  Monday, Mar 14th
  <ul>
  <li><b>12:00-12:30am</b>: Continue translating controls to voice commands - fix infinite loop in voice recognition state machine</li>
  </ul>
  <br>
<p>The primary goal for this week was to build the core of the new UI that would replace the existing UI. To do so, a speech recognition system was integrated into the game engine to allow playes to provide input to the game via voice commands. This, coupled with the speech synthesis engine integrated into the game engine earlier, will provide most of the input and information retrieval systems for the game. While a good portion of the game is playable with the curent state of the voice command system, the voice commands are not very "intelligent". Players currently have to repeat commands several times to accomplish something that can be done in the base game with a single tap. Additionally, much of the information provided to the player in the current state is very general, and is not adequate on its own to fully replace the visual information of the game. The next phase of the project will involve augmenting the ifnor retrieval and input systems to make them more "intelligent" - making inputs more intuitive, making information more precise, etc. I expect this phase will rely heavily on user feedback and playtests, especially from those who have not yet played the base game. </p>

<br> 

<iframe width="560" height="315" src="https://drive.google.com/file/d/1AezYvpx29veXJGiDa1QLWTaIubLSx-fP/view?usp=sharing"  frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

