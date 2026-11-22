<p align="center">
  <img src="images/banner.png" width="100%" alt="NOTORYX Connect: Engineered for independence.">
</p>

# NOTORYX Connect downloads

**An independent field app for LoRa mesh radios running Meshtastic® firmware, for Android, macOS and Windows.** Part of the **NOTORYX** off-grid communications family.

This repository hosts NOTORYX Connect builds. Get the latest from **[Releases](../../releases)**. NOTORYX Connect is free software under GPL-3.0; to get the source code for any build, [open an issue](../../issues/new) here.

<p align="center">
  <img src="images/home.png" width="190" alt="Home: radio readout, trip plan, check-in and hold for SOS">
  <img src="images/chats.png" width="190" alt="Chats: channels and direct messages">
  <img src="images/nodes.png" width="190" alt="Nodes: active nodes with distance, hops, battery and signal">
  <img src="images/traffic_map.png" width="190" alt="Map with the live Traffic view: a packet hopping through a relay">
</p>
<p align="center">
  <img src="images/tools.png" width="190" alt="More, Tools: connection doctor, timeline, field guide, antenna hunt and mesh activity">
  <img src="images/sarneg.png" width="190" alt="SARNEG code word: today's word hidden, share, and encode by hand">
  <img src="images/field_records.png" width="190" alt="Field records: incident log, templates, coverage and bot safeguards">
  <img src="images/settings.png" width="190" alt="More, Settings: radio, phone location sharing and position precision">
</p>

<sub>Screenshots show the default BLACKOUT theme, rendered from the app's built-in demo mode (a pretend radio and mesh with made-up names). Map tiles need the internet, so the base map is blank in these renders.</sub>

## Why NOTORYX Connect?

Most mesh apps are built for poking at radios at your desk. NOTORYX Connect is built for when you're out there and the cell bars are gone.

- **It's built for the field.** A dark, high-contrast interface (the BLACKOUT theme by default) with big targets, a deployment checklist, battery runtime math, an incident log and check-in templates. Everything you reach for at the trailhead is one tap from the bottom bar.
- **It watches your back.** Plan a trip with up to 6 contacts, check in with one tap, and **hold for SOS** to repeat a call for help until someone answers. The team map shows where each contact was last heard, how long ago, and the trail they took.
- **It doesn't pretend.** Every radio setting you save is read back from the radio before the app calls it done. If the radio didn't take the change, you'll know. Delivery states come from real routing acknowledgments, not a hopeful checkmark.
- **Your messages don't vanish.** Type with no radio connected and they queue on the phone, then go out when the link comes back. History, queues and nodes are kept separately for every radio you own.
- **It stays connected.** Bluetooth, Wi-Fi or USB. A background service keeps the link up with the screen off, it reconnects on its own when you walk back into range, and the connection doctor explains what's wrong when it can't.
- **Your data is yours.** No account, no analytics, no ads and no NOTORYX servers. Everything stays in the app's private storage on your phone, location sharing is opt-in and can be rounded before it leaves the phone, and backups are encrypted with your password.
- **The bot has manners.** Bot Mode auto-replies with quiet hours, rate limits, per-node cooldowns and loop protection, so it can't spam the mesh.
- **Try it without a radio.** Demo mode gives you a pretend radio and mesh to explore. Nothing is sent.
- **It's free and open source.** GPL-3.0, independently built, with its own identity. In English, Spanish, French and German.

## Latest: v1.0.0-beta.37 (22 November 2026)

**[v1.0.0-beta.37](../../releases/tag/v1.0.0-beta.37)** (build 41): **drive recording**. A new **Drive** screen in More › Tools maps where the mesh reaches as you drive. It shows a live map of your trail and coverage squares (100 m or 300 m), keeps direct and relayed readings apart, and counts distance, nodes heard and squares covered. GPS keeps running with the screen off while a drive records. Drives export as GPX, KML, CSV, GeoJSON or a drive file, with the first and last 500 m left out by default. An optional two-way check is off by default. Not yet tested on radios or on a drive.

### New since beta.31
- **Drive recording:** Drive screen with a live coverage map, direct vs relayed readings, screen-off GPS, saved drives, exports and import, and an optional two-way check (beta.37).

- **BLACKOUT look:** new app icon and BLACKOUT as the default theme; themes cut to BLACKOUT, Blaze, Bare Beauty, Okabe-Ito and Night Ops (beta.36).
- **Imported nodes show in the Nodes list** and the Home count (beta.35).
- **SARNEG hardening:** the clipboard, the encode/decode box and an opened decode line clear after 1 minute, a shown code word hides after 30 seconds, a **Random word** button, a warning for well-known code words, and no screenshots of the code-word screens on Android (beta.34).
- **Frosted glass look** closer to NOTORYX Core: floating glass tab bar, a new header with the radio's status, an instrument panel and field tools on Home (beta.33).
- **SARNEG code words:** send grids, frequencies and times as letters from a code word your team agrees on, and tap a received `[SARNEG]` message to decode it. It keeps numbers away from a casual listener; it isn't encryption. [What SARNEG is and why we added it](https://meshmayhem.org/notoryx/#sarneg) (beta.32).
- **Five tabs** (Home, Chats, Nodes, Map, More), glass cards over a backdrop you can change, a color or photo for any node, and sensors on Home (beta.32).
- **New tools** in More › Tools: **track log**, **trail routing**, **team setup QR**, **mesh activity**, **antenna hunt**, **battery watch**, a **field guide**, and an optional **SOS relay** (beta.32).

## Earlier highlights

Shipped between v1.0.0-beta.5 and v1.0.0-beta.31. See each release for details.

- **Connect over Wi-Fi or USB** as well as Bluetooth, with a **connection doctor**, **demo mode**, a home-screen widget and a Quick Settings tile.
- **Trip readiness** check, airtime-aware SOS, a **check-in delivery map**, zone and off-route alerts, **day replay** of team positions, and a shareable trip plan.
- **NodeVault** with a favorites filter, **node journal**, telemetry charts, **network diagram**, **mesh health** and node-key change alerts.
- Map: **place search**, rally points and routes, traceroute on the map, coverage heatmap, **topo map and line-of-sight planner**, **GPX/KML/GeoJSON layers** and **offline maps from MBTiles**, plus a list view for screen readers.
- Messaging: reactions, replies, @mentions, pins and unread markers, **forward** and **send later**, delivery receipts that say whether the radio proved delivery, hops and signal on each message, an airtime estimate while typing, and a lookalike-name warning.
- **SALUTE** and **9-Line** report forms, **automations**, a **timeline**, offline **checklists**, and optional **community moderation** (off by default).
- **Two-way ATAK** (asks before sharing positions), **MQTT client proxy**, **remote admin**, per-channel position precision, identity key backup and a new-radio checklist.
- Optional **app lock** and **encrypted chat history** in an on-phone database.
- **App-wide search** (beta.31), **Discard changes?** on radio settings pages (beta.30), private keys for new channel slots (beta.29), **node import** (beta.28), a **live Traffic map**, **range rings** and stale-node marking (beta.24 to 27), and redone **Nodes** and **Chats** tabs (beta.18 to 22).
- **Spanish, French and German** translations (unreviewed).
- **macOS and Windows** downloads.

## Everything it does

### Trip safety
- **Home** tab with an instrument panel (battery, voltage, channel use, nodes) and field tools.
- **Plan your trip:** up to 6 trip contacts, an overdue alert (30 min to 8 h) and a check-in reminder.
- **Check in** with one tap: I'm OK, At camp, Delayed or Heading back. Each goes to every trip contact as a direct message with the time, your position and battery. You see who it reached and can resend to the rest.
- **Hold for SOS** for 2 seconds (TalkBack users get a confirmation instead). It goes to your trip contacts and optionally a channel, repeats every 5 minutes up to 12 times, stops when a contact answers, and **I'm safe** sends an all-clear.
- **SOS relay** (off by default): passes on, once, a NOTORYX SOS that reached you with no hops left.
- **Team setup QR:** channels, radio settings and trip contacts in one scan.

### Connecting
- Scan for nearby radios with live Bluetooth signal strength, then connect in one tap.
- A verified session: NOTORYX Connect checks the Meshtastic service, runs the PhoneAPI handshake and syncs the node database before it says **READY**.
- Automatic reconnect with backoff. It respects a manual disconnect and waits for Android Bluetooth to come back on.
- Background connection service so the link survives the screen turning off.

### Search
- One search button on every tab finds nodes (by name or node ID, with or without `!`), channels, messages (accents don't matter), saved places and settings or tools.

### Messaging
- Chats is a list of conversations, one per channel and one per direct chat, each with its own unread count.
- Channel and direct messages, with a thread for each node.
- Delivery states from routing acknowledgments.
- Offline queue: messages wait on the phone and send when the radio reconnects.
- Choose any enabled channel slot for each message. The 228-byte limit is shown as you type.
- Quick replies: Copy, On my way, Need assistance, What is your position?
- Search across all saved messages, including queued ones.
- Message timeline and received-signal (SNR) history for the session.
- Chat history (500 to 5,000 messages per conversation, your choice), queues and nodes kept separately for each radio.
- Optional message notifications.
- **SARNEG code words:** a button in the message box codes numbers as letters before you send, and received `[SARNEG]` messages get a tap-to-decode line. Share the word by QR code. Not encryption.
- Emoji reactions (tap a message), a draft saved for each conversation, and a **via MQTT** label on messages that came over the internet.
- **Ignore** or **mute** a node, and hide messages containing words you choose. An SOS reply from a trip contact is never missed, even if you ignored them.
- Optional automatic deletion of old channel messages (direct messages are kept) and reading new messages aloud.
- App-icon shortcuts: Check in / SOS, Chats, Nodes and Map.

### Nodes and NodeVault
- Live mesh node list grouped into Active now, Today and Older, with distance, hops, battery and signal on each row.
- **Stale** marking for nodes that have gone quiet (Off, 1 h, 6 h, 24 h, 3 days or 7 days).
- **Import nodes** from a Meshtastic app node database export.
- **NodeVault:** every node your radios have heard, saved on the phone, with favorites and your own notes.
- Node details: telemetry, position, signal history and neighbors.
- Request position or telemetry from a node.
- **Traceroute** with the SNR of every hop.

### Maps and location
- Map of node positions and waypoints from the mesh. Create your own waypoints too. Nodes at the same spot share one pin.
- **Live Traffic map:** packets your radio hears drawn hop by hop, coloured by type.
- **Range rings** around your radio with distance labels and N/E/S/W marks.
- **Team view:** each trip contact's status (fresh, stale or lost), distance, direction and battery, with the position's age on their pin.
- **Trails** of where your trip contacts and you have been over the last 24 hours.
- **Export GPX** of waypoints and trails to open in other mapping apps.
- **Track log** with a stray warning, and **trail routing** over trails you download beforehand (the download sends the area's bounds to OpenStreetMap's Overpass service).
- **Units:** miles and feet, or kilometers and meters, set from your region by default.
- OpenStreetMap areas you've viewed are cached offline for a year.
- Opt-in phone location sharing, with optional rounding (about 360 m, 1.5 km or 6 km) before it leaves the phone.
- Low-power field mode, which lowers GPS accuracy and update rate to save battery.

### Field tools
- **Deployment checklist:** radio charged, antenna attached, region configured, primary channel verified, GPS/position policy checked.
- **Battery runtime calculator** from battery capacity and average current.
- **RSSI field reference:** what Bluetooth signal-strength numbers mean in practice.
- **Incident log:** up to 500 private notes, tagged with your radio, exportable as CSV.
- **Emergency and check-in templates** (assistance, check-in, all-clear). You fill in the details, pick a channel and review the exact text before it's sent.
- **Drive recording:** record where you were and the signal (SNR and RSSI) you received from each node, with direct and relayed readings kept apart. See it live on a map of 100 m or 300 m squares, keep each drive, and export it as GPX, KML, CSV, GeoJSON or a drive file. GPS keeps running with the screen off while a drive records. Recording stops on its own when you disconnect.
- **Range test** log with signal and distance for each packet, and gaps that show lost packets.
- **Store & forward:** replay messages you missed from a router node.
- **Mesh beacons:** see the beacons your radio hears, review and join a channel a beacon offers, or send a beacon by hand (up to once an hour).
- **Local mesh discovery** (read-only for now): plan a listen across LoRa presets and see the nodes your radio has already heard.
- **Mesh activity:** field stats, network changes and a live packet log.
- **Antenna hunt:** clicks speed up as one node's signal gets stronger.
- **Battery watch:** every node that reports its battery, the most worrying first.
- **Field guide:** mesh basics, batteries in the cold, solar and antennas.

### Field alerts (phone notifications only, nothing is sent over the mesh)
- Low battery on your radio or a favorite, at a threshold you set.
- A new node heard for the first time.
- A favorite going quiet for longer than you set while you're connected.

### Bot Mode
- Away auto-reply on a channel you choose.
- Quiet hours (default 22:00–07:00), 6 replies an hour, 30 seconds between replies and a 5-minute cooldown per node.
- Ignores replays, old messages, replies from NOTORYX bots and messages meant for other nodes.

### Radio management
- Edit every config section and module through a generated settings form: owner, LoRa (modem preset, transmit, RX boosted gain, external LNA), channels, device role, position (fixed position, smart broadcast) and more.
- **Settings availability** check shows which sections your radio actually returns.
- Saves need an authenticated, connected session and your confirmation, and every save is verified with a fresh read from the same radio.
- Share channels as `meshtastic.org/e/#` links or QR codes, and import them by link or by scanning a QR code with the camera. Add to your channels or replace them all.

### Backups and privacy
- **Encrypted radio backup and restore:** settings, all channel slots, owner names and modules, encrypted with AES-256-GCM (PBKDF2, 600,000 iterations). Preview before restoring, then the result is read back from the radio. Device identity keys and session credentials are never included.
- **Encrypted phone data backup** to a file: chats and queues for every radio, NodeVault, waypoints, field records and settings. Perfect for moving to a new phone. Restore rolls back if anything fails.
- **Privacy & data** screen that lists exactly what's stored and what's sent, with buttons to delete chat history or all phone data.

### Look and feel
- Five themes: **BLACKOUT** (the default), Blaze, Bare Beauty (light), Okabe-Ito (color-blind safe) and Night Ops (dim reds), all checked for readable contrast.
- Glass cards over a backdrop you choose (theme glow, a color, a gradient or your photo), and an optional second theme for dark mode.
- Hide the dashboard sections you don't use.
- Follows your phone's text size. Status switches to an icon with a spoken label when text is large.

<p align="center">
  <img src="images/privacy.png" width="190" alt="Privacy and data: what's stored and what's sent">
  <img src="images/radio_backup.png" width="190" alt="Encrypted radio backup">
  <img src="images/phone_backup.png" width="190" alt="Phone data backup">
  <img src="images/home_light.png" width="190" alt="Home in the light Bare Beauty theme">
</p>

> NOTORYX Connect is a test beta. The latest betas were checked on one phone (a Samsung Galaxy A15) with one radio (a Seeed T1000-E). Many newer features, and the macOS and Windows builds, have automated tests but haven't been checked on a range of hardware yet. Don't rely on it as your only way to call for help.

## Which file do I need?

| You have | Download | Notes |
|---|---|---|
| An Android phone (ARM64) | `NOTORYX-Connect-<version>-<build>.apk` | Signed with the release key. Check it with `SHA256SUMS.txt` and `SIGNATURE.txt` |
| A Mac (Intel or Apple silicon) | `NOTORYX-Connect-<version>-<build>-macOS-universal.zip` | Not notarized: right-click the app and choose **Open** the first time |
| A Windows PC (64-bit) | `NOTORYX-Connect-<version>-<build>-Windows-x64-setup.exe` or `-Windows-x64.zip` | Installs for your user, no admin needed. Not code signed, so SmartScreen warns on first launch |

The `.aab` is for the Play Store, not for installing directly. There is no iPhone release yet.

Betas are marked as pre-releases, so look through the **[Releases](../../releases)** list rather than only at "Latest". The newest is **v1.0.0-beta.37** (build 41).

## Install on Android

1. On your phone, open the latest release and download the `.apk`.
2. Open the file. If Android asks, allow installs from your browser or file manager.
3. Open NOTORYX Connect and allow **Bluetooth**, **location** and **notifications** when asked.
4. For a steady background link, set the app's battery use to **Unrestricted** (**More → Settings → Background connection** shows how).

**Updating?** Newer betas install over older ones and keep your data. Don't uninstall first.

**Coming from v0.1.3-beta.1 or earlier?** The app ID changed from `org.backcountrysignal.bastion` to `com.bastionmesh.connect`, so the new app installs separately. In the old app, make a backup (**More → Settings → Phone data backup / restore**), install the new app, restore the backup there, then uninstall the old one. You only do this once.

## About

NOTORYX Connect (formerly Bastion) is independently developed and is not affiliated with, sponsored by, endorsed by, or an official application of Meshtastic LLC. Meshtastic® is a registered trademark of Meshtastic LLC; references to it describe compatibility only.
