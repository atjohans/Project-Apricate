
This week involved a lot more documentation reading. The primary goal of this week was to build a TTS engine that would allow me to easily communicate chosen audio to the player by simply sending messages from an event dispatcher to an event listener. With this tool in place, I can begin to build the actual user interface that allows players to retrieve chosen information, and I can begin to modify the games flow to better work with this system. A good portion of the time spent this week was ensuring that this event dispatch system was compatible with both the desktop and android builds of the game - this required some creative thinking given that both the TTS Engines used were not built with cross-compatibility in mind. 
<br> 
<br>
<i>Week 5 Timeline</i>: 
<br>

Sunday, Feb 20th: 
<ul>
  <li><b>12:00pm</b>: Start working for the day</li>
<li><b>12:00-4:00pm</b>: Integrate Java Free-TTS into the Desktop build of the game</li>

<li><b>4:00-5:30</b>: Fix issues where calls to Free-TTS synthesizer block all other game process while audio is playing</li>
<li><b>5:30-11:59pm</b>: 
    <ol>
      <li>Fix dependency resolution error: (Duplicate class de.dfki.lt.freetts.mbrola.MbrolaAudioOutput found in modules freetts (freetts.jar) and mbrola (mbrola.jar)) </li>
      <li>Explore solutions for integrating Free-TTS to Android build of the game </li>
      <li>Work on building interface that allows for easy message calling from any core file of the game source (TTS Manager Class)</li>
  </ol>
  
</li>
</ul>
<br>
Monday, Feb 21st: 
<ul>
<li><b>12:00-1:45am</b>: Implement alternate (non Java Free-TTS) text-to-speech solution for android build, as android java environment does not support core libraries of Free TTS</li>
 <li><b>1:45-2:15am</b>: Break for Ramen</li> 
<li><b>2:15-3:45am</b>:
  <ol>
    <li>Read documentation on Android TextToSpeech library, begin implementation of TTSManager class for Android platform</li>
    <li>Begin implementation of event dispatch system that allows for sending messages to the speech event handler, regardless of build platform</li>
    </ol>
  </li>
  <li><b>12:00-2:00pm</b>: Finalize event dispatch system </li>
</ul>
<br>

