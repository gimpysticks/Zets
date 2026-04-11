---
title: discord_browser_Hijack
created: 2026-03-04
---

Let me check what `xdg-open` is actually routing Discord URLs to — the Discord Flatpak may have registered itself as a handler for `discord.com` URLs:

**Command Executed:**
```bash
xdg-mime query default x-scheme-handler/https && grep -r "discord" ~/.config/mimeapps.list /var/lib/flatpak/exports/share/applications/ 2>/dev/null | head -20
```

**Output:**
```
firefox.desktop
```


**Command Executed:**
```bash
grep -r "discord" ~/.config/mimeapps.list ~/.local/share/applications/ 2>/dev/null; flatpak info com.discordapp.Discord 2>/dev/null | grep -i version
```

**Output:**
```
     Version: 0.0.127
```

No Discord MIME handlers found. Let me check the Flatpak's desktop file to see if it's registered as a handler for Discord URLs:

**Command Executed:**
```bash
cat /var/lib/flatpak/exports/share/applications/com.discordapp.Discord.desktop 2>/dev/null || flatpak run --command=cat com.discordapp.Discord /app/share/applications/com.discordapp.Discord.desktop 2>/dev/null
```

**Output:**
```
[Desktop Entry]
Name=Discord
StartupWMClass=discord
Comment=All-in-one voice and text chat for gamers that's free, secure, and works on both your desktop and phone.
GenericName=Internet Messenger
Exec=com.discordapp.Discord %U
Icon=com.discordapp.Discord
Type=Application
Categories=Network;InstantMessaging;
X-Desktop-File-Install-Version=0.28
MimeType=x-scheme-handler/discord;
```

Let me check if Firefox has Discord configured as a protocol handler (from a previous visit):

**Command Executed:**
```bash
grep -r "discord" ~/.mozilla/firefox/*.default*/handlers.json 2>/dev/null || grep -r "discord" ~/.mozilla/firefox/*/handlers.json 2>/dev/null
```

**Output:**
```
/home/sticks/.mozilla/firefox/4xgwnmpi.default-release-1/handlers.json:{"defaultHandlersVersion":{},"mimeTypes":{"application/pdf":{"action":3,"extensions":["pdf"]},"image/webp":{"action":3,"extensions":["webp"]},"image/avif":{"action":3,"extensions":["avif"]}},"schemes":{"mailto":{"stubEntry":true,"handlers":[null,{"name":"Gmail","uriTemplate":"https://mail.google.com/mail/?extsrc=mailto&url=%s"}]},"warp":{"action":4},"nordvpn":{"action":4},"discord":{"action":4},"antigravity":{"action":4}},"isDownloadsImprovementsAlreadyMigrated":false}
/home/sticks/.mozilla/firefox/5w42yuga.default-release/handlers.json:{"defaultHandlersVersion":{},"mimeTypes":{"application/pdf":{"action":3,"extensions":["pdf"]},"image/webp":{"action":3,"extensions":["webp"]},"image/avif":{"action":3,"extensions":["avif"]}},"schemes":{"mailto":{"stubEntry":true,"handlers":[null,{"name":"Gmail","uriTemplate":"https://mail.google.com/mail/?extsrc=mailto&url=%s"}]},"warp":{"action":4},"nordvpn":{"action":4},"discord":{"action":4}},"isDownloadsImprovementsAlreadyMigrated":false}
```

Found the issue. Firefox has Discord's protocol handler set to `"action":4` (use system default), meaning when Discord's webpage fires a `discord://` redirect, Firefox automatically launches the Discord app and the browser tab gets hijacked.

This isn't a script problem — it's a Firefox setting. To fix it:

1. Open Firefox → **Preferences** → **General**
2. Scroll to **Applications**
3. Find **discord** in the list
4. Change the action from "Use Discord (default)" to **"Always Ask"**

That will stop Firefox from silently handing off Discord URLs to the app, and the tab will stay in the browser.
