---
layout: post
title: Convert audio with ffmpeg on the command line
date: 2018-02-07
---

## ffmpeg:

For example, from m4a to ogg, on the command line:

    ffmpeg -i input.m4a -vn -sn -acodec libvorbis output.ogg 

where:
-vn to exclude video
-sn to exclude subtitles
-i  to indicate the input
-acodec to say that you are going to use an audio codec
libvorbis for ogg

The order of the arguments is important.
