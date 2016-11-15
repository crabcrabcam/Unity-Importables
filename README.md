# Unity-Importables
The importable files for use anywhere in Unity games. Enjoy :)

The code is stored [here!](https://github.com/crabcrabcam/Unity-Importables-Project)


# Platformer Movement
This package contains:
- Player Movement Script
- Ground block
- Player Object
- Setup of all the other things
- Everything else needed for the setup

What you need to do:
- Change the sprites.
  To do this you just need to put an image file in the Assets folder and select the "Player" object. Then you just need to drag the file to the "Sprite" section of the Player.
  This will change the image. You then repeat this for the ground blocks. 
- Create levels
  Use these building blocks to make levels. You'll be able to make something playable with only these items. To do multiple levels you'll need some more things from this repo. (Level Manager Kit)
- Change the speed and jump height to suit your game
  
  
# Camera Controller
This package contains:
- Camera Controller Script
- Camera prefab

What you need to do:
- Set the target for the camera to follow. This will usually be your player.
- Change the offset if you so wish.

You can use the camera controller on any object to make it follow any other. It will move instantly. I might work on a lag behind script to combat this and allow you to have it lag behind. For now just use the offset. With the offset you can change it to show more of what you're heading towards. You'd have to take the PlayerMovement script and create a camera object in it and have the offset be changed by the player movement script. Or you can take the follow target, determine it's direction and make the camera offset either behind or infront of where the player is going. 

Hopefully this will help you make a larger level than having a static camera and allow you to do more interacate things with the camera than just have it stuck to the player. (Also a problem if you ever want to flip the player.)


# Level Manager
This package contains:
- Level Manager script and object
- startOfLevel object
- LevelUp script and object

What you need to do:
- Set the variables in the LevelManager object. You need to set where you want the player to respawn. This only matters if you're using a killing script to kill the player. You need to set the player for this so it knows where to restart.
- You need to set the level where the player wants to go after they complete this level
- If this is the last level of your game you need to check the box that says "lastLevel". This will take them to the hardcoded level. By default it's "CompletedScene". You need to change this to be the correct name.
- You need to add all the scenes you make to the build manager. This is done by pressing "File, Build Settings". Then add all the scenes by dragging in them from the project screen. The one set to "0" is the one that will run at the start of the game. Set this to either the Menu or first level depending on how you want the game to start. 
- Set what the LevelUp object has set as its "LevelManager". This is the LevelManager object. 

This is a pretty basic set of things you will do with the LevelManager. Everything that your levels do is pretty much done in the LevelManager. As you can see, the levelUp script just calls the LevelManager. The RespawnPlayer function is in there if you want to give killing stuff your own go! I'm sure you can work it out ;) Otherwise there is another package for these blocks. 
