# TankTroubleDarkMaze

TTDM is a lightweight simple browser extension for the online game *Tank Trouble* that replaces the in-game maze background texture with one that is dark-themed.

#### It works best when used with CommanderAnime's [TankTroubleAddons](https://github.com/turtlesteak/TankTroubleAddonsFinale) extension!
[TankTroubleAddons](https://github.com/turtlesteak/TankTroubleAddonsFinale) has a dark theme for the *Tank Trouble* website content, which blends nicely with TTDM's dark theme mazes - reducing eye strain for your midnight mayhem needs!

## Features
- Dark theme for lobby mazes and game mazes.
- Light colored bullets and shrapnel.
- Transparent tank destruction fragments.
- Orange tinted tank destruction smoke. (The original black smoke was impossible to see with the dark theme maze background.)
- Outline around tank tracks. (Slightly transparent, matches the color of the tank hull - useful for improving hitbox visibility if you are using dark colored tracks.)
- Support for holiday themes. (Hopefully... This can only be tested when TT Staff enables a holiday theme!)
- Support for HD texture variants. (See the "How it works" section for more info.)

[![image.png](https://i.postimg.cc/wvPggvDw/image.png)](https://postimg.cc/hz9H0Kym)

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

This process works the same for the lobby maze backgrounds as well as the HD texture variants of both the lobby and the game.  
HD variants are loaded when your browser's zoom level is above 100%. (HD variants are a default *Tank Trouble* feature, not a TTDM feature!)

The [server](https://tanktroubledarkmaze.pages.dev/) hosting the dark-themed texture images is operated entirely on Cloudflare's "Pages" network.   
If the files become outdated, they can be updated on the server-side without requiring users to download a new version of the extension.

[![image.png](https://i.postimg.cc/6qvzT9mW/image.png)](https://postimg.cc/9wcynj2K)

## Editor's note
This project is my first-ever public release. I have never previously used GitHub, nor have I ever created a browser extension of any kind.  
I am experienced in Python, Lua, and AutoIt but I don't have much experience or knowledge in JavaScript, HTML, and JSON.  
If anything is broken or not working correctly, please let me know!

I will try my best to keep this extension maintained and up to date with the latest version of the game.  

Thank you 😊
