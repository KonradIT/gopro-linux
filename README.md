# GoPro Linux Tool

Bash script which helps with post production for GoPro cameras in Linux, can be used as a replacement for GoPro Studio

### Features:

First run `gopro` to check if you have any missing dependencies (it relies on FFmpeg, imagemagick and mencoder)

`gopro help` will show:

````
- gopro timelapse [fps] [outfilename] [res width] [res height]
Makes a timelapse with pictures in the current folder, make sure to cd to a DCIM/XXXGOPRO folder!
Example: gopro timelapse 30 goproTL.mp4 1920 1080

- gopro superview
Applies SuperView to all GoPro videos in the current dir

- gopro fisheye
Fixes barrel distorsion to all GoPro pictures in the current folder

- gopro fisheye_video [video]
Fixes barrel distorsion on GoPro videos, [video] is optional, remove to apply to all mp4 videos in current dir

- gopro convert
Converts all GoPro MP4 videos to MPEG4 MOV videos for easy editing

- gopro slowmo [video]
Reduces the speed in a High FPS GoPro Video
Example: gopro slowmo GOPRO0553.MP4

- gopro trim [input video] [output video] [HH:MM:SS start] [HH:MM:SS stop]
Trims a video, use this to trim a slow motion video!
Example: gopro trim GOPR0553.MP4 Trimmed.mp4 00:05:04 00:07:43

- gopro sort
Sorts media, please execute in DCIM/XXXGOPRO!
````

### Install

#### [Arch Linux](https://www.archlinux.org/)

Available as [AUR package](https://aur.archlinux.org/packages/gopro-tools-git/)

```
git clone https://aur.archlinux.org/gopro-tools-git.git
cd gopro-tools-git
makepkg -si
```

#### manually on Linux

1. First install [FFmpeg](http://ffmpeg.org/), [imagemagick](http://www.imagemagick.org/) and [mencoder (now part of mplayer)](http://www.mplayerhq.hu/) for your distribution.
2. Then run the folowing commands
```
sudo curl https://raw.githubusercontent.com/KonradIT/gopro-linux/master/gopro -o /usr/local/bin/gopro
sudo chmod +x /usr/local/bin/gopro
```

## TODO:

- windows/mac version?
- update camera firmware using [gopro_fw_dl](http://github.com/konradit/gopro_fw_dl)
- flux
- install kdenlive protune presets

## Other software worth checking out:

- https://github.com/encarsia/gpt