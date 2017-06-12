#GoPro Linux Tool

Bash script which helps with post production for GoPro cameras in Linux, can be used as a replacement for GoPro Studio

###Features:

First run ``gopro`` to check if you have any missing dependencies (it relies on FFmpeg, imagemagick and mencoder)

``gopro help`` will show:

````
- gopro timelapse [fps] [outfilename] [res width] [res height]
Makes a timelapse with pictures in the current folder, make sure to cd to a DCIM/XXXGOPRO folder!
Example: gopro timelapse 30 goproTL.mp4 1920 1080

- gopro superview
Applies SuperView to all GoPro videos in the current dir

- gopro fisheye
Fixes barrel distorsion to all GoPro pictures in the current folder

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

###Download/Install

    sudo curl https://raw.githubusercontent.com/KonradIT/gopro-linux/master/gopro > /usr/local/bin/gopro

Note, /usr/local/bin/ is for all users, ~/.bin/ is for current user.
