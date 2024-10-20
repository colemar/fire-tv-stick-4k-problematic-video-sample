# Fire TV Stick 4K Problematic Video Sample
Fire TV Stick 4K (2nd gen.) fails on some videos that play well on other Android platforms.

![image](https://github.com/user-attachments/assets/792af13e-5c01-4c28-836d-48ed154abb1a)

## [black-screen-no-osd.mkv](https://github.com/colemar/fire-tv-stick-4k-problematic-video-samples/raw/refs/heads/main/video/black-screen-no-osd.mkv)
This is a video sample that does not play on Fire TV Stick 4K (2nd gen.).
It results in a completely black screen, not even the OSD is displayed.

It plays well on:
- Pixel 7 Pro phone (Android 14): VLC, MX Player, Kodi
- TV LG OLED48CX3LB (WebOS updated to sept 2024): Kodi, Plex (no transcoding), Jellyfin (no transcoding), Stremio
- On Windows 10: Windows Media Player 12.0, MPC-BE 1.8.0, SMPlayer 24.5.0, Kodi 21.1.

On TIMVISION Box Sagemcom DTIW3930 there is no audio output irrespective of player.

Here is the Mediainfo report:
```
General
Unique ID                                : 51265169665455028893211215284950431723 (0x2691500260A9FBCFDA6F0B400EEE77EB)
Complete name                            : black-screen-no-osd.mkv
Format                                   : Matroska
Format version                           : Version 4
File size                                : 23.9 MiB
Duration                                 : 8 s 188 ms
Overall bit rate                         : 24.5 Mb/s
Writing application                      : Lavf60.16.100
Writing library                          : Lavf60.16.100
ErrorDetectionType                       : Per level 1

Video
ID                                       : 1
Format                                   : HEVC
Format/Info                              : High Efficiency Video Coding
Format profile                           : Main 10@L5@High
HDR format                               : Dolby Vision, Version 1.0, dvhe.08.06, BL+RPU, HDR10 compatible / SMPTE ST 2094 App 4, Version 1, HDR10+ Profile A compatible
Codec ID                                 : V_MPEGH/ISO/HEVC
Duration                                 : 8 s 188 ms
Bit rate                                 : 24.5 Mb/s
Width                                    : 3 840 pixels
Height                                   : 1 606 pixels
Display aspect ratio                     : 2.40:1
Frame rate mode                          : Variable
Frame rate                               : 20 909.868 FPS
Original frame rate                      : 24.000 FPS
Color space                              : YUV
Chroma subsampling                       : 4:2:0 (Type 2)
Bit depth                                : 10 bits
Bits/(Pixel*Frame)                       : 0.000
Stream size                              : 20.4 GiB
Language                                 : English
Default                                  : Yes
Forced                                   : No
Color range                              : Limited
Color primaries                          : BT.2020
Transfer characteristics                 : PQ
Matrix coefficients                      : BT.2020 non-constant
Mastering display color primaries        : BT.2020
Mastering display luminance              : min: 0.0050 cd/m2, max: 1000 cd/m2
Maximum Content Light Level              : 714 cd/m2
Maximum Frame-Average Light Level        : 123 cd/m2
```
[Feedback](https://www.reddit.com/r/firetvstick/comments/1g7mv91/fire_tv_stick_4k_does_not_play_some_pretty_common/).
[Github issue](https://github.com/jellyfin/jellyfin-androidtv/issues/2630)

Possible workaround:
```
alias dovifix='tf() { ffmpeg -i "$1" -map 0 -c copy -bsf:v "filter_units=remove_types=39" "dovifix_$1"; }; tf'
dovifix moviefiletofix.mkv
```
