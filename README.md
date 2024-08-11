# GoPro Linux Tool

Various Linux Bash scripts and command line interface for processing media filmed on GoPro HERO 3, 4, 5, 6, and 7 cameras.

**New functions for GoPro HERO BLACK 7 devices.**

<b style="color: red;">NOTICE:</b>

This project has been deprectated, I will be adding most functions from this script to my new project [mmt](https://github.com/konradit/mmt). MMT is cross compatible with Win/OSX/Linux since it's a Golang program. 

### Usage:

````
- gopro
    >>Check for missing dependencies, e.g. ffmpeg, imagemagick and mencoder

- gopro timelapse [fps] [outfilename] [res width] [res height]
		>>Makes a timelapse with pictures in the current folder, make sure to cd to a DCIM/XXXGOPRO folder!
		>>Example: gopro timelapse 30 goproTL.mp4 1920 1080

- gopro superview
		>>Applies SuperView to all GoPro videos in the current dir

- gopro fisheye
		>>Fixes barrel distorsion to all GoPro pictures in the current folder

- gopro fisheye_video [video]
		>>Fixes barrel distorsion on GoPro videos, [video] is optional, remove to apply to all mp4 videos in current dir
		>>Also needs camera name input

- gopro convert
		>>Converts all GoPro MP4 videos to MPEG4 MOV videos for easy editing

- gopro convert-h265-toh264 [input_video]
		>>Converts videos with h.265 codecs to h.264
		>>This is useful for backwards compatibility. Some videos recorded on HERO Black 7 devices cannot be played on older hardware until codecs are converted.

- gopro slowmo [video]
		>>Reduces the speed in a High FPS GoPro Video
		>>Example: gopro slowmo GOPRO0553.MP4

- gopro trim [input video] [output video] [HH:MM:SS start] [HH:MM:SS end]
		>>Trims a video to start and end times
		>>Example: gopro trim GOPR0553.MP4 Trimmed.mp4 00:05:04 00:07:43

- gopro merge [output_video]
		>>Merges all videos present in the current folder to [output_video]

- gopro rotate90deg [input_video]
		>>Rotates video 90 degrees clockwise (edit 'translate=2' argument for counter-clockwise)

- gopro stabilize
		>>Stabilizes video
		>>Example: gopro GOPRO0005.MP4 Stabilized.MP4

- gopro sort
		>>Sorts media, please execute in DCIM/XXXGOPRO

- gopro wifiinfo
		>>Sets Wifi SSID and Password for HERO5, 6, 7 cameras

- gopro gif
		>>Makes gif from images in current dir
		>>Example: gopro gif 800x600 animation.gif

- gopro proxy [option]
		>>[rename] = renames .LRV to lowres/*.MP4
		>>[move] = when finish editing, moves highres/*.MP4 to lowres/

- gopro update
		>>Updates this script

- gopro help
		>>show this usage message

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
2. Then run the following commands
```
sudo curl https://raw.githubusercontent.com/KonradIT/gopro-linux/master/gopro -o /usr/local/bin/gopro
sudo chmod +x /usr/local/bin/gopro
```

## Other software worth checking out:

- https://github.com/encarsia/gpt
- https://github.com/konradit/gopro_fw_dl
