---
lastSync: Fri Jul 26 2024 22:23:06 GMT+0200 (Central European Summer Time)
tags: en
dg-publish: true
---

> [!warning] Requisites
> Assuming you already have:
> - An Obsidian vault on a PC.
> - A Google Drive.
> - An empty vault on mobile.

Warning: Max sync number is 1000 files.
# Installation
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

# PC Configuration
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
# iOS Configuration
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

# Chromebook Configuration
1. Make sure Android and Obsidian is installed.
2. Get the vault folder to your Chromebook device.
3. Unzip the zip we have by moving the folder to Android.
4. `Open folder as vault` in Obsidian and instead of going on your root folder, go to `My files`, and then `Android`.
5. You should see the name of your vault folder.
6. Enable Community Plugins (If you are opening the vault for the first time you might be asked to confirm to "Trust Author and Enable Plugin", click to enable it).---
lastSync: Fri Jul 26 2024 22:22:19 GMT+0200 (Central European Summer Time)
---
