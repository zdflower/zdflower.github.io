---
layout: post
title: Convert audio with ffmpeg on the command line
date: 2018-02-07
---

## ffmpeg:

For example, from m4a to ogg, on the command line:

    ffmpeg -i input.m4a -vn -sn -acodec libvorbis output.ogg 

Where:
* _-vn_ to exclude video
* _-sn_ to exclude subtitles
* _-i_  to indicate the input
* _-acodec_ to say that you are going to use an audio codec
* _libvorbis_ for ogg

The __order__ of the arguments is important.