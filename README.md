# Ore UI Web

Ore UI Web is a lightweight vanilla CSS/JS UI library with a pixel-inspired visual style.  
This refactor introduces a consistent `ore-ui-` component naming system while preserving all legacy class behavior for backward compatibility.

---

## 1) Introduction

This library now supports two class APIs:

- **Legacy classes** (existing projects keep working)
- **New unified classes** prefixed with `ore-ui-`

The visual output, spacing, colors, and interactive behavior remain unchanged for existing components.

---

## 2) Installation (CDN usage)

Use the jsDelivr CDN path:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/preload.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/libs/main.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/libs/buttons.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/libs/input.css">

<script type="module" src="https://cdn.jsdelivr.net/gh/hamalainenmiska100-hue/oreui-web@main/dist/lite.init.js"></script>
```

Recommended stylesheet order:
1. `preload.css`
2. `main.css`
3. `buttons.css`
4. `input.css`
5. optional `icons.css`, `images.css`, etc.

---

## 3) Component list

- Buttons
- Inputs
- Cards
- Switches
- Progress bars
- Icons
- Utility helpers (`ore-ui-banner`, `ore-ui-center`, `ore-ui-flex`, `ore-ui-disabled`)

---

## 4) Usage examples

### Buttons

#### Example

```html
<button class="ore-ui-btn">Default</button>
<button class="ore-ui-btn ore-ui-btn-primary">Primary</button>
<button class="ore-ui-btn ore-ui-btn-success">Success</button>
<button class="ore-ui-btn ore-ui-btn-danger">Danger</button>
<button class="ore-ui-btn ore-ui-btn-disabled" disabled>Disabled</button>
```

#### Classes

- `ore-ui-btn`: Base button style (legacy alias: `button.normal`)
- `ore-ui-btn-primary`: Primary variant (legacy alias: `.blue`)
- `ore-ui-btn-success`: Success variant (legacy alias: `.green`)
- `ore-ui-btn-danger`: Danger variant (legacy alias: `.red`)
- `ore-ui-btn-disabled`: Disabled state (legacy alias: `.disabled` on normal button)

#### Additional variants

- `ore-ui-btn-dark` (legacy alias: `.dark`)
- `ore-ui-btn-info` (legacy alias: `.skyblue`)
- `ore-ui-btn-warning` (legacy alias: `.yellow`)
- `ore-ui-btn-link` (legacy alias: `.link`)
- `ore-ui-btn-icon` (legacy alias: `.icon`)
- `ore-ui-btn-cube` (legacy alias: `.cube`)

---

### Inputs

#### Example

```html
<div class="ore-ui-input-wrapper">
  <input class="ore-ui-input" type="text" placeholder="Type here">
</div>

<textarea class="ore-ui-input ore-ui-input-multiline"></textarea>
```

#### Classes

- `ore-ui-input`: Base input appearance (aliases existing `input`, `textarea`, and contenteditable styles)
- `ore-ui-input-wrapper`: Optional wrapper utility for layout grouping
- `ore-ui-input-multiline`: Multiline treatment for textareas

---

### Cards

#### Example

```html
<div class="ore-ui-card">
  <div class="ore-ui-card-header">Card Header</div>
  <div class="ore-ui-card-body">Card content</div>
  <div class="ore-ui-card-footer">Card footer</div>
</div>
```

#### Classes

- `ore-ui-card`: Base card container (legacy alias: `.box`)
- `ore-ui-card-header`: Header region
- `ore-ui-card-body`: Body region
- `ore-ui-card-footer`: Footer region

---

### Switches

#### Example

```html
<label class="ore-ui-switch">
  <input type="checkbox">
  <span class="ore-ui-switch-slider"></span>
</label>
```

#### Classes

- `ore-ui-switch`: Switch wrapper
- `ore-ui-switch-slider`: Track + knob visual element

---

### Progress bars

#### Example

```html
<div class="ore-ui-progress">
  <span class="ore-ui-progress-bar" style="width: 60%;"></span>
</div>
```

#### Classes

- `ore-ui-progress`: Progress track container
- `ore-ui-progress-bar`: Fill element controlled by width

---

### Icons (existing)

#### Example

```html
<span class="-icon -menu"></span>
<span class="-icon -help"></span>
<span class="-icon -save"></span>
```

#### Available icon modifiers

- `-loading`, `-copy`, `-clip`, `-extlink`, `-help`, `-menu`, `-save`

---

## 5) Naming conventions

The new naming format follows simple BEM-like patterns:

- **Block/base:** `ore-ui-btn`, `ore-ui-card`, `ore-ui-input`
- **Variant/modifier:** `ore-ui-btn-primary`, `ore-ui-btn-danger`
- **Elements:** `ore-ui-card-header`, `ore-ui-card-body`, `ore-ui-card-footer`

Guidelines:
- Prefix all public component classes with `ore-ui-`
- Keep modifiers descriptive and short
- Preserve legacy class aliases for migration safety

---

## 6) Design philosophy

- **No visual regressions:** Existing components preserve the same style and behavior.
- **Backward compatible:** Legacy class names still function.
- **Predictable structure:** Components have clearer DOM patterns.
- **Vanilla-first:** No framework dependency added.
- **Progressive migration:** You can migrate class names gradually.

---

## Demo

A complete component showcase is available in `index.html` at repo root, including old and new class usage side by side.
