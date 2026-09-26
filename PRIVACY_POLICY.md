# Hana Bot Privacy Policy

**Last updated: 26 September 2026**

This Privacy Policy explains how Hana ("Hana", "we", "us") handles information when you use the Hana Discord bot. It covers Hana's own processing; Discord and each third-party provider have their own policies.

## 1. Privacy by default

Hana normally keeps conversational memory separate by **Discord User ID + Guild (server) ID**. It does not use one server's memory in another server unless the owner of that memory enables cross-server sharing in `/settingai`.

Hana does not infer personal facts such as your age, identity, location, or relationship status. If you did not provide a fact yourself, Hana should treat it as unknown. Please do not enter highly sensitive data such as passwords, bank details, home addresses, phone numbers, government identifiers, health records, or private information about other people.

## 2. Information Hana processes and stores

Depending on the feature you use, Hana may process the following.

### Discord and server information

- Discord user, message, channel, and guild IDs; display names; and command or interaction metadata needed to answer a command, apply permissions, or enforce limits.
- Enabled RoomAI channel IDs, guild and channel names, enabled status, and recent RoomAI conversation context. Recent context is limited to the latest 16 messages before older context is discarded.
- A short link between an original RoomAI message and Hana's reply (message IDs, channel ID, reply ID, and timestamp) so Hana can remove its reply if the original message is deleted. These links expire after seven days.
- For guild admission and operational auditing: guild ID and name, owner ID and display name, total and human-member counts, and the minimum-membership check result. Hana may send this admission report to its configured operator. Hana does not automatically fetch or persist an invite or vanity URL when it joins a server.
- Hana requires at least 25 non-bot members when it is added to a server. If the fetched non-bot member count is below 25, Hana records the admission result and automatically leaves that server. If Discord does not provide enough information to verify the count, Hana records that verification failure for operational review.
- When the configured operator sends `!guildrequest <Guild ID>` or `!guildcheck <Guild ID>` to Hana in a private direct message, Hana processes that Guild ID to check whether it is installed there. `!guildrequest` fetches an invite only on demand and may return an existing invite or create a new invite only where Discord permissions permit; Hana does not persist the returned link in its guild registry, user profile, or conversation memory. `!guildcheck` returns the names, types, and visible category labels of channels Hana itself can view, so the operator can assess a reported problem before joining. For a reported outage, security concern, misuse, or support request, the operator may use an available invite to join and investigate the server. The operator can access only channels allowed by Discord permissions and must use the access for that operational purpose; it is not automatic access to the server. These requests are not stored as new user-profile or conversation-memory records.
- Server context and templates that an authorised server administrator deliberately saves for Hana to use. Administrators should not place personal or sensitive information in these fields.

### Conversation, memory, and relationship information

- Messages sent in an enabled RoomAI channel, Hana's replies, and the current RoomAI context needed to generate a response. The optional AI drawing-game prompt uses Hana's own current theme/status context, not the player’s RoomAI conversation or profile.
- If memory is enabled for that server, Hana stores a compact summary, communication preferences, topic memories, explicitly requested important memories, and unsummarised conversation lines until they can be summarised. Important memories are limited to 12 items per user per server.
- A per-user, per-server relationship record: a score and level, limited communication/boundary status, counts of repeated romance requests, activity timestamps, language preference, and a short non-sensitive callback topic. It is designed not to store raw sensitive conversation text.
- A legacy-memory archive where an older record has no known source server. Hana does not inject this archive into AI prompts unless its owner explicitly moves it through `/settingai`.
- Your `/settingai` choices, such as reply mention preference, local-memory preference, cross-server memory sharing, proactive greeting preference, time zone, and the optional profile fields you voluntarily enter (name, age, dates, and about text).

### Usage, RoomAI relay, administrator messaging, action, and voice information

- Per-user and per-guild AI request counts and date for cooldown and quota enforcement. Usage records are pruned after 14 days.
- Hana does **not** provide an anonymous `/dm` command. That command and its cooldown storage have been removed.
- If a user explicitly asks Hana in an enabled RoomAI server channel to tell another member something, Hana may temporarily store a named RoomAI relay. The record contains the guild ID, target user ID and display name, sender user ID and display name, relay type, the requested message text (up to 300 characters where present), and creation and expiry times. Hana identifies the sender when delivering the relay in RoomAI; it is not an anonymous direct message. The record is deleted after delivery or expires after seven days.
- `/dmpanel` lets an authorised server administrator send administrator-written direct messages to selected members or a selected role. Hana processes the selected recipient IDs and message long enough to perform that request. Hana does not add the message to RoomAI memory or the named-relay store. Discord may retain delivered direct messages under its own policies. Server administrators are responsible for using this feature lawfully and without spam or harassment.
- `/act` and `/actwith` request a fresh GIF from the configured image provider for each use. Hana does not maintain an action-GIF cache.
- Japan public-holiday dates returned by Nager.Date for the fixed country code `JP`, cached by year to add limited holiday context to Hana's global schedule. No Discord user, server, message, location, or device information is sent to Nager.Date.
- When you explicitly ask RoomAI about Hana's current verified travel status or use `/travelphoto <Japan prefecture>`, Hana may request a fresh stock image from Pexels using only a fixed Japan location query. RoomAI uses the current verified Hana location and attaches an image only when its supplied description matches the approved Japan place. `/travelphoto` randomly selects from a curated landmark list for the prefecture requested; where Pexels omits enough metadata to verify the exact landmark, Hana may attach a clearly labelled visual reference from that landmark search rather than claim it depicts the exact place. Hana does not send your Discord message, identity, or location to Pexels, and does not cache these photo results.
- Text submitted to `/tts` while Hana is connected to a voice channel. Hana synthesises that text; it does not record, transcribe, or store other people’s voice audio.

### Information Hana does not collect for a feature

Hana's global life schedule, character status, event state, and Sapporo weather context are not personalised user profiles. The weather request uses fixed public coordinates for Sapporo, Japan; it is not a request for your device location.

## 3. How we use information

We use the information above to:

- Run RoomAI, commands, games, TTS, named RoomAI relays, administrator messaging, action, status, and moderation/administration features.
- Keep memory, relationship context, and replies scoped to the correct user and server.
- Enforce consent controls, cooldowns, quotas, permissions, and abuse protections.
- Restore enabled RoomAI rooms after a restart and operate the bot safely.
- Diagnose service failures, prevent misuse, and improve reliability.

We do not sell personal information or use it for cross-context behavioural advertising.

## 4. When information is sent to third parties

Hana uses the following providers only when the relevant feature needs them:

| Provider | Purpose | Information involved |
| --- | --- | --- |
| [Discord](https://discord.com/privacy) | Platform, messages, commands, direct messages, and voice connection | Information you send or make available through Discord and the metadata needed by Discord to deliver it |
| [Google Gemini](https://policies.google.com/privacy) | RoomAI response generation, conversation-memory summaries, and optional drawing-game prompt generation | Relevant RoomAI message/context, Hana context, applicable memory, and character/status context needed for the response or summary; drawing prompts use Hana’s theme/status context only |
| [Google Translate TTS](https://policies.google.com/privacy) | Speech synthesis for `/tts` | The text selected for speech and language setting |
| [Open-Meteo](https://open-meteo.com/en/terms) | Public Sapporo weather used by Hana's life/status context | Fixed Sapporo forecast parameters; no Discord user content or device location |
| [Nager.Date](https://github.com/nager/Nager.Date) | Japan public-holiday dates used by Hana's global schedule | Fixed year and country code `JP` only; no Discord user, message, server, or location data |
| [Nekos.best](https://nekos.best/) | Anime GIFs for `/act` and `/actwith` | Requested action category only; no conversation message content |
| [Pexels](https://www.pexels.com/api/documentation/) | Fresh travel-scene image for a verified Hana travel-status question in RoomAI or `/travelphoto <Japan prefecture>` | A fixed status-matched Japan query or curated Japan landmark query only; no Discord user content, identity, or device location |

If you enable cross-server sharing, Hana may include eligible memory from up to three of your other servers in the prompt for your current server. This happens only while sharing is enabled and only for your own records; Hana does not provide other members' memory to Gemini.

## 5. Your choices and controls

`/settingai` is an ephemeral panel: only the person opening it can see and change it. It lets you, where available:

- Turn local memory on or off for the current server.
- Turn cross-server memory sharing on or off.
- View, move, or delete your local memory, all of your memory, and legacy memory. Moving memory requires a second confirmation and moves the matching relationship record with it.
- View or edit your optional personal profile and settings.
- Choose whether Hana mentions you in replies, allows proactive greetings, and uses your selected time zone.

You can also remove a message in Discord, remove Hana from a server, or ask the team through the official support server for help with information not covered by an in-bot control. Server administrators can disable RoomAI for a room and manage server context they created.

Deleting local memory also deletes the matching local relationship record. Deleting all memory deletes all of that user's relationship records and legacy archive. Some operational records may remain briefly in backups or logs while they age out.

## 6. Retention

Hana keeps information only as long as needed for the active feature or until it is removed through the available controls, except where a short operational retention period is needed. Examples: RoomAI reply links expire after seven days, named RoomAI relay records are deleted after delivery or expire after seven days, and AI usage records are pruned after 14 days. Hana does not retain an action-GIF cache or anonymous `/dm` cooldown records.

Memory, settings, relationship records, RoomAI configuration, and administrator-provided context may remain until the relevant user, administrator, or Hana team deletes them. Legacy memory is archived and not used by AI until its owner explicitly restores or moves it.

## 7. Security

We use scoped storage, permission checks, ephemeral settings panels, and feature-specific limits to reduce unnecessary access. No system can guarantee absolute security. Keep Discord account security enabled and avoid submitting sensitive information to any bot or AI service.

## 8. Children

Hana is not directed to people below the minimum age permitted to use Discord in their country. If you believe a child has provided personal information to Hana improperly, contact us so we can review the request.

## 9. Changes and contact

We may update this Policy as Hana changes. The latest version and date will be published in this repository.

For privacy requests, questions, or reports, contact the Hana team through the official Discord server: <https://discord.gg/qWbQEABAPA>.
