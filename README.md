# FFmpeg - A64 platform (Cedrus HW Encoder - CMOS Camera)

FFmpeg with built in Cedrus264 HW Encoder for the A64 platform.
This was build on Ubuntu Xenial 16.04


Dependencies
============

	sudo apt-get install libmp3lame-dev libx264-dev libpulse-dev libv4ll2rds0


Source Code and Instructions
============================

https://github.com/linux-sunxi/libcedrus
https://github.com/uboborov/ffmpeg_h264_H3


How to use it
=============

- Attach you CMOS camera
- Clone the repo: git clone https://github.com/avafinger/ffmpeg_cedrus264_H3.git
- cd ffmpeg_cedrus264_H3
- type: 

	sudo ./ffmpeg -f v4l2 -channel 0 -video_size 640x480 -i /dev/video0 -pix_fmt nv12 -r 30 -b:v 64k -c:v cedrus264 test.mp4

Play the MP4 file with your preferred application

Limitations
===========
 * Read the author's notice - POC
