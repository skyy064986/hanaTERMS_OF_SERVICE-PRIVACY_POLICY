# Hana Bot Privacy Policy

**Last updated:** 15 September 2026

This Privacy Policy explains how Hana ("Hana", "the Bot", "we", "us") processes information when used on Discord. It applies to RoomAI, optional memory, text-to-speech, roleplay, status updates, and mini-games.

## 1. Information Hana processes

Hana processes information needed to provide its features:

- **Discord identifiers and context:** Discord user ID, display name/username, server ID, channel ID, and interaction data needed to respond to commands.
- **RoomAI messages:** message content and sender display name only in a channel where an administrator enabled RoomAI.
- **Conversation context and memory:** recent conversation context for the current speaker; optional summary, relationship profile, and pinned preferences/facts for that speaker. Memory is separated by Discord user ID and server ID by default.
- **Settings and usage data:** optional reply-mention preference, an optional user-selected timezone, privacy choices, and daily AI request counters. Counters contain an identifier, JST date, and count.
- **Voluntary personal profile:** a user may optionally enter a nickname/pseudonym, age, important dates, or basic context through `/settingai`. Hana does not infer age, identity, address, or private facts from an avatar, name, language, or Discord profile.
- **Mini-game and voice input:** temporary mini-game state and text used for optional text-to-speech in an active Bot voice/stage channel.

## 2. Information you should not submit

Do not submit your address, phone number, email address, password, Discord token, API token, banking or payment details, identity documents, precise location, health information, or similar sensitive information. Use a nickname or pseudonym and basic non-sensitive context only.

## 3. How information is used and shared

We use information to answer messages and commands, maintain optional conversation continuity, generate AI responses and spoken audio, run mini-games, enforce limits, troubleshoot errors, and maintain the Bot. We do not sell personal information, run targeted advertising, or use Discord API data to profile users or their relationships.

Information is shared only as needed for the selected feature:

- **Discord** transmits messages and interactions through its platform.
- **Google Gemini** may receive the applicable message, current-speaker context, and only relevant memory/settings enabled by that speaker to generate a response or memory summary.
- **Google text-to-speech services** may receive text submitted for optional audio generation.

These providers process information under their own terms and privacy practices.

## 4. Memory boundaries and retention

- Personal memory is isolated by Discord user ID and server ID. Hana does not use one member's private memory to answer another member.
- Cross-server memory is off by default. If its owner explicitly enables it in `/settingai`, Hana may read only that same user's sanitized summaries from other servers where memory remains enabled; records are not merged.
- Legacy memory whose original server is unknown is archived and not used in AI prompts unless its owner restores it.
- Room context, mini-game sessions, relays, quotas, and other runtime records are retained only as reasonably needed to operate the feature, resolve issues, or until deleted where controls are available.

## 5. Your controls

`/settingai` is visible only to the caller. It lets users control local memory, cross-server sharing, reply mentions, timezone, voluntary personal profile, and deletion of memory/profile data. Deletion actions require confirmation. A server administrator can disable RoomAI or remove Hana from a server.

## 6. Security and changes

We use reasonable administrative and technical measures intended to protect stored runtime data. No online system is completely secure; do not submit sensitive information to Hana.

We may revise this policy when features or requirements change. The current version shows its update date at the top.

## 7. Contact

For privacy questions, Premium, support, or a data request, contact Hana through the official Discord community:

https://discord.gg/qWbQEABAPA
