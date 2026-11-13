<p align="center">
  <img src="images/icon.png" width="120" alt="NOTORYX app icon">
</p>

# NOTORYX Connect downloads

**An independent Android field app for LoRa mesh radios running Meshtastic® firmware.** Part of the **NOTORYX** off-grid communications family. **No Towers. No Limits.**

This repository hosts NOTORYX Connect builds. Get the latest from **[Releases](../../releases)**. The source code is at [TheLogsAreScreaming/notoryx-connect](https://github.com/TheLogsAreScreaming/notoryx-connect) (GPL-3.0).

<p align="center">
  <img src="images/home.png" width="190" alt="Home: field console, trip plan, check-in and hold for SOS">
  <img src="images/trip.png" width="190" alt="Plan your trip: contacts, overdue alert and check-in reminder">
  <img src="images/beacons.png" width="190" alt="Mesh beacons heard, and sending one by hand">
  <img src="images/discovery.png" width="190" alt="Local mesh discovery planner">
</p>
<p align="center">
  <img src="images/nodes.png" width="190" alt="Nodes: scan for radios and connect">
  <img src="images/chats.png" width="190" alt="Chats: channel and direct messages with quick replies">
  <img src="images/tools.png" width="190" alt="Tools: battery runtime, RSSI guide and deployment checklist">
  <img src="images/field_records.png" width="190" alt="Field records: incident log, templates, coverage and bot safeguards">
</p>

## Why NOTORYX Connect?

Most mesh apps are built for poking at radios at your desk. NOTORYX Connect is built for when you're out there and the cell bars are gone.

- **It's built for the field.** A dark, high-contrast interface with big targets, a deployment checklist, battery runtime math, an incident log and check-in templates. Everything you reach for at the trailhead is one tap from the bottom bar.
- **It watches your back.** Plan a trip with up to 6 contacts, check in with one tap, and **hold for SOS** to repeat a call for help until someone answers. The team map shows where each contact was last heard, how long ago, and the trail they took.
- **It doesn't pretend.** Every radio setting you save is read back from the radio before the app calls it done. If the radio didn't take the change, you'll know. Delivery states come from real routing acknowledgments, not a hopeful checkmark.
- **Your messages don't vanish.** Type with no radio connected and they queue on the phone, then go out when the link comes back. History, queues and nodes are kept separately for every radio you own.
- **It stays connected.** A background service keeps the Bluetooth link up with the screen off, and it reconnects on its own when you walk back into range or flip Bluetooth back on.
- **Your data is yours.** No account, no analytics, no ads and no NOTORYX servers. Everything stays in the app's private storage on your phone, location sharing is opt-in and can be rounded before it leaves the phone, and backups are encrypted with your password.
- **The bot has manners.** Bot Mode auto-replies with quiet hours, rate limits, per-node cooldowns and loop protection, so it can't spam the mesh.
- **It's free and open source.** GPL-3.0, independently built, with its own identity.

## Everything it does

### Trip safety
- **Home** tab with a field console: radio status, node count and battery.
- **Plan your trip:** up to 6 trip contacts, an overdue alert (30 min to 8 h) and a check-in reminder.
- **Check in** with one tap: I'm OK, At camp, Delayed or Heading back. Each goes to every trip contact as a direct message with the time, your position and battery. You see who it reached and can resend to the rest.
- **Hold for SOS** for 2 seconds (TalkBack users get a confirmation instead). It goes to your trip contacts and optionally a channel, repeats every 5 minutes up to 12 times, stops when a contact answers, and **I'm safe** sends an all-clear.

### Connecting
- Scan for nearby radios with live Bluetooth signal strength, then connect in one tap.
- A verified session: NOTORYX Connect checks the Meshtastic service, runs the PhoneAPI handshake and syncs the node database before it says **READY**.
- Automatic reconnect with backoff. It respects a manual disconnect and waits for Android Bluetooth to come back on.
- Background connection service so the link survives the screen turning off.

### Messaging
- Channel and direct messages, with a thread for each node.
- Delivery states from routing acknowledgments.
- Offline queue: messages wait on the phone and send when the radio reconnects.
- Choose any enabled channel slot for each message. The 228-byte limit is shown as you type.
- Quick replies: Copy, On my way, Need assistance, What is your position?
- Search across all saved messages, including queued ones.
- Message timeline and received-signal (SNR) history for the session.
- Chat history (newest 500 per radio), queues and nodes kept separately for each radio.
- Optional message notifications.
- Emoji reactions (long-press a message), a draft saved for each conversation, and a **via MQTT** label on messages that came over the internet.
- **Ignore** or **mute** a node, and hide messages containing words you choose. An SOS reply from a trip contact is never missed, even if you ignored them.
- Optional automatic deletion of old channel messages (direct messages are kept) and reading new messages aloud.
- App-icon shortcuts: Check in / SOS, Chats, Nodes and Map.

### Nodes and NodeVault
- Live mesh node list with mesh health and signal for the session.
- **NodeVault:** every node your radios have heard, saved on the phone, with favorites and your own notes.
- Node details: telemetry, position, signal history and neighbors.
- Request position or telemetry from a node.
- **Traceroute** with the SNR of every hop.

### Maps and location
- Map of node positions and waypoints from the mesh. Create your own waypoints too.
- **Team view:** each trip contact's status (fresh, stale or lost), distance, direction and battery, with the position's age on their pin.
- **Trails** of where your trip contacts and you have been over the last 24 hours.
- **Export GPX** of waypoints and trails to open in other mapping apps.
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
- **Coverage history:** record where you were and the signal (SNR and RSSI) you received from each node, then export it as CSV. It keeps up to 2,000 readings for 30 days and stops on its own when you disconnect.
- **Range test** log with signal and distance for each packet, and gaps that show lost packets.
- **Store & forward:** replay messages you missed from a router node.
- **Mesh beacons:** see the beacons your radio hears, review and join a channel a beacon offers, or send a beacon by hand (up to once an hour).
- **Local mesh discovery** (read-only for now): plan a listen across LoRa presets and see the nodes your radio has already heard.

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
- Dark (default), light or system theme, with a NOTORYX orange accent checked for readable contrast.
- Hide the dashboard sections you don't use.
- Follows your phone's text size. Status switches to an icon with a spoken label when text is large.

<p align="center">
  <img src="images/privacy.png" width="190" alt="Privacy and data: what's stored and what's sent">
  <img src="images/radio_backup.png" width="190" alt="Encrypted radio backup">
  <img src="images/phone_backup.png" width="190" alt="Phone data backup">
  <img src="images/settings.png" width="190" alt="Settings: appearance, units, filters and messages">
</p>

> NOTORYX Connect is a beta, checked on one radio (a Seeed T1000-E) so far. Don't rely on it as your only way to call for help.

## Which file do I need?

Download the `NOTORYX-Connect-<version>-<build>.apk` from the latest release (ARM64 Android phones). Releases also include an `.aab` (for the Play Store, not for installing directly), checksums in `SHA256SUMS.txt`, and signing details in `SIGNATURE.txt`.

Betas are marked as pre-releases, so look through the **[Releases](../../releases)** list rather than only at "Latest".

## Install on Android

1. On your phone, open the latest release and download the `.apk`.
2. Open the file. If Android asks, allow installs from your browser or file manager.
3. Open NOTORYX Connect and allow **Bluetooth**, **location** and **notifications** when asked.

**Updating?** Newer betas install over older ones and keep your data. Don't uninstall first.

**Coming from v0.1.3-beta.1 or earlier?** The app ID is changing from `org.backcountrysignal.bastion` to `com.bastionmesh.connect`, so the next release installs as a separate app. In the old app, make a backup (**Settings → Phone data backup / restore**), install the new app, restore the backup there, then uninstall the old one. You only do this once.

## About

NOTORYX Connect (formerly Bastion) is independently developed and is not affiliated with, sponsored by, endorsed by, or an official application of Meshtastic LLC. Meshtastic® is a registered trademark of Meshtastic LLC; references to it describe compatibility only.
