# TankTroubleDarkMaze

TTDM is a lightweight simple browser extension for the online game *Tank Trouble* that replaces the in-game maze background texture with one that is dark-themed.

#### It works best when used with CommanderAnime's [TankTroubleAddons](https://github.com/turtlesteak/TankTroubleAddonsFinale) extension!
[TankTroubleAddons](https://github.com/turtlesteak/TankTroubleAddonsFinale) has a dark theme for the *Tank Trouble* website content, which blends nicely with TTDM's dark theme mazes - reducing eye strain for your midnight mayhem needs!

# Installation
1. [Download the latest source code](https://github.com/TankTroubleMaverick/TankTroubleDarkMaze/archive/refs/heads/main.zip) (Version 11.06.2023.02)  
2. Extract the ZIP folder to a location of your choice.  
3. Navigate to your browser's extension menu. For Chrome, this is at `chrome://extensions`  
4. Find the "Developer mode" button and turn it on. For Chrome, this is at the top right corner.  
5. Click the "Load unpacked" button.  
6. In the pop-up window, navigate to the folder you extracted in Step 2.  
7. Open it and click "TankTroubleDarkMaze-main"  
8. Click "Select Folder"  

TTDM should now show up in your browser's extension menu.  
It will run whenever you visit [Tank Trouble](https://www.tanktrouble.com)!  
If you want to restore the default light theme, disable TTDM from your browser's extension menu.

## How it works
TTDM does not rely on any JavaScript or HTML code. It simply utilizes Google's Manifest v3 `declarativeNetRequest` redirect logic.  
The `manifest.json` file indexes the net request rule, which is defined in `game-game_rule.json`.

When the *Tank Trouble* website is loading, the rule causes this original HTTP request...  
[https://cdn.tanktrouble.com/RELEASE-20XX-XX-XX-XX/assets/images/game/game.png](https://cdn.tanktrouble.com/RELEASE-2023-09-06-01/assets/images/game/game.png)

...to be redirected to:  
[https://tanktroubledarkmaze.pages.dev/assets/images/game/dark_game.png](https://tanktroubledarkmaze.pages.dev/assets/images/game/dark_game.png)

The original URL is the game's default texture image, and the redirect URL is the modified dark-themed texture image.  
This redirect causes the game to load the dark-themed texture in place of the default texture.

The server hosting the dark-themed texture image is operated entirely on Cloudflare's "Pages" network.

## Editor's note
This project is my first-ever public release. I have never previously used GitHub, nor have I ever created a browser extension of any kind.  
I am experienced in Python, Lua, and AutoIt but I don't have too much experience or knowledge in JavaScript, HTML, and JSON.  
If anything is broken or not working correctly, please let me know!

I will try my best to keep this extension maintained and up to date with the latest version of the game.  

Thank you 😊
