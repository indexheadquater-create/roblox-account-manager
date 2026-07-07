# Roblox Account Manager

A desktop app for Windows that lets you keep all your Roblox accounts in one place and jump into games on any of them without logging in and out every time.

Built with Tauri, so the app stays small and light instead of shipping a whole browser with it.

## What it does

- Add accounts either by logging in through a real Roblox login window, or by pasting a `.ROBLOSECURITY` cookie directly.
- Launch any account straight into Roblox with one click.
- Set one private server link and send any account into it (works with both the old `?privateServerLinkCode=` links and the newer `share?code=` links).
- Open an account in a browser window to check its inventory, trades, groups, and so on.
- Copy an account's cookie to the clipboard when you need it.
- Organize accounts into groups. You can create, rename, reorder, and delete groups.
- Drag accounts to reorder them, search by name, and select several at once for bulk launch or removal.
- Auto-updates itself when a new version is released.

## Where your data lives

Everything stays on your machine. Nothing is sent anywhere except to Roblox itself.

- Accounts are saved to `%APPDATA%\com.speediboipc.robloxaccountmanager\accounts.dat`.
- That file is encrypted with AES-256-GCM. The cookies are never stored in plain text.
- The encryption key is kept in the Windows Credential Manager, separate from the data file, so copying `accounts.dat` on its own does not get anyone your accounts.
- Settings (private server link, groups) live next to it in `settings.json`.

## A note on safety

Your `.ROBLOSECURITY` cookie is basically your account. Do not share it, do not paste it into random sites, and be careful who you send an exported cookie to. This app keeps them encrypted for that exact reason.
