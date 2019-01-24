Cell Wars
=============
**Built using huytd's source**

A simple but powerful Agar.IO clone built with socket.IO and HTML5 canvas on top of NodeJS.

---

**How to Play**
Players start as small round "Cells". The object of the game is to gain mass by eating pellts and other players. As a cell passes over another cell or pellet, the larger of the two will absorb, or eat, the smaller and gain the mass of the aten pellet or cell. 

**Game Basics**
- Move your mouse around the screen to move your cell.
- Eat food and other players in order to grow your character (food respawns every time a player eats it).
- A player's **mass** is the mass gained from players & food particles eaten.
- **Objective**: Try to get as big as possible and eat other players.

**Gameplay Rules**
- Players who haven't eaten yet cannot be eaten as a sort of "grace" period. This invincibility fades once they gain mass.
- Everytime a player joins the game, **3** food particles will spawn.
- Everytime a food particle is eaten by a player, **1** new food particle will respawn.
- The more food you eat, the slower you move to make the game fairer for all.

---

**Latest Changes**
- Game logic is handled by the server
- The client side is for rendering of the canvas and it's items only.
- Mobile optimisation.
- Implementation of working viruses.
- Display player name.
- Now supporting chat. 
- Type`-ping` in the chatbox to check your ping, as well as other commands!
- Left clicking your mouse will "Split" your cell into multiple pieces
- Right clicking your mouse will eject a small amount of mass
---

**Installation**

**Requirements**
To run / install this game, you'll need: 
- NodeJS with NPM installed.
- socket.IO.
- Express.


**Downloading the dependencies**
After cloning the source code from Github, you need to run the following command to download all the dependencies (socket.IO, express, etc.):

```
npm install
```

**Running the Server**
After downloading all the dependencies, you can run the server with the following command:

```
npm start
```

The game will then be accessible at `http://localhost:3000` or the respective server installed on. The default port is `3000`, however this can be changed in config. 

---

**FAQ**
1. **What is this game?**

  This is a clone of the game [Agar.IO](http://agar.io/). 
  
2. **Why would you make a clone of this game?**

  Well, while the original game is still online, it is closed-source, and always suffers from massive lag. I want to make an open source version of it: for educational purposes, and to let the community add the features that they want, self-host it on their own servers, have fun with friends and more.
  
3. **Any plans on adding an online server to compete with Agar.IO or making money out of it?**

 Possibly, but either way, this version of the game belongs to the open-source community, and it will remain open-source, even if commercial plans come into play for myself, personally. 
  
4. **Can I deploy this game to my own server?**

  Sure you can! That's what it's made for! ;)
  
5. **I don't like HTML5 canvas. Can I write my own game client with this server?**

  Of course! As long as your client supports WebSockets, you can write your game client in any language/technology, even with Unity3D if you want (there is an open source library for Unity to communicate with WebSockets)!
  
**TODO**
Here is an example video taken from Chopcoin.io to sho what I am trying to achieve and here is a list of the items I still have not gotten done yet. Always open to new ideas and suggestions too!
<ol>
    <li>Need to make eating other players and Cell Rejoining a more smoother action. As of now, once a cell "covers" another cell enough         for it to trigger an "absorb" action, it "pops". A smoother transition is needed. (For example, see https://chopcoin.io)</li>
    <li>Implement skins feature. Skins will be simple graphics that will fit on a players cell, rowing with it and also apparing on             every cell when a player splits. Skins should be 1 color, more like a sillouhette, for network lag consideration. (For example,         see https://chopcoin.io)</li>
    <li>Bombs. Currently, the bombs that cause players to explode into mmultiple smaller pieces when a player hits them, are drawn onto         the canvas as larger, non-moving circles. Need to change them to a sprite. Also, a player should be able to eject mass and if           mass hits the bombs , it should cause a new bomb to spwan from the original bomb with accelreation away from the original bomb.         This allows players to "shoot" other players with bombs essentially. Finally, if a player is split into th max number of pieces         allowed, absorbing a bomb smaller than the cell should cause the cell to gain the bombs mass, which should be set to 4 times its         actual size. </li>
    <li>Create different game modes. </li>
    <li>Improve front end ui</li>
 </ol>
**License**
This project is licensed under the terms of the **MIT** license.
