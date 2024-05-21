# BASH 2013 ARCHIVE

I have merged four old repos from 2013 with BASH scripts into one repo, for archive purposes. Enjoy.


# encode4yt.sh
## WHY?

Because I want to **upload audio files to YouTube**.

To be able to do that I must first [convert audio files into a format that will work on YouTube][1] and I want to do that through GNU/Linux command-line.

## WHAT?

This bash shell wrapper script will take **an audio file as input** and **output a video file** ready for upload to YouTube (e.g. via command-line script [youtube-upload][2]).

Audio formats supported: MP2, MP3, LC-AAC, HE-AAC, AC3

Audio quality remains unchanged therefore output file will be slightly bigger than input file.

## HOW?

### USAGE

    $ encode4yt INPUT [IMAGE]

Output file will be written in the same directory where `INPUT` file is located and also will have identical name, only different extension i.e. **mp4**.

You can provide as a second argument path to an `IMAGE` that you would like to use as a video background. Recommended `IMAGE` size is 1920x1080 pixels.

### REQUIREMENTS

1. [GNU sed][3]
2. [ImageMagick][4]
3. [FFmpeg][5]

### INSTALLATION

Example commands listed below are based on Ubuntu 12.04 LTS.

0. Install requirements, e.g.:
        
        $ sudo add-apt-repository ppa:jon-severinsson/ffmpeg
        $ sudo apt-get update
        $ sudo apt-get install sed imagemagick ffmpeg

1. Create a symbolic link to the `encode4yt.sh` in a directory that is already in your PATH.

## MISCELLANEOUS

This script is based on various sources from the Internet, mostly from:

- [EncodeforYouTube FFmpeg wiki page][6]
- [FFmpeg documentation][7]
- [ImageMagick v6 Examples -- Text to Image Handling][8]
- [Advanced encoding settings][9]



[1]: https://support.google.com/youtube/answer/1696878?hl=en&ref_topic=2888648
    "Upload audio or image files @ YouTube upload instructions and settings help"
[2]: https://code.google.com/p/youtube-upload/
    "youtube-upload"
[3]: http://www.gnu.org/software/sed/
    "GNU sed"
[4]: http://www.imagemagick.org/
    "ImageMagick"
[5]: http://ffmpeg.org/
    "FFmpeg"
[6]: https://trac.ffmpeg.org/wiki/Encode/YouTube
    "How to Encode Videos for YouTube and other Video Sharing Sites"
[7]: http://ffmpeg.org/ffmpeg-all.html
    "FFmpeg documentation"
[8]: http://www.imagemagick.org/Usage/text/
    "ImageMagick v6 Examples -- Text to Image Handling"
[9]: https://support.google.com/youtube/answer/1722171?hl=en&ref_topic=2888648
    "Advanced encoding settings @ YouTube upload instructions and settings help"


# download-website.sh
## Download web*

Download entire website or a single webpage.

## Useful extra options:
    --no-check-certificate
    --no-parent
    --accept
    --reject
    --quota=
    --limit-rate=
    --spider
    --no-directories
    --directory-prefix=
    --level=1

## MISCELLANEOUS

If you don't fancy GNU/Linux command-line too much you could try [HTTrack][10] - a free and easy-to-use offline browser utility that comes with a GUI.

[10]: http://www.httrack.com/
    "HTTrack Website Copier website"


# filenames-conversion.sh
## USAGE

`filenames-conversion PATTERN OUT IN [convert]`

Match files with (case sensitive!) **PATTERN** and replace **OUT** with **IN** string in filename if **convert** argument is provided, othervise conversion will be only simulated.


# squash-sbv.sh
## Why?

Because I want to make a decent documents out of automatic captions of my YouTube videos and I want to speed up a little bit that process.

## What?

This bash shell wrapper script will delete all position markers and empty lines and merge all that into one gigantic piece of text.

## How?

Usage: `squash-sbv captions.sbv [EXTENSION]`
