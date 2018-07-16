---
layout: post
title: Resize/scale images with the command line
date: 2018-07-16
---

Software: [ImageMagick](https://imagemagick.org/).

Examples:

    convert -resize 640x480 -quality 90 source.png output.png

    convert -resize 50% source.jpg output.jpg

    convert -scale 270 source.png output.png
    
[ImageMagick Documentation](https://imagemagick.org/script/convert.php) for convert.
