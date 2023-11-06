# TankTroubleDarkMaze

TTDM is a lightweight simple browser extension for the online game *Tank Trouble* that replaces the in-game maze background texture with one that is dark-themed.

It works best when used with CommanderAnime's [TankTroubleAddons](https://github.com/turtlesteak/TankTroubleAddonsFinale) extension - it has the ability to enable a dark theme for the *Tank Trouble* website.

## How it works
TTDM does not rely on any JavaScript or HTML code. It simply utilizes Google's Manifest v3 `declarativeNetRequest` redirect logic.  
The `manifest.json` file indexes the net request rule, which is defined in `RedirectRule_game.json`.

When the *Tank Trouble* website is loading, the rule causes this original HTTP request...  
[https://cdn.tanktrouble.com/RELEASE-2023-09-06-01/assets/images/game/game@2x.png](https://cdn.tanktrouble.com/RELEASE-2023-09-06-01/assets/images/game/game@2x.png)

...to be redirected to:  
[https://tanktroubledarkmaze.pages.dev/assets/images/game/dark_game@2x.png](https://tanktroubledarkmaze.pages.dev/assets/images/game/dark_game@2x.png)

The original URL is the game's default texture image, and the redirect URL is the modified dark-themed texture image.  
This redirect causes the game to load the dark-themed texture in place of the default texture.

The server hosting the dark-themed texture image is operated entirely on Cloudflare's "Pages" network.

## Editor's note
This project is my first-ever public release. I have never previously used GitHub, nor have I ever created a browser extension of any kind.  
I am experienced in Python, Lua, and AutoIt but I don't have too much experience or knowledge in JavaScript, HTML, and JSON.  
If anything is broken or not working correctly, please let me know!

I will try my best to keep this extension maintained and up to date with the latest version of the game.  

Thank you 😊
