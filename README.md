# saUCEy-Syncs
A simple tool for managing UCE libraries and their respective cox files for AtGames Legends devices and CoinopsX

SaUCEy Syncs is a tool I crated to make it easier to manage UCE libraries of console and computer games for use alongside the main CoinopsX Arcade releases. CoinopsX is a special (unofficial) build of the Coinops frontend made to run on the AtGames Legends family devices, and most specific to the controls on their Legends Ultimate Arcade cabinet. UCE files are a special compressed file format used for packaging ROM files, a RetroArch emulator core, as well some additional graphics and other information.

The tool is an HTA (HTML Application), written in VBScript and, of course, HTML. I don't expect that it works on anything outside of the Windows ecosystem, but within Windows this makes it very portable as no special libraries are required. It's just one file, and if you want to know what it's doing viewing the code is as simple as opening it in a text editor.  I have also attempted to comment everything well enough to make it clear what is happening even if you don't understand the code. 

The GUI uses a straightforward Source & Destination layout. I highly recommend creating separate UCE file folders for each system (i.e. SNES, C64, etc.) in parallel to your cox folder (same place as the Arcade folder). Set one of these folders as the destination and another folder containing an extracted collection of UCE files (also in proper parallel relation to its extracted cox files folder) as the source. You can obtain some of these CoinopsX UCE collections from Archive.org, but several of them have updated UCE directories within their compressed archives, which fix save and button mapping issues but also lack the associated cox files, so look, read, and be sure you've extracted everything to the proper location. I also recommend maintaining all of your own system UCE folders and their shared cox folder separate from the CoinopsX arcade build, and just copying them on top of the arcade build when you put together your flash drive.  This will make it easier to add your own system libraries to new CoinopsX arcade builds when they are released and also allow this tool to run faster because it won't have to parse through all of the arcade cox files in addition to those specific to your own system libraries.  

Using the arrow button will transfer selected UCE files as well as their identically named cox file counterparts into the destination folder and its adjacent cox folder, creating new file folders there as needed.

With the desired files in the destination folder, you have several options, including:

-Rename: This will rename the selected destination UCE file and all of its identically named cox files. The CoinopsX All Games list is organized alphabetically, so you can use this function to make sure games from the same franchise, but with disparate names, appear together or in the order you prefer.  CoinopsX will only display the logo, and not the name changed here, so you can pretty much name things whatever you want to get the desired effect.

-Delete: This will delete the selected destination UCE file and all of its identically named cox files.

-Playlist: This will create a new playlist based on the destination UCE file list. The tool will prompt you to enter a playlist name, but the default will be the name of the destination UCE folder.

-Pull COX files from source: This function can be used in the event that you have a destination folder of UCE files, but have not copied any/all of the applicable cox files to the cox folder adjacent to your specified destination folder. Select a source folder in parallel to the cox folder where applicable cox files can be found. The tool will parse through the source adjacent cox sub-folders for any files identically named to the UCE files in the destination folder, and if found, it will copy those files into the applicable destination adjacent cox folder, saving you the time and effort of trying to locate and move them individually.

Hopefully all of the other functions are straightforward enough to not require explanation.

Known Issues:

-If you attempt to scroll one of the list boxes while the tool is working it may force close with no error message. I'm not sure what causes this, but I've encountered it a few times so I just leave the window alone while it's doing its thing.  

-Sometimes files in the destination list box are not displayed alphabetically even after re-defining the destination folder. This is inconsistent and my best guess is that it has something to do with the file system being used. Since the list box order is used to write playlists it could mean your playlist is also not written alphabetically. The tool can be updated to make sure playlists are created in alphabetical order, but for the time being you my may have to manually reorder your playlist if you encounter this issue.  
