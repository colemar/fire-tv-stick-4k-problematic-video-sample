# Fire TV Stick 4K Problematic Video Samples
Fire TV Stick 4K (2nd gen.) fails on some videos that play well on other Android platforms.

![image](https://github.com/user-attachments/assets/792af13e-5c01-4c28-836d-48ed154abb1a)

These are some video samples that do not play correctly on Fire TV Stick 4K (2nd gen.).
I try to keep them under 10 seconds.

## [black-screen-no-osd.mp4](https://github.com/colemar/fire-tv-stick-4k-problematic-video-samples/raw/refs/heads/main/video/black-screen-no-osd.mp4)
This one results in a completely black screen, not even the OSD is displayed.
It plays well on:
- Pixel 7 Pro phone (Android 14): VLC, MX Player, Kodi
- TV LG OLED48CX3LB (WebOS updated to sept 2024): Kodi, Plex (no transcoding), Jellyfin (no transcoding), Stremio
- On Windows 10: Windows Media Player 12.0, MPC-BE 1.8.0, SMPlayer 24.5.0, Kodi 21.1.

On TIMVISION Box Sagemcom DTIW3930 there is no audio output irrespective of player.

Here is the Mediainfo report from the original uncutted file:
```
General                                                 Unique ID                                : 123118159945506803629099092060091709300 (0x5C9FB1F1A8FDF446CA9C9D161C67F774)
Complete name                            : Alien.Romulus.2024.4K.HDR.DV.2160p WEBDL Ita Eng x265-NAHOM.mkv
Format                                   : Matroska
Format version                           : Version 4
File size                                : 21.6 GiB
Duration                                 : 1 h 59 min   Overall bit rate                         : 25.8 Mb/s
Encoded date                             : UTC 2024-10-15 22:16:45                                              Writing application                      : mkvmerge v87.0 ('Black as the Sky') 64-bit
Writing library                          : libebml v1.4.5 + libmatroska v1.7.1

Video
ID                                       : 1
Format                                   : HEVC
Format/Info                              : High Efficiency Video Coding
Format profile                           : Main 10@L5@High
HDR format                               : Dolby Vision, Version 1.0, dvhe.08.06, BL+RPU, HDR10 compatible / SMPTE ST 2094 App 4, Version 1, HDR10+ Profile A compatibleCodec ID                                 : V_MPEGH/ISO/HEVC
Duration                                 : 1 h 58 min
Bit rate                                 : 24.5 Mb/s
Width                                    : 3 840 pixels
Height                                   : 1 606 pixels
Display aspect ratio                     : 2.40:1
Frame rate mode                          : Constant
Frame rate                               : 24.000 FPS
Color space                              : YUV
Chroma subsampling                       : 4:2:0 (Type 2)
Bit depth                                : 10 bits
Bits/(Pixel*Frame)                       : 0.166
Stream size                              : 20.4 GiB (95%)                                                       Language                                 : English
Default                                  : Yes          Forced                                   : No
Color range                              : Limited      Color primaries                          : BT.2020
Transfer characteristics                 : PQ           Matrix coefficients                      : BT.2020 non-constant
```
Feedback [here](https://www.reddit.com/r/firetvstick/comments/1g7mv91/fire_tv_stick_4k_does_not_play_some_pretty_common/).
