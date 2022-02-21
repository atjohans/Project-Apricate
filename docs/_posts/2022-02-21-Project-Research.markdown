
Week 4's goals consisted of solidifying my choice og game to modify. This involved browsing for new candidate games, briefly playing those I was unfamiliar with, and (mostly) reading documentation regarding the source code or modding APIs of the game. 
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
      <li>Fix Explore solutions for integrating Free-TTS to Android build of the game </li>
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

