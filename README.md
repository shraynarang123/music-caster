<h1 align="left">
<img width=30px src="https://raw.githubusercontent.com/elibroftw/music-caster/master/resources/Music%20Caster%20Icon.png" alt="Logo" style="vertical-align: bottom">
Music Caster</h1>

[![GitHub Releases](https://img.shields.io/github/downloads/elibroftw/music-caster/latest/total?color=blue&label=github%20downloads%40latest&style=for-the-badge)](https://github.com/elibroftw/music-caster/releases/latest)
[![Source Forge](https://img.shields.io/sourceforge/dt/music-caster?color=orange&label=SourceForge%20downloads&style=for-the-badge)](https://sourceforge.net/projects/music-caster/)

Music Caster is a music player which lets you cast your local music files to a Google Cast Device (Chromecast, Home, etc.)

## [Download Here (Windows 64-bit)](https://github.com/elibroftw/music-caster/releases/latest)

Click the image below for a video demo.

[![demo link](https://i3.ytimg.com/vi/y0fWPyhNSB0/maxresdefault.jpg)](https://www.youtube.com/watch?v=y0fWPyhNSB0)

## [Screenshots (v4.25.0)](http://www.elopez.me/music-caster/)

## Usage
### TLDR
When running the app for the first time, if you have music files in different folders, right click the tray icon and open settings.

On the first startup, the app will be in your hidden tray. You can move it onto the "Taskbar" and it'll stay there on future launches.
Right click the icon and then click Settings.
Add or remove music dirs. The home music directory is there by default.

When you click Play All, all the music from these directories are shuffled and played.

When you click Play File, you can select a file to play and then the music in your directories are shuffled into the music queue.

Music Caster supports media keys.

## Limitations and Known Issues
- Only supports MP3 files (for now)
- Scrolling over the volume bar or progress meter does not work yet

## Data Collection
- Errors are automatically sent to me
```JS
// As seen near the bottom of music_caster.py
'TIME': current_time,
'VERSION': VERSION,          // of Music Caster
'OS': platform.platform(),
'TRACEBACK': trace_back_msg  // error output
'MAC': MAC                   // unqiueness of error
'TRACEBACK': trace_back_msg  // error output
```
- On every startup, MAC, VERSION, and TIME is sent to me so I know how many users I have
- Only I have access to this data

## Keyboard Shortcuts
There exists keyboard shortcuts, but I will put them here later

## Settings.json Guide
- Music Caster will detect changes within 10 seconds of editing `settings.json`
  - Caveat: any color code changes requires a restart
- The music directories is a list of valid directory paths
  - The first path is the default directory MC opens when you want to play a file
- The playlist variable follows the convention `{'PLAYLIST NAME': ['paths to files']}`
- If MC stops working after changing the file, try using an IDE to detect syntax errors in `settings.json`

## Build Instructions
1. Have Python 3.6.x installed
2. Have Visual Studio 2019 Installed
3. `pip install -r requirements.txt`
4. Make sure Python scripts folder is on PATH
5. Have Inno Setup installed and `C:\Program Files (x86)\Inno Setup 6\` on PATH 
6. run `build` or `build.py`

## Credits
- default.png made by [ivke32](https://pixabay.com/users/ivke32-2526695/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1413583) from [Pixabay](https://pixabay.com/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1413583)
- speaker icon in main window made by [Naomi Atkinson](https://thenounproject.com/naomiatkinson/) from [The Noun Project](https://thenounproject.com/term/speaker/5609/) and modified by me
- repeat icon in main window made by [Brandy Bora](https://thenounproject.com/brandy.bora) from [The Noun Project](https://thenounproject.com/search/?q=repeat&i=1555394) and modified by me
- Folder icon in main window by [Landan Lloyd](https://thenounproject.com/landan/) from [The Noun Project](https://thenounproject.com/term/folder/1352565/)
