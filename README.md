# QuestAutocompleter

A Vencord plugin that automatically accepts and completes Discord quests.

It keeps a queue of active quests and processes them one-by-one, handling things like reloads, account switches, and mid-session enabling so it doesn’t break or double-run.


## ⚠️ Disclaimer

This plugin automates Discord quest progress. Use it at your own risk and make sure you understand Discord’s Terms of Service.

I am not responsible for any account actions, flags, or bans that may occur from using this plugin.


## Features

* Auto-complete supported quest types
* Optional auto-accept for new quests
* Queue system to avoid conflicts
* Handles reloads and account switching
* Console logging for progress/debugging


## Supported Tasks

* WATCH_VIDEO
* WATCH_VIDEO_ON_MOBILE
* PLAY_ON_DESKTOP
* STREAM_ON_DESKTOP
* PLAY_ACTIVITY

Some tasks require the Discord desktop app and will be skipped on web.


## Installation (Source Build Required)

⚠️ **This plugin requires Vencord to be built from source.**  
It will **NOT work** with the standard Vencord installer or by dropping files into AppData.

### Steps

1. Go to the plugins folder:

   ```
   src/plugins/QuestAutoCompleter
   ```

2. Create a folder `QuestAutocompleter`

3. Copy `QuestAutocompleter.tsx` into that folder and rename it to:

   ```
   index.tsx
   ```

4. Install dependencies and build Vencord:

   ```bash
   pnpm install
   pnpm build
   ```

5. Inject Vencord into Discord:

   ```bash
   pnpm inject
   ```

6. Restart Discord and enable the plugin:

   ```
   Settings → Vencord → Plugins → QuestAutoCompleter
   ```

7. (Optional) Enable auto-accept in the plugin settings.

For more information on building Vencord from source, see:
[https://docs.vencord.dev/installing/](https://docs.vencord.dev/installing/)

## Credit

The original quest completion logic was based on:
[https://gist.github.com/aamiaa/204cd9d42013ded9faf646fae7f89fbb](https://gist.github.com/aamiaa/204cd9d42013ded9faf646fae7f89fbb)

The rest of the plugin (queueing system, session handling, auto-accept logic, etc.) was built and expanded on top of that idea.

## License

GPL-3.0 (same as Vencord)

```
