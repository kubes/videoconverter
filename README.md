Server Side HTML5 and Flash Video Converter
==============

A python script for server side conversion of videos to HTML5 and Flash video
formats.  Converts input videos to flv, ogg, mp4, and webm allowing them to be
played on a wide range of browsers including mobile devices.

Script usage:

    flash_converter.py [-hitpfdebvg]
      [-h | --help] prints this help and usage message
      [-i | --input-dir] the video input root directory.
      [-t | --output-dir] the video output directory.
      [-p | --prefix] a filename prefix for video outputs.
      [-f | --input-file] the input video file to convert
      [-d | --dry-run] dry run, print commands, don't convert
      [-e | --exists] ignore file if output already exists.
      [-b | --backup] backup old videos, rename to *.bak
      [-v | --verbosity] the verbosity level, quiet to debug
      [-g | --logfile] the conversion logfile
      [-m | --format] list of output formats, overrides default


To operate correctly serveral pieces of software must be installed from source.
The follwing guide explains in detail how to download and install the software
correctly. Other libraries such as libtheora may also need to be installed.

https://ffmpeg.org/trac/ffmpeg/wiki/UbuntuCompilationGuide

In general the script takes a single file or directory structure of files to 
convert.  For each video it uses the mediainfo command to gather information, 
using this information to create a web video of good quality at an acceptable
size.  This involves setting correct frame rates, sampling rates, and scaling
widths and heights.  Aspect ratios are kept the same as the original video and
it is scaled up or down as needed.  The video is padded with black bars to get
a final scaled output. Ffmpeg is used to do the conversion to different video 
output formats.

Please feel free to send any improvements or bug fixes.