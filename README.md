HTML5 and Flash Video Converter
==============

A python script that converts video files to multiple formats including flv, ogg, 
mp4 (playable on ios), and webm.  This should allow videos to be played on all
browsers using html5 and flash.

This script assumes the server has all the required software.  Please follow
this guide to install everything.

https://ffmpeg.org/trac/ffmpeg/wiki/UbuntuCompilationGuide

Other libraries such as libtheora may also need to be installed.

The mediainfo command is used to gather information about the video file to be
converted, such as video width and height and frame rate, to allow good quality
conversion.  The ffmpeg command is used to do the actual conversion to different
video output formats.  Aspect ratios are kept and padding is applied to videos.

Video files can be converted individually or in batch.  There are options for 
saving old files when converting individually. When batch converting videos, all
files under a given directory are assumed to be video files.  The converted 
files can then be output to another directory keeping the same directory 
structure.
