# Panda Client

Panda Client is an independent Windows launcher and client project for Minecraft Java Edition, currently in development. It is not an official Minecraft product and is not affiliated with Mojang or Microsoft.

## Current functionality

- Separate Vanilla and Fabric profiles, with a release catalogue starting at Minecraft Java 1.21.
- Modrinth search, compatible mod installation, and Modrinth modpack imports.
- Direct game launch using a user's authenticated Microsoft/Xbox/Minecraft session.
- An included Panda Fabric mod for Minecraft 1.21.11, with custom in-game menus, two additional pause-menu entries, configurable HUD elements, and a HUD position editor.
- Launcher background themes and color palettes.

The current launcher version is 0.2.2. The native Panda mod currently targets Minecraft 1.21.11; the presence of a newer Minecraft release in the normal launcher catalogue does not imply Panda mod support for that version.

## Microsoft and Minecraft authentication

Panda uses its own public Microsoft application ID and the OAuth device-code flow. Users sign in with their own Microsoft accounts on Microsoft's website. Panda does not ask users to enter their Microsoft passwords into the launcher. It checks Minecraft Java entitlements and retrieves the Minecraft profile before launching an authenticated game session.

Authentication and refresh tokens are handled in the Electron main process. Persistent sessions use operating-system-backed encryption when available. If suitable encryption is unavailable, the session is kept in memory. Diagnostic logs record service names, endpoints and error codes, not tokens or device login codes.

Microsoft and Xbox authentication have succeeded in a local test. The Minecraft Services authentication request currently returns HTTP 403. Approval of the project's application ID for Minecraft Services has not been confirmed. The launcher is not represented as approved or fully operational for public sign-in.

## Development roadmap and limitations

The requested feature catalogue includes HUD, gameplay, visual, world, chat, social and cosmetic features. Additional gameplay automation and cheat-style modules are planned, including combat and movement features. Their inclusion in the catalogue is not an implementation or compatibility claim. Unimplemented entries are marked unavailable in the current client.

Friend, party and voice-chat functionality is not yet implemented. No anti-cheat bypass is implemented or guaranteed. Server-crashing and targeted server-disruption features are excluded from the project.

The project remains a prototype. A successful local build or automated test does not establish that every requested feature works, or that an authenticated production game session has been verified.
