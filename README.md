# Windows 3.0 Yamaha display experiments for Olivetti PC1

Experimental Windows 3.0 real-mode Yamaha V6355D profiles are available from the canonical [oemdisplay-tandy project](https://github.com/astrobleem/oemdisplay-tandy):

- [Download PC1/B000 Candidate 03](https://raw.githubusercontent.com/astrobleem/oemdisplay-tandy/main/downloads/experimental/yamaha-candidate03/PC1-B000-CANDIDATE03.ZIP) — `PC1YAMA.DRV`, 160×200×16
- [Download standalone B800 Candidate 03](https://raw.githubusercontent.com/astrobleem/oemdisplay-tandy/main/downloads/experimental/yamaha-candidate03/YAMAHA-B800-CANDIDATE03.ZIP) — `YAM160.DRV`, 160×200×16
- [Source and evidence archive](https://raw.githubusercontent.com/astrobleem/oemdisplay-tandy/main/downloads/experimental/yamaha-candidate03/YAMAHA-CANDIDATE03-SOURCE-EVIDENCE.ZIP)

These are repository-file downloads, not GitHub Release assets or installers. The PC1/B000 profile has build and host checks only; no Windows Setup, emulator, or physical PC1 run is recorded. Do not treat it as qualified. For either package, follow its included README and the [Yamaha install and recovery guide](https://github.com/astrobleem/oemdisplay-tandy/blob/main/experiments/YAMAHA/README.MD) in a disposable Windows 3.0 clone. The Setup profiles need `CGA.GR2` and `CGALOGO.LGO` from your own licensed Windows media; neither file is included. The reduced B800 package has not been tested end-to-end.

## Emulator screenshot

![Original 86Box screenshot: Windows 3.0 real mode on an emulated IBM XT (1986), standalone Yamaha V6355D B800h profile, 160×200×16](https://raw.githubusercontent.com/astrobleem/oemdisplay-tandy/main/docs/yamaha/YAMAHA03.JPG)

*86Box built from [commit ceb009f](https://github.com/86Box/86Box/commit/ceb009f17daeecbb81e1ddf26ad63beda9300afe) · emulated IBM XT (1986), 8088 at 4.77 MHz, 640 KB · Windows 3.0 real mode · Yamaha V6355D at B800h, 160×200×16. This shows the B800 emulator profile, not an Olivetti PC1 or physical hardware. See the [qualification record](https://github.com/astrobleem/oemdisplay-tandy/blob/main/docs/yamaha/QUALIFICATION.MD) and public [source baseline commit 212842c](https://github.com/astrobleem/oemdisplay-tandy/tree/212842cdd9c6877d8a01b00d8d6bc7e8e65f401a); the recorded candidate source commit is not in public Git history.*

Physical PC1 operation, monitor output, RGB/SCART behavior, and Windows 3.1 remain unqualified. Some 160-pixel dialogs can clip. See the [canonical development repository](https://github.com/astrobleem/oemdisplay-tandy).
