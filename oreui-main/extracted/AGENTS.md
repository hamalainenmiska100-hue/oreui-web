# Ore UI Web – AGENTS.md

This repository contains the **core Ore UI web assets**.

## Folder structure

- /dist  → all CSS, JS, fonts, icons (main system)
- /assets → images/icons used by the UI

Do not rename these folders.

---

## How to use in a project

Place your HTML file in the same root as `/dist` and `/assets`.

### Required HTML setup (in <head>)

<link rel="stylesheet" href="./dist/preload.css">
<link rel="stylesheet" href="./dist/libs/main.css">
<link rel="stylesheet" href="./dist/libs/buttons.css">
<link rel="stylesheet" href="./dist/libs/input.css">
<link rel="stylesheet" href="./dist/libs/icons.css">
<link rel="stylesheet" href="./dist/libs/fonts.css">

<script type="module" src="./dist/lite.init.js"></script>

---

## Critical rules

1. Always use **relative paths**
   ./dist/... and ./assets/...

2. Use:
   lite.init.js

   DO NOT use:
   all.init.js
   → it often freezes on mobile

3. Always remove loader manually:

window.addEventListener("load", () => {
  const loader = document.querySelector("loader")
  if (loader) loader.style.display = "none"
})

---

## What Ore UI actually is

Ore UI is mostly:
- CSS styles
- UI components

It is NOT a reliable JS framework.

Best usage:
→ treat it as a **design system / skin**

---

## Known issues

- all.init.js may hang (especially on iOS)
- fonts may fail if server does not serve font files correctly
- some components rely on JS that is unstable

---

## Recommendations

- Use Ore UI for styling only
- Build your own JS logic
- Test on mobile early

---

## CDN usage (optional)

You can use this repo via jsDelivr:

https://cdn.jsdelivr.net/gh/USERNAME/REPO/dist/...

Example:

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/USERNAME/REPO/dist/preload.css">

---

## Summary

- Keep /dist and /assets intact
- Use lite.init.js
- Hide loader manually
- Do not rely heavily on Ore UI JS

This package is intended to be reused as a **portable UI base** (e.g. DeepSeed).
