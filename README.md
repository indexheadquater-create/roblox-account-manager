# Roblox Account Manager

A desktop app for Windows that lets you keep all your Roblox accounts in one place and jump into games on any of them without logging in and out every time.

Built with Tauri, so the app stays small and light instead of shipping a whole browser with it.

## What it does

* Add accounts either by logging in through a real Roblox login window, or by pasting a `.ROBLOSECURITY` cookie directly.
* Launch any account straight into Roblox with one click.
* Set one private server link and send any account into it (works with both the old `?privateServerLinkCode=` links and the newer `share?code=` links).
* Open an account in a browser window to check its inventory, trades, groups, and so on.
* Copy an account's cookie to the clipboard when you need it.
* Organize accounts into groups. You can create, rename, reorder, and delete groups.
* Drag accounts to reorder them, search by name, and select several at once for bulk launch or removal.
* Auto-updates itself when a new version is released.

## How to use

* Add an account from the **Add Account** button.

<img width="1684" height="72" alt="image" src="https://github.com/user-attachments/assets/ca054f74-fd11-46f5-9cd1-d4bf4157b5e7" />

* Click the 1st (**Browser**) button to open the account in your web browser.
* Click the 2nd (**Join PS**) button to join your configured private server. Make sure you've set a private server link first.
* Click the 3rd (**Launch**) button to start Roblox using the selected account.

## Why does SmartScreen flag it?

If Windows shows a **"Windows protected your PC"** message when you open the installer, it does **not** automatically mean the application is unsafe.

Microsoft SmartScreen uses a reputation-based system to help protect users from potentially harmful software. Since this project is relatively new and the installer is not digitally signed, Windows may not have enough information to automatically trust it yet.

This usually happens because:

* The installer is not digitally signed. Code signing certificates are expensive and are often out of reach for independent developers and hobby projects.
* The application is new and has not yet built enough reputation with Microsoft SmartScreen.

The installer does **not** contain malware, spyware, or unwanted software. If you'd like to verify it yourself, feel free to scan it with your preferred antivirus or upload it to VirusTotal before running it.

If you downloaded the installer from the official GitHub release page and trust the source, you can continue by clicking **More info** and then **Run anyway**.

[VirusTotal Link](https://www.virustotal.com/gui/file/159436b47cc04c67804de68e5aba99d685fa7fcb167255b1e5ba4f41a9013ba2?nocache=1)
3/67 (3 because it is a installer and they are false)

## Where your data lives

Everything stays on your machine. Nothing is sent anywhere except to Roblox itself.

* Accounts are saved to `%APPDATA%\com.speediboipc.robloxaccountmanager\accounts.dat`.
* That file is encrypted with AES-256-GCM. The cookies are never stored in plain text.
* The encryption key is kept in the Windows Credential Manager, separate from the data file, so copying `accounts.dat` on its own does not get anyone your accounts.
* Settings (private server link, groups) live next to it in `settings.json`.

## A note on safety

Your `.ROBLOSECURITY` cookie is basically your account. Do not share it, do not paste it into random sites, and be careful who you send an exported cookie to. This app keeps them encrypted for that exact reason.

## Screenshots

<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/77d3b723-a0aa-40ff-b581-218dd20039c3" />
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/87674456-9a88-46a0-b4ac-c4dad0563dfb" />
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/430a7127-8fd1-4a6a-b24f-2e5907091a3b" />
