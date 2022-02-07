Given the time restraints associated with this project, I have opted not to build a novel game from scratch, but rather, to take existing software and experiment with implementing accessibility features into it. 

OpenRA is an open source project that seeks to recreate popular classic RTS games such as Command & Conquer. The screenshots below are taken from the project's recreation of Red Alert. From the screenshots, we can see that accessibility was not a primary consideration for the project. Aside from basic key remapping options, the game offers no accessibility features. This is common for all of the OpenRA engines core game mods (RA,CNC,D2K). 

<img style="width:175px" src="https://github.com/atjohans/Project-Apricate/blob/gh-pages/assets/images/image1.png?raw=true"></img>
<img style="width:175px" src="https://github.com/atjohans/Project-Apricate/blob/gh-pages/assets/images/image2.png?raw=true"></img>
<img style="width:175px" src="https://github.com/atjohans/Project-Apricate/blob/gh-pages/assets/images/image3.png?raw=true"></img>
<img style="width:175px" src="https://github.com/atjohans/Project-Apricate/blob/gh-pages/assets/images/image4.png?raw=true"></img>


This week’s work involved assessing the OpenRA engine as a candidate for this project’s goals and experimentation. There were two primary tasks for this week:
Play the base game
The purpose of playing the base game was twofold: 
Gain familiarity with with the core game and its overall feel and mechanics 
Identify some of the game-critical information and how it is communicated to the player
Analyze the OpenRA Mod SDK 
In analyzing the OpenRA Mod SDK I was primarily interested in a few things: 
Is the SDK still supported and updated relatively regularly 
Does the SDK provide most of the tools necessary to build and run the game with minimal setup effort 
Does the SDK provide the control necessary to restructure how game-critical information is delivered to the player

I spent most of my time this week gaining familiarity with the engine and setting up an environment in which I can experiment with modifying the core functionality of the game. The project allows developers to create “mod overlays” in which they can modify existing standalone mods built on the OpenRA engine, and also gives developers full access to the OpenRA engine in which they can create their own classic 2D RTS. To gain familiarity with the overarching structure of the project, I walked through the project's basic modding tutorial (https://github.com/OpenRA/OpenRAModSDK/wiki/Getting-Started). Ultimately, I was able to successfully install and build the base game and the mod sdk, and was able to successfully build and run the modified version I had created with relative ease and few compatibility issues. 

From my experimentation I have determined a few things.  The first is that the “overlay-modding” capability of the OpenRAModSDK will be insufficient in-and-of-itself to provide the accessibility functionality necessary to create an RTS that is accessible to the visually impaired. This means that I will likely need to create my own OpenRA standalone mod over the course of this project, should I continue to work with the OpenRAModSDK. 
