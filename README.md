# Prettier Login Screen for Foundry VTT
Based on [code by u/bass-blowfish](https://www.reddit.com/r/FoundryVTT/comments/nmbq55/version_2_more_user_friendly_login_screen/), this simple, v0.8.x compatible CSS aims to make the login screen for worlds in [Foundry VTT](https://www.foundryvtt.com/) a little bit prettier by tidying up the interface and including custom logos. The CSS can be applied by adding it to the `style.css` file in the `/foundry_vtt/resources/app/public/css` folder of your Foundry installation.

![Login screen example with logo](https://static.dnd.theepicsnowwolf.com/naoulan/foundry/css_example.jpg)

If you want to keep the original world title instead of replacing it with an image, simply remove the declaration under `/* Logo as world title */` and replace the first declaration with the following code:
```css
/* Hide world description and session info */
#join-game .right.flexcol, #join-game .app:not(#world-title) h1, #join-game .left.flexcol .app:nth-of-type(2) {
    display: none;
}
```
![Login screen example without logo](https://static.dnd.theepicsnowwolf.com/naoulan/foundry/css_example_with_world_title.jpg)
