chromecastize
=============
Simple bash script to convert video files into Google Chromecast supported format.

Script identifies video and audio format of given file (using `mediainfo`) and converts it if necessary (using `ffmpeg`).

The original video file will be removed when the file conversion is complete.

Requirements
------------
- `mediainfo`
- `ffmpeg`

Install requirements by running e.g. `apt-get install ffmpeg mediainfo` (Debian) or `brew install ffmpeg mediainfo` (MacOS with Homebrew).

Usage
-----
```
./chromecastize.sh [--mp4 | --mkv] <videofile1> [videofile2 ...]
```

### Examples:
- `./chromecastize.sh /Volumes/MyNAS` - converts all videos on your NAS (assuming that it's mounted to `/Volumes/MyNAS`)
- `./chromecastize.sh Holiday.avi Wedding.avi` - converts specified video files

### Options:
- `--mp4` forces conversion to MPEG-4 container
- `--mkv` forces conversion to Matroska container

Authors
-------
- **Petr Kotek** (did the script save you some time? donations appreciated: www.petrkotek.com)
