---
title: "Colors"
date: 2014-12-17 13:39:51
categories:
  - trivia
tags:
  - colorspace
  - yuv2rgb
toc: true
---

[List of color spaces and their uses - Wikiwand](https://www.wikiwand.com/en/List_of_color_spaces_and_their_uses)
[What are the differences between RGB, HSV and CIE-Lab? - Quora](https://www.quora.com/What-are-the-differences-between-RGB-HSV-and-CIE-Lab)

[Colour management, part 1](https://bjango.com/articles/colourmanagementgamut/)
[Colour management, part 2](https://bjango.com/articles/colourmanagementgamma/)
[Colour management, part 3](https://bjango.com/articles/colourmanagementsettings/)

[Android Color Management: What Developers and Designers Need to Know](https://medium.com/google-design/android-color-management-what-developers-and-designers-need-to-know-4fdd8054557e) in Android Oreo
[Understanding Color (Google I/O '17) - YouTube](https://www.youtube.com/watch?v=r8NeG0wmFXM)
[Compatible Color: The Ultimate Three-For-One Special - YouTube](https://www.youtube.com/watch?v=InrDRGTPqnE)

---

# Colorspace

[Color tutorial](http://www.tomjewett.com/colors/)
[The HSB Color System: A Practitioner's Primer – Learn UI Design](https://learnui.design/blog/the-hsb-color-system-practicioners-primer.html)

[Colors - Radiolab](http://www.radiolab.org/story/211119-colors/)

[Data Color Picker – Learn UI Design](https://learnui.design/tools/data-color-picker.html)

There are several standards regulating the YUV colorspace:

## EBU

```
Y'= 0.299*R' + 0.587*G' + 0.114*B'
U'=-0.147*R' - 0.289*G' + 0.436*B' = 0.493*(B' - Y')
V'= 0.615*R' - 0.515*G' - 0.100*B' = 0.877*(R' - Y')

R'= Y' + 0.000*U' + 1.140*V'
G'= Y' - 0.396*U' - 0.581*V'
B'= Y' + 2.029*U' + 0.000*V'
```

## ITU.BT-601

```
Y'= 0.299*R' + 0.587*G' + 0.114*B'
Cb=-0.169*R' - 0.331*G' + 0.500*B' = 0.564(B - Y')
Cr= 0.500*R' - 0.419*G' - 0.081*B' = 0.713(R - Y')

R'= Y' + 0.000*U' + 1.403*V'
G'= Y' - 0.344*U' - 0.714*V'
B'= Y' + 1.773*U' + 0.000*V'
```

## ITU.BT-709

```
Y'= 0.2215*R' + 0.7154*G' + 0.0721*B'
Cb=-0.1145*R' - 0.3855*G' + 0.5000*B'
Cr= 0.5016*R' - 0.4556*G' - 0.0459*B'

R'= Y' + 0.0000*Cb + 1.5701*Cr
G'= Y' - 0.1870*Cb - 0.4664*Cr
B'= Y' - 1.8556*Cb + 0.0000*Cr
```

## yCbCr<-->rgb (ITU.BT-565?)

```
Y’ = 0.257*R' + 0.504*G' + 0.098*B' + 16
Cb' = -0.148*R' - 0.291*G' + 0.439*B' + 128
Cr' = 0.439*R' - 0.368*G' - 0.071*B' + 128

R' = 1.164*(Y’-16) + 1.596*(Cr'-128)
G' = 1.164*(Y’-16) - 0.813*(Cr'-128) - 0.392*(Cb'-128)
B' = 1.164*(Y’-16) + 2.017*(Cb'-128)
```

## Packaging and colorspace

Packaging is defined by [fourcc](http://www.fourcc.org/yuv.php) and independent of the colorspace.

Add principles: additive and subtractive
[JavaScript 进行 RGB 和 HEX(16 进制)颜色转换 - 进击的程序媛，Laker's blog](http://laker.me/blog/2015/10/10/15_1010_rgb_hex_color/#more)

## Node.js library

[MoOx/color-convert](https://github.com/MoOx/color-convert)
[substack/mrcolor](https://github.com/substack/mrcolor)
[Automattic/Color.js](https://github.com/Automattic/Color.js)

## References:

http://en.wikipedia.org/wiki/YUV
http://www.fourcc.org/fccyvrgb.php
http://www.fourcc.org/yuv.php
http://www.martinreddy.net/gfx/faqs/colorconv.faq
http://blog.weisu.org/2008/01/ycbcr-yuv-sampling.html
http://discoverybiz.net/enu0/faq/faq_YUV_YCbCr_YPbPr.html
