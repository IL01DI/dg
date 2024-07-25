---
tags:
  - en
---

> [!check] Tested devices
> - Windows 11
> - Linux Fedora 40
> - iOS

>[!missing] Untested devices
> - macOS 
> - Android

> [!attention] Requisites
> Services you need to register:
> - Github
>
> On Windows, make sure to have installed:
> - [Obsidian](https://obsidian.md/download)
> - [Github Desktop](https://github.com/apps/desktop)
>
> On Linux, instead of using [Obsidian](https://obsidian.md/download), just use:
> - [VSCodium](https://vscodium.com/) or [VSCode](https://code.visualstudio.com/)
>
> While on iOS, you should have:
> - [Obsidian](https://obsidian.md/download)
> - [Git](https://obsidian.md/plugins?id=obsidian-git)

> [!hint] Advice
> There are many ways to sync, but here you can follow the one I provide, so it may work for you.
> Even if there are untested devices, you can also proceed the steps similarly, unless you don't know what you are doing.
> I assume you that you don't have vaults neither on Linux and iOS, only Windows.
>
> Tips:
> - Avoid creating your vault in iOS first.
> - To setup, it is recommended using Windows.

# Windows

1. Open your web browser and go to your repo, or create a new one if you haven't.
2. Click the green button "Code" and open Github Desktop.

## 1.1. Current vault
If you currently have a vault, you can import it to the git folder. To do so:
1. Choose the desired location (not the vault's location).
2. Now, move your vault folder to the git folder you have created.
3. Open Obsidian to check if your files are OK.

## 1.2. New vault
If you don't ahve any vaults, you need one. To do so:
1. Choose the desired location.
2. Open Obsidian and create a new vault from the chosen location.
3. Configure your settings and install the plugins you want.

## 2. Opt-out file sync 
> [!hint] Recommended
> It is adviced to not sync plugins in Github as it will expose your PAT to the public, which will be used on iOS.

1. If you don't want to sync the settings or plugins between devices, create a new file named `.gitignore` using File Explorer.
2. Open the created file using Notepad or any text editor and add the first line as `.obsidian/plugins` if you don't want to sync plugins; otherwise you may prefer it as `.obsidian`,so it will only sync your Markdown files of your vault.

## 3. Upload files to Github

1. In your Github Desktop, you should see the changes. If so, name the message in the source control and commit it.
2. Congrats! Now, whether the order, it is up to you if it will be Linux or iOS.

# Linux

1. Open VSCodium and go to Source Control.
2. Clone the repo you have created.
3. Optionally, install Obsidian (if you don't like writting on VSCodium).
4. Every change on the files will appear in VSCodium, and so it is used for sending and receiving to Github repo.

# iOS

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
