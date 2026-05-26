# Better Toast

Frosted-glass pill toast notifications for [Zen Browser](https://zen-browser.app/).

## What it does

Replaces the default Zen toast with a pill-shaped frosted glass notification that:

- Blurs whatever is behind it (`backdrop-filter: blur(12px) saturate(1.6)`)
- Sits at **10vw / 10vh** from the screen edge — never hugging corners
- Floats above everything (`z-index: 2147483647`, `position: fixed`)
- Adapts to dark and light mode automatically
- Highlights in your Zen accent color on hover

## Position settings

Controlled from Zen Browser → Settings → Mods → Better Toast:

| Setting | Options | Default |
|---|---|---|
| Vertical | Top / Bottom | Top |
| Horizontal | Auto / Left / Center / Right | Auto |

**Auto** is sidebar-aware — places the toast on the opposite side from your sidebar.

## Install

**From the store:** Settings → Mods → Browse → search "More Better Toast"

**Manually:**
1. Settings → Mods → Add from file
2. Select the folder containing `chrome.css` and `metadata.json`
3. Enable the mod

## Customise

Edit the variables at the top of `chrome.css`:

```css
--mbt-blur:         12px;    /* blur intensity */
--mbt-radius:       999px;   /* lower = rounded rect instead of pill */
--mbt-padding:      8px 16px;
--mbt-font-size:    12px;
--mbt-max-width:    320px;
```

## Files

| File | Purpose |
|---|---|
| `chrome.css` | All styles |
| `metadata.json` | Mod metadata + preference definitions |
| `preferences.json` | Store preference schema |

## Troubleshooting

If blur doesn't show: open `about:config` and set `layout.css.backdrop-filter.force-enabled` to `true`.

## License

MIT
