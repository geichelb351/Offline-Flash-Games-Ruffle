# Steve's Offline Flash Games
Offline Flash Games that can work offline and never be blocked, for use during those boring times at school or work but also useful for times where there is no internet.
View the [Online Demo](htpp://stevesflashgames.orgfree.com).
NOTE: ALL IINFORMATION BELOW IS THE OG INFORMATION, I HAVENT TESTED ANY OF IT YET. HOWEVER, RUFFLE NEEDS TO BE ONLINE TO WORK< SO YOU NEED TO SELF HOST OR USE MY LINK ABOVE.
## Games
 - 2048 (no support yet)
 - Chess 3 (no support yet)
 - Doom
 - Duck Life 1, 2, 3 & 4 (no support yet)
 - Earn to Die 1, 2, 2012 & 2012 Part 2 (no support yet)
 - Minicraft (no support yet)
 - Nyan Cat - Lost in Space (no support yet)
 - PAC-MAN (no support yet)
 - Run 1, 2 & 3 (Run 3 is VERY laggy on ruffle, working on a fix.)
 - Tetris (no support yet)
 - Fireboy and Watergirl in The Crystal Temple, Forest Temple, Ice Temple & Light Temple (These haven't been tested properly yet + no support)

## Download (DONT DO)
View the [releases here](https://github.com/Steve-Tech/Offline-Flash-Games/releases).
There is no Mac version because I don't have a Mac so I can't test or get the files needed to compile, you will have to run the HTML version or compile Electron for yourself, feel free to fork this and make a Mac version.
## Compiling (DONT DO)
1. Install Node.js, electron and electron-packager
 - [Download Node.js here](https://nodejs.org/en/)
 - Open command prompt in the directory of the repository and run `npm install electron --save-dev`
 - In the same command prompt run `npm install electron-packager --save-dev`
2. You will need to find the Pepper Flash Player files
 - Windows 64 bit: `C:\Windows\System32\Macromed\Flash\pepflashplayer64_<version>.dll`
 - Windows 32 bit: `C:\Windows\SysWOW64\Macromed\Flash\pepflashplayer32_<version>.dll`
 - Mac: `/Library/Internet Plug-Ins/Flash Player.plugin`
3. Put them in the `flash/player` directory

4. In the command prompt from earlier, run ```electron-packager . offline-flash-games --overwrite --platform=win32 --arch=ia32 --prune=true --out=release-builds --version-string.FileDescription="Steve's Offline Collection of Flash Player Games" --version-string.ProductName="Steve's Offline Flash Games"```
    
Notes:
 - ASAR does not work with Flash
 - You may want to go into `main.js` to find `'\\flash\\pepflashplayer32.dll'` and change the 32 to 64 if using different versions of electron
