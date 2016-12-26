# FFmpeg - A64 platform (Cedrus HW Encoder - CMOS Camera)

FFmpeg with built in Cedrus264 HW Encoder for the A64 platform.
This was build on Ubuntu Xenial 16.04


Dependencies
============

	sudo apt-get install libmp3lame-dev libx264-dev libpulse-dev libv4l-dev libav-dev


Source Code and Instructions
============================

https://github.com/linux-sunxi/libcedrus

https://github.com/uboborov/ffmpeg_h264_H3


How to use it
=============

- Attach you CMOS camera
- Clone the repo: git clone https://github.com/avafinger/ffmpeg_cedrus264_A64.git
	or get the deb: https://github.com/avafinger/ffmpeg-3.1.4_cedrus264_A64_deb
- cd ffmpeg_cedrus264_A64
- type: 

	sudo ./ffmpeg -f v4l2 -channel 0 -video_size 1024x768 -i /dev/video0 -pix_fmt nv12 -r 15 -qp 20 -b:v 64k -c:v cedrus264 test.mp4

Play the MP4 file with your preferred application

Limitations
===========
 * Read the author's note - POC
 * maximum win size is 1024x768
