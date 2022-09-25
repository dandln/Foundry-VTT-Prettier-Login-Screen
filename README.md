# Prettier Login Screen for Foundry VTT
Based on [code by u/bass-blowfish](https://www.reddit.com/r/FoundryVTT/comments/nmbq55/version_2_more_user_friendly_login_screen/), this simple CSS aims to make the login screen for worlds in [Foundry VTT](https://www.foundryvtt.com/) a little bit prettier by tidying up the interface and including custom logos. It is compatible with FoundryVTT version 0.8.X, v9 and v10.

## Manual Installation
Add the CSS to the `style.css` file in the `/resources/app/public/css` folder of your Foundry installation. The code includes instructions on how to insert your images and adjust certain variables like button colour.

## Installation through a Translation Module (v10 only)
Installing the CSS as a module ensures that your modifications/additions to the CSS will not be lost with a Foundry update. See below for limitations.
1. Install the module in Foundry through this manifest URL: `https://raw.githubusercontent.com/TheEpicSnowWolf/Foundry-VTT-Prettier-Login-Screen/main/foundry-module/module.json`
2. Still in Foundry's Setup screen, go to "Configuration" and set "Default Language" to `Latin - Prettier Login Screen`
![image](https://user-images.githubusercontent.com/18694887/155840581-859ce741-cd48-490e-9fcd-9173b4aeca59.png)
3. Save the configuration and restart Foundry
4. The CSS sits in your user data folder at `/Data/modules/prettier-login/foundry_login.css`. The code includes instructions on how to insert your images and adjust certain variables like button colour.

### Limitations
The module provided here is technically a Core Translation Module, as those allow to inject CSS that is loaded before logging into a world. It includes an empty translation catalogue for Latin, and as Foundry falls back to English for all strings not translated by the active translation module, it is able to still apply the CSS modifications while not actually changing any text.

However, this also means that **you will not be able to use it if you are using Foundry in any language other than English.** If you do, your only way to apply the CSS to the login screen will be to install it manually.

## Example images
![Login screen example with logo](https://user-images.githubusercontent.com/18694887/155850580-f714742a-2a68-4a15-94f9-dcfbe62bf208.png)

![Login screen example without logo](https://static.dnd.theepicsnowwolf.com/naoulan/foundry/css_example_with_world_title.jpg)
