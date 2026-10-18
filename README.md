# Windows 3.0 on the Olivetti PC1

This repository is a discoverability page for experimental Yamaha display-driver work. The canonical implementation and public evidence live in [astrobleem/oemdisplay-tandy](https://github.com/astrobleem/oemdisplay-tandy).

## Public status

No Yamaha driver ZIP or source/evidence archive is currently published in the canonical repository or its GitHub Releases. The Candidate 03 screenshot and a curated test summary are public; they do not qualify an Olivetti PC1.

| Candidate | Recorded results | Qualification |
| --- | --- | --- |
| Standalone Yamaha V6355D emulator profile, B800h: `YAM160.DRV`, 160x200x16 | Build PASS; 49 host semantic cases and 30 rejected staging mutations; 92 Windows 3.0 cases in 86Box, 2,944,000 pixel comparisons and 160,000 cursor-pixel comparisons; two exit/relaunch cycles | Emulator profile only. Not a PC1 test or hardware qualification. |
| Olivetti PC1, B000h: `PC1YAMA.DRV`, 160x200x16 | Build PASS; 49 host semantic cases and 30 rejected staging mutations | No emulator, PC1 hardware, or Windows Setup test. |

![Original 86Box screenshot: Windows 3.0 on an emulated IBM XT (1986), standalone Yamaha V6355D B800h profile, 160x200x16](https://raw.githubusercontent.com/astrobleem/oemdisplay-tandy/main/docs/yamaha/YAMAHA03.JPG)

This original capture is from source-built [86Box commit ceb009f](https://github.com/86Box/86Box/commit/ceb009f17daeecbb81e1ddf26ad63beda9300afe), configured as an IBM XT (1986), 8088 at 4.77 MHz, 640 KB, with a standalone Yamaha V6355D card. It shows Windows 3.0 real mode at 160x200x16. It is emulator output, not a PC1 photo or physical-hardware result. See the [qualification summary](https://github.com/astrobleem/oemdisplay-tandy/blob/main/docs/yamaha/QUALIFICATION.MD) and [source baseline commit 212842c](https://github.com/astrobleem/oemdisplay-tandy/tree/212842cdd9c6877d8a01b00d8d6bc7e8e65f401a). The recorded Candidate 03 source commit is not in public Git history.

The B800 Setup run used the original local packet with `CGA.GR2` and `CGALOGO.LGO` present. Those Windows support files are not published; any future OEM Setup package would require users to supply matching files from their own licensed Windows 3.0 installation/media. No reduced Candidate 03 package was tested end-to-end.

Windows 3.1, physical PC1 operation, monitor output, and RGB/SCART behavior remain unqualified. The original eight-line XT Pixels fonts remain, so some 160-pixel dialogs can clip. See the [canonical Yamaha guide](https://github.com/astrobleem/oemdisplay-tandy/blob/main/experiments/YAMAHA/README.MD).