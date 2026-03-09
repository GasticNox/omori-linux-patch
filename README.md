# omori-linux-patch

A patch to make the OMORI RPG Maker MV Project (mostly) work on Linux.

### Disclaimer

This repository is a fork of [surrealegg/omori-linux-patch](https://github.com/surrealegg/omori-linux-patch).
It includes a small fix to improve compatibility with certain plugins and mods.

# Instructions

Ensure that you have OMORI and RPG Maker MV installed.

## 1. Install OneLoader

To create an RPG Maker MV project, you first need to install OneLoader, which is a mod loader for OMORI. You can follow the instructions provided here: [OneLoader Installation Guide](https://omori.wiki.mods.one/installing_oneloader).

## 2. Decrypt OMORI

1. Launch OMORI and navigate to Options > Mods > Decrypt.
2. Confirm that the "Generate RPG Maker project?" option is set to "YES."
3. Click the "CLICK HERE TO START" button to initiate the decryption process (this may take some time).

![Decrypt](https://i.imgur.com/CcIkxnI.png)

Upon completion, you should see a new folder created, which will look like this:

![New Folder](https://i.imgur.com/fNg9DZJ.png)

## 3. Add the Surrealegg_LinuxPatch.js Plugin to the Project

Download the [Surrealegg_LinuxPatch.js](https://github.com/gasticnox/omori-linux-patch/blob/main/Surrealegg_LinuxPatch.js) plugin and save it in the following directory:
`www_playtest_[random_id]/js/plugins`

Now, open RPG Maker MV and access your project. Typically, it can be found here, but the location may vary depending on your distribution:
`~/.local/share/Steam/steamapps/common/OMORI/www_playtest_[random_id]/Game.rpgproject`

Navigate to `Tools` > `Plugin Manager...`, scroll to the bottom, and double-click an empty space. This will open a new window. Select "Surrealegg_LinuxPatch" and click "Ok."

![Plugin](https://i.imgur.com/ySNg81T.png)

Next, move the plugin to the top to ensure it runs first. It should look something like this:

![Plugin Manager](https://i.imgur.com/q3nbxtq.png)

## 4. Run the Game

After saving your changes, you can run the game by pressing `Ctrl` + `R` or by selecting `Game` > `Playtest` from the menu.

Happy Modding!

![Result](https://i.imgur.com/hqmNpxg.png)

# Notes

### If playtesting doesn't work/doesn't show up
Try updating RPG Maker MV's copy of **NW.js** to a newer version.

The one currently bundled with the program is old and often has issues running on modern Linux kernels.

### Before bundling your mod...

I would recommend disabling the plugin and removing this patch **before compiling and bundling your mod**.

It shouldn't break on its own, but it could cause unexpected issues if certain mods are mixed. Also it's highly unnecessary if running the game natively on Windows or through Proton.