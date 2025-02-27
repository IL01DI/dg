---
tags: en
dg-publish: true
published: true
---

> [!warning]
> Do not run more than one syncing tool at the same time. Remember to always back up first before trying out.

# Overview

|                                  Plugin Name                                  | Rating | E2EE |            Version history            | Cross-platform | Number of synced platforms  | Offline First | Vault settings | Selective sync |
|:-----------------------------------------------------------------------------:|:------:|:----:|:-------------------------------------:| -------------- | --------------------------- | ------------- | -------------- | -------------- |
|       [Remotely Save](obsidian://show-plugin?id=remotely-save) [^1] ⭐        | 3.5/5  |  ✅  | Not implemented, but cloud integrated | ✅             | ♾️                          | ✅            | ✅             | ❌             |
|     [Self-Hosted Live Sync](obsidian://show-plugin?id=obsidian-livesync)      | 3.5/5  |  ✅  |            Not implemented            | ✅             | ♾️                          | ✅            | ✅             | ❌             |
|          [Obsidian Git](obsidian://show-plugin?id=obsidian-git) [^2]          | 3.5/5  |  ❌  | Not implemented, but cloud integrated | ✅             | ♾️                          | ✅            | ✅             | `.gitignore`   |
|                     Obsidian Google Drive Auto Sync [^3]                      | 2.5/5  |  ❌  | Not implemented, but cloud integrated | ✅             | ♾️                          | ✅            | ❌             | ✅             |
|                   [Fit](obsidian://show-plugin?id=fit) [^4]                   | 2.5/5  |  ❌  | Not implemented, but cloud integrated | ✅             | ♾️                          | ✅            | ❌             | `.gitignore`   |
| [Fleeting Notes Sync](obsidian://show-plugin?id=fleeting-notes-obsidian) [^5] |  2/5   |  ✅  |                  ❌                   | ✅             | 1 in Fleeting Notes; but ♾️ | ✅            | ❌             | ✅             |

[^1]: Freemium: limited features may affect your usage. May add unexpected folders, unless encryption is enabled. Chromebook is not supported due to the auth link.
[^2]: Async.
[^3]: Slow sync, may lose data, and cannot sync over 1000 files.
[^4]: Not very good at auto merge conflict. Every run by an interval sync notifies you of an error, although it works.
[^5]: Extremely fast sync between Obsidian and Fleeting Notes.
# Obsidian Git

> [!check] Tested Platforms
> - Windows 11
> - Linux Fedora 40
> - iOS
> - Chrome OS

>[!missing] Untested Platforms
> - macOS 

> [!attention] Requisites
> Services you need to have registered:
> - [GitHub](https://github.com)
>
> On Windows, make sure to have installed:
> - [Obsidian](https://obsidian.md/download)
> - [GitHub Desktop](https://github.com/apps/desktop)
>
> On Linux, instead of using [Obsidian](https://obsidian.md/download), just use:
> - [VSCodium](https://vscodium.com/) or [VSCode](https://code.visualstudio.com/)
>
> While on iOS, you should have:
> - [Obsidian](https://obsidian.md/download)
> - [Git](https://obsidian.md/plugins?id=obsidian-git)

> [!hint] Advice
> There are many ways to sync, but you can follow here the one I provide, so it may work for you.
> Even if there are untested devices, you can also proceed these steps similarly, unless you don't know what you are doing.
> I assume you that you don't have vaults neither on Linux nor on iOS, only Windows.
>
> Tips:
> - Avoid creating your vault in iOS first.
> - To set up, it is recommended using Windows.

## Windows

1. Open your web browser and go to your repo, or create a new one if you haven't.
2. Click the green button “Code” and open GitHub Desktop.

### 1.1. Current vault
If you currently have a vault, you can import it to the git folder. To do so:
1. Choose the desired location (not the vault's location).
2. Now, move your vault folder to the git folder you have created.
3. Open Obsidian to check if your files are OK.

### 1.2. New vault
If you don't have any vaults, you need one. To do so:
1. Choose the desired location.
2. Open Obsidian and create a new vault from the chosen location.
3. Configure your settings and install the plugins you want.

### 2. Opt-out file sync 
> [!hint] Recommended
> It is advised to not sync plugins in GitHub as it will expose your PAT to the public, which will be used on iOS.

1. If you don't want to sync the settings or plugins between devices, create a new file named `.gitignore` using File Explorer.
2. Open the created file using Notepad or any text editor and add the first line as `.obsidian/plugins` if you don't want to sync plugins; otherwise you may prefer it as `.obsidian', so it will only sync your Markdown files of your vault.

### 3. Upload files to GitHub

1. In your GitHub Desktop, you should see the changes. If so, name the message in the source control and commit it.
2. Congrats! Now, whether the order, it is up to you if it will be Linux or iOS.

## Linux

1. Open VSCodium and go to Source Control.
2. Clone the repo you have created.
3. Optionally, install Obsidian (if you don't like writing on VSCodium).
4. Every change on the files will appear in VSCodium, and so it is used for sending and receiving to GitHub repo.

## iOS & Android

1. The repo must be public in order to work.
2. Open Obsidian and open the new vault.
3. Go to the Git Settings and fill the `Username Git` and `PAT`.
4. Then, use Command Palette and search `Clone a remote repository`.
5. Enter the URL of your repo. The format must be the same as the following example: `https:github.com/username/repo.git`
6. Select your choice:
	  - If you don't have the `.obsidian` folder on Git, enter `NO`.
	  - If you do have the `.obsidian` folder on Git:
	    - And you want to also sync with the Desktop config, enter `YES`.
	    - Otherwise, enter `NO`.
7. After cloning files from the repo, close the app and reopen it.
8. Redownload the plugin, as it is no longer available.
9. Add author's commit and email commit.

# Obsidian Google Drive Auto Sync Plugin

> [!warning] Requisites
> Assuming you already have:
> - An Obsidian vault on a PC.
> - A Google Drive.
> - An empty vault on mobile.

Warning: Max sync number is 1000 files.
## Installation
To install the Obsidian Google Drive Auto Sync Plugin, follow these steps (if you have previously installed any unofficial plugin the steps are identical):
1. On your PC, go to [Obsidian Google Drive Sync Plugin GitHub Repo](https://github.com/stravo1/obsidian-gdrive-sync?tab=readme-ov-file#obsidian-google-drive-sync-plugin) and download from the latest release the `obsidian-gdrive-sync.zip`.
2. Unzip it, then you should have a folder named `obsidian-gdrive-sync` containing 3 files. If after unzipping you end up with 3 different files (main.js, styles.css, manifest.json), place them under a new folder called `obsidian-gdrive-sync`.
3. Navigate to your vault's location.
4. Open the .obsidian folder (Turn on `Show Hidden Files and Folders` in your file manager if this folder is not visible).
5. Go to plugins (You might have to create this folder if you never installed any plugin before). Paste the folder containing 3 files.
6. The path to the plugin should look like this: `/$PATH_TO_VAULT/.obsidian/plugins/obsidian-gdrive-sync`
7. Open the required vault in Obsidian.
8. Enable Community Plugins under Settings (If you are opening the vault for the first time you might be asked to confirm to "Trust Author and Enable Plugin", click to enable it).
9. Enable the Google Drive Sync plugin under Installed Plugins. Wait for a few seconds. Make sure to have a good internet connection.
10. Click on the Google Drive Sync settings under Community Plugins section that becomes visible.

## PC Configuration
Configuring the plugin is straightforward:

1. Under the plugin settings you will be provided with a link to Login.
2. Clicking the link will open a new browser window.
3. Choose the Google account whose Drive space will be used.
4. Provide access to all the permissions (`See, edit, create, and delete only the specific Google Drive files you use with this app`).
5. You will be provided with a code/token (`Refresh Token`).
6. Copy the code and paste it in the space provided (Set Refresh Token) under the plugin settings and click on Checkmark button.
7. As prompted, reload the plugin by turing it on and off under Communtiy Plugins.
8. If you are using this plugin for the first time with a vault, you will be prompted to **Initialize vault**. This creates a folder with the same name as your vault in your Google Drive and copies all the files into it. You might need to reload the plugin again once initialization is complete. 
9. Once the previous steps are complete, set your preferred synchronization interval.
## iOS Configuration
1. With your Obsidian vault set up on your desktop, navigate to its parent folder in your file explorer (Finder if on Mac, File Explorer for Windows).
2. Compress the entire vault folder (containing the `.obsidian` folder and all the `.md` files) in the explorer by right-clicking the folder and choosing the appropriate option.
3. Check if `.obsidian` is in the folder zip. If for some reason doesn't include it, then copy manually and paste it inside.
4. On your iOS device, create a vault with the same name (if your vault is called "vaulty", compressing it should make a "vaulty.zip", so make a vault called "vaulty" on your iOS device). Make sure to uncheck the "Store in iCloud" option.
5. To confirm it's all good so far, check the Obsidian folder in the "On your iPad/iPhone" folder in Files. It should pretty much be empty except for the vault we just made.
6. Get the compressed file from your desktop to mobile.
7. Move the .zip to this Obsidian data folder, beside the empty vault we just made.
8. Delete the (empty) vault folder, and unzip the zip we have by tapping and holding on it and selecting “Extract”.
9. Now we should have effectively the “same” vault as before, except now it's populated with files.
10. Close Obsidian from the app switcher and reopen it.
11. Hopefully your files should sync after a bit once the extension loads.

## Chromebook Configuration
1. Make sure Android and Obsidian is installed.
2. Get the vault folder to your Chromebook device.
3. Unzip the zip we have by moving the folder to Android.
4. `Open folder as vault` in Obsidian and instead of going on your root folder, go to `My files`, and then `Android`.
5. You should see the name of your vault folder.
6. Enable Community Plugins (If you are opening the vault for the first time you might be asked to confirm to "Trust Author and Enable Plugin", click to enable it).
