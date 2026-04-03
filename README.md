# oreui-web

CDN distribution of Ore UI Web.

---

## Base CDN

All files must be loaded from:

https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/

---

## Critical rule

Never use local paths like:

./dist/...
./assets/...

Always use CDN URLs.

---

## Core CSS

dist/preload.css  
Initial styles. Must be loaded first to avoid layout issues.

dist/libs/main.css  
Main UI styling system.

dist/libs/buttons.css  
Button styles.

dist/libs/input.css  
Input and form styles.

dist/libs/icons.css  
Icon system.

dist/libs/fonts.css  
Font loader definitions.

dist/libs/images.css  
Image-related styles.

---

## JavaScript

dist/lite.init.js  
Main initializer. Only recommended entry point.

dist/libs/main.js  
Core UI logic (optional).

dist/libs/info.js  
Information utilities (optional).

dist/libs/sounds.js  
Sound handling logic.

---

## NOT recommended

dist/all.init.js  
Heavy bundle. May cause infinite loading.

dist/all.init.css  
Full CSS bundle. Not needed in most cases.

---

## Fonts

All fonts are auto-loaded via fonts.css.

Examples:

dist/fonts/Minecraft-Five-48bb3.otf  
Minecraft-style font.

dist/fonts/Minecraft-Five-Bold-4ded8.otf  
Bold variant.

dist/fonts/Minecraft-Seven-66398.otf  
Alternative pixel font.

dist/fonts/Minecraft-Ten-ed29a.otf  
Extended pixel font.

dist/fonts/NotoSans-Bold-14d47.ttf  
Standard bold UI font.

dist/fonts/NotoSans-Italic-11442.ttf  
Italic font.

dist/fonts/NotoSansArabic-Regular-9137a.ttf  
Arabic support.

dist/fonts/NotoSansJP-Regular-aaed5.otf  
Japanese support.

dist/fonts/NotoSansKR-Regular-8625b.otf  
Korean support.

dist/fonts/NotoSansSC-Regular-a4317.otf  
Simplified Chinese.

dist/fonts/NotoSansTC-Regular-2eeaf.otf  
Traditional Chinese.

dist/fonts/NotoSansTamilSupplement-Regular-a407d.ttf  
Tamil support.

dist/fonts/NotoSansMongolian-Regular-f4200.ttf  
Mongolian support.

dist/fonts/NotoSansSyriac-Regular-1bff6.ttf  
Syriac support.

dist/fonts/NotoSansMerged-Regular-5df70.ttf  
Merged fallback font.

---

## Legacy (optional)

dist/legacy/mc-fonts.css  
Old Minecraft font system.

dist/legacy/notosans.css  
Legacy font config.

dist/legacy/fonts/Mojangles.ttf  
Legacy Minecraft font.

dist/legacy/fonts/minecraft-ten.ttf  
Legacy variant.

---

## Resources (images)

dist/res/Clipboard-bbbc0.png  
Clipboard icon.

dist/res/Copy-9b6af.png  
Copy icon.

dist/res/Save-72f24.png  
Save icon.

dist/res/animation-074ed.gif  
Loading animation.

dist/res/empty-state-art-461d2.png  
Empty UI illustration.

dist/res/emptyStatesNoProgress-02663.png  
Empty state variant.

dist/res/error-1ee9c.png  
Error illustration.

dist/res/external-link-b22bb.png  
External link icon.

dist/res/externalLink-0e493.png  
Alternate icon.

dist/res/help.png  
Help icon.

dist/res/menu.png  
Menu icon.

---

## Sounds

dist/sounds/modal_hide-2341f.ogg  
UI hide sound.

dist/sounds/release-7c974.ogg  
Release interaction sound.

dist/sounds/snes_pop-7a6d3.ogg  
Pop sound effect.

---

## Config

dist/oreuicfg.json  
Internal configuration file.

---

## Example usage

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/preload.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/libs/main.css">

<script type="module" src="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/lite.init.js"></script>

---

## Loader fix

<script>
window.addEventListener("load", () => {
  const loader = document.querySelector("loader")
  if (loader) loader.style.display = "none"
})
</script>

---

## What this is

Ore UI Web is:

- a CSS design system
- UI component library

It is NOT a full JavaScript framework.

---

## AI instructions

- Always use CDN URLs
- Never use ./dist paths
- Always include preload.css first
- Always use lite.init.js
- Avoid all.init.js
- Treat this as a CSS system

---

## Summary

- CDN only
- preload.css first
- lite.init.js only
- no local paths
