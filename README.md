# ColonEmoji

**Discord-style `:emoji:` autocomplete and a `::` emoji picker, on every website.**
Works in Chrome, Edge, Brave and Firefox (Manifest V3) — no account, no tracking,
nothing you type ever leaves your browser.

## What it does

- Type `:fir` → ranked suggestions, `Tab`/`Enter` inserts the emoji
- Type `::` → full searchable picker with categories and recents
- Type a complete shortcode like `:fire:` → it converts as you type;
  Backspace once brings the shortcode back selected, Backspace again clears it
- Learns what you actually use (frecency ranking) and remembers recent emoji
- Custom Discord server emoji (`<:name:id>` → image insert)
- Per-site on/off switch, toolbar toggle, `Alt+Shift+E` global shortcut
- Skin tones, `flag_<cc>` + country-code aliases, searchable by alias, tags and description

## Install

**Firefox**

1. Download `colonemoji-1.0.0.zip` from this repository.
2. Open `about:debugging` → **This Firefox** → **Load Temporary Add-on…**
3. Select the zip (rename it to `.xpi` if the file picker asks).

Temporary add-ons are removed when Firefox restarts — the permanently signed
version is coming to Firefox Add-ons (AMO).

**Chrome / Edge / Brave — Windows, no developer mode**

Stock Chrome refuses to install extensions from anywhere but its Web Store, and
it also ignores `--load-extension` these days — the one supported no-store route
is a policy install, which needs **one double-click, never developer mode**:

1. Go to **[Releases](https://github.com/Azaanrocks/ColonEmoji/releases)** and
   download **`install.reg`**.
2. Double-click it → *Yes* → *Yes* (UAC asks for admin **once** — this is not
   developer mode, nothing gets enabled).
3. Chrome (restart it) silently downloads the extension from the release and
   installs it. It also **auto-updates** itself from the same place forever.

To remove it: download **`uninstall.reg`** from the release, double-click, restart Chrome.

> Fallback for tinkerers/macOS/Linux: extract the zip, open `chrome://extensions`,
> enable *Developer mode*, *Load unpacked*. Nothing about the extension requires
> developer mode — only that manual fallback does.

## Privacy

- Single permission: `storage` (your settings and recents).
- **Nothing you type is logged, stored off-device or transmitted.** No analytics,
  no remote code, no background workers.
- The only network requests are loading *your own* custom Discord emoji images,
  on demand.

## License

**Free to use, forever. Not free to change.** No modifications, no derivatives;
exact unmodified copies may be shared. The full terms ship inside the package
(`LICENSE` inside the zip).
