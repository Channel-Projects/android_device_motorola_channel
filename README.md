TWRP device tree for Motorola g(7) Play (channel)
==================================
## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core 1.8 GHz Cortex-A53
CHIPSET | Qualcomm SDM632 Snapdragon 632
GPU     | Adreno 506
Memory  | 2GB
Shipped Android Version | 9.0 (Pie)
Internal Storage | 32GB
microSD | Up to 1 TB (dedicated slot)
Battery | 3000 mAh
Dimensions | 147.3 x 71.5 x 8 mm 
Display | 720 x 1512  pixels, 5.7-inch IPS LCD
Rear Camera  | 13 MP (f/2.0, 1.12µm, PDAF)
Front Camera | 8 MP (f/2.2, 1.12µm, HDR)

![Motorola g7 play](https://fdn2.gsmarena.com/vv/pics/motorola/motorola-moto-g7-play-1.jpg "Motorola g7 play")

### Kernel Source

See /prebuilt/README.md

### How to compile

```sh
. build/envsetup.sh
lunch twrp_channel-eng
mka adbd bootimage
```

### Build with TWRP installer

To automatically make the twrp installer, you need to import this commit in the build/make path:
```sh
https://gerrit.omnirom.org/#/c/android_build/+/33182/
```

Then add @osm0sis' standard twrp_abtemplate repo to a local manifest as indicated below (followed by another `repo sync` to download the repo):
```xml
<project name="osm0sis/twrp_abtemplate" path="bootable/recovery/installer" remote="github" revision="master"/>
```

### Copyright
 ```
  /*
  *  Copyright (C) 2013-19 The OmniROM Project
  *
  * This program is free software: you can redistribute it and/or modify
  * it under the terms of the GNU General Public License as published by
  * the Free Software Foundation, either version 3 of the License, or
  * (at your option) any later version.
  *
  * This program is distributed in the hope that it will be useful,
  * but WITHOUT ANY WARRANTY; without even the implied warranty of
  * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  * GNU General Public License for more details.
  *
  * You should have received a copy of the GNU General Public License
  * along with this program.  If not, see <http://www.gnu.org/licenses/>.
  *
  */
  ```
