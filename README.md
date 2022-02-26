# Prettier Login Screen for Foundry VTT
Based on [code by u/bass-blowfish](https://www.reddit.com/r/FoundryVTT/comments/nmbq55/version_2_more_user_friendly_login_screen/), this simple, v0.8.x and v9 compatible CSS aims to make the login screen for worlds in [Foundry VTT](https://www.foundryvtt.com/) a little bit prettier by tidying up the interface and including custom logos. The CSS can be applied by adding it to the `style.css` file in the `/resources/app/public/css` folder of your Foundry installation and includes instructions on how to insert your images and adjust certain variables like button colour.

## How to use this module
1. Download this module as Add-on module. (manifest url : https://raw.githubusercontent.com/jbblily/Foundry-VTT-Prettier-Login-Screen/jbblily-patch-1/module.json)
2. On Setup screen, go to Configuration tab. Find "Default Language".
3. Set defalt lanuage as "Latine - Prettier Login Screen". 
![image](https://user-images.githubusercontent.com/18694887/155840581-859ce741-cd48-490e-9fcd-9173b4aeca59.png)
4. Restart the Foundry

## Notice
This module is technically considered as "Core Translation Moudule", which means **you can't use this module if you are using another core translation module**.

Foundry's language file falls back to default language (English) if your json file doesn't contain appropriate keys. 

Therefore, the screen will be shown as English, with world's login screen css applied.

A user can only use one core translation module at a time. 

If you are already using other core translation module, you should manually add css file to your module.


## Example images
![Login screen example with logo](https://user-images.githubusercontent.com/18694887/155850580-f714742a-2a68-4a15-94f9-dcfbe62bf208.png)

![Login screen example without logo](https://static.dnd.theepicsnowwolf.com/naoulan/foundry/css_example_with_world_title.jpg)
