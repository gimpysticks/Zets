# Twitch Chat Slash Commands

## General Viewer Commands

| Command | What It Does |
| :--- | :--- |
| `/mods` | Lists all moderators in the channel |
| `/vips` | Lists all VIPs in the channel |
| `/vote` | Vote in the channel's active poll |
| `/color {colorname}` | Changes your username color (Blue, Red, Green, HotPink, etc.) |
| `/color {#hex}` | Turbo users can set any hex color (e.g. `#FF5733`) |
| `/block {username}` | Blocks all messages and whispers from a user |
| `/unblock {username}` | Removes a user from your block list |
| `/disconnect` | Disconnects you from chat (refresh to reconnect) |
| `/w {username} {message}` | Sends a private whisper to another user |
| `/me {message}` | Posts a message in italics/colored text as an action |
| `/gift {quantity}` | Gifts a number of subs to the community |
| `@{username}` | Tags or replies to a specific user's message |

## Moderator Commands

| Command | What It Does |
| :--- | :--- |
| `/ban {username}` | Permanently bans a user from chat |
| `/unban {username}` | Removes a ban |
| `/timeout {username} [seconds]` | Temporarily silences a user (default 600s) |
| `/untimeout {username}` | Removes a timeout early |
| `/warn {username}` | Issues an official warning to a user |
| `/slow [seconds]` | Enables slow mode — limits how often users can chat |
| `/slowoff` | Disables slow mode |
| `/subscribers` | Enables subscribers-only chat mode |
| `/subscribersoff` | Disables subscribers-only mode |
| `/followers [duration]` | Enables followers-only chat mode |
| `/followersoff` | Disables followers-only mode |
| `/emoteonly` | Restricts chat to emotes only |
| `/emoteonlyoff` | Disables emote-only mode |
| `/uniquechat` | Prevents duplicate messages in chat |
| `/uniquechatoff` | Disables unique chat mode |
| `/clear` | Clears all chat history |
| `/announce {message}` | Posts a highlighted announcement in chat |
| `/pin {message}` | Pins a message to the top of chat |
| `/shoutout {username}` | Shows a follow button shoutout for another streamer |
| `/monitor {username}` | Flags a user's messages for monitoring |
| `/unmonitor {username}` | Removes monitoring from a user |
| `/restrict {username}` | Restricts a user's ability to chat |
| `/unrestrict {username}` | Removes a restriction |
| `/user {username}` | Opens a user's profile card with moderation details |

## Broadcaster Commands

| Command | What It Does |
| :--- | :--- |
| `/mod {username}` | Promotes a user to moderator |
| `/unmod {username}` | Removes moderator status |
| `/vip {username}` | Grants VIP status to a user |
| `/unvip {username}` | Removes VIP status |
| `/color {username}` | (Broadcaster) Changes a user's chat color |
| `/commercial [seconds]` | Runs an ad (30, 60, 90, 120, 150, or 180 seconds) |
| `/raid {username}` | Raids another channel with your viewers |
| `/unraid` | Cancels an in-progress raid |
| `/marker [description]` | Creates a stream marker for VOD editing |
| `/host {username}` | Hosts another channel (deprecated on some versions) |
| `/unhost` | Stops hosting |
