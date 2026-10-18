# Windows 3.0 on the Olivetti PC1

This repository is a discoverability page for experimental Olivetti PC1 display-driver work. The canonical implementation and any future public release belong in [astrobleem/oemdisplay-tandy](https://github.com/astrobleem/oemdisplay-tandy).

## Current public status

No Olivetti driver package is published in the canonical project's [releases](https://github.com/astrobleem/oemdisplay-tandy/releases). Recovered private evidence identifies two distinct candidate builds; neither is currently a public download:

- **PC1/B000 candidate:** `PC1-B000/PC1YAMA.DRV` (54,992 bytes; SHA-256 `8c73d52d6811fff071dd252343c33702a1cfea0b2613ec8b20faf5a739da2a08`). It was built and passed ISA/linker checks, but this PC1-specific profile has not been tested on a PC1 or in an emulator. It is not a qualified PC1 driver.
- **Standalone V6355D emulator profile:** `EMULATOR-B800/YAM160.DRV` (55,008 bytes; SHA-256 `a3d339a3f1e831bd8499fb2b0a28c683bf08f9fbeb0e96689dc3f6ef9a627c8a`). The reported Windows 3.0 guest run used source-built [86Box commit `ceb009f17daeecbb81e1ddf26ad63beda9300afe`](https://github.com/86Box/86Box/commit/ceb009f17daeecbb81e1ddf26ad63beda9300afe), configured as an IBM XT (1986), 8088 at 4.77 MHz, 640 KB, with a standalone V6355D card using the B800, display type 2 / RGB333 profile. It passed 92 cases, 2,944,000 pixel comparisons plus cursor comparisons, two exit/relaunch cycles, and DOS Setup installation. This qualifies only that emulator profile; it does not qualify the PC1/B000 profile or real hardware.

The candidate binaries, source/evidence bundle, and capture remain private while their contents are audited for a safe public package. No emulator or hardware support is claimed for the Olivetti PC1, and there is no direct download yet. Windows 3.1 remains unqualified.

- [Canonical source project at the public upstream snapshot](https://github.com/astrobleem/oemdisplay-tandy/tree/212842cdd9c6877d8a01b00d8d6bc7e8e65f401a)
- [PR #137: experimental-driver navigation](https://github.com/astrobleem/oemdisplay-tandy/pull/137)
- [Canonical repository issue tracker](https://github.com/astrobleem/oemdisplay-tandy/issues)

When a public package is ready, use the canonical project's release notes and installation guide. This repository contains no driver binaries or duplicated implementation.
