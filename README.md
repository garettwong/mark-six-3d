# 六合彩 · Mark Six — 5th-Generation 3D Draw Machine

A photoreal, AAA-quality **Three.js** 3D simulation of the Hong Kong Jockey Club's
**Mark Six (六合彩)** lottery — modelled on the current **5th-generation Smartplay draw
machine** that debuted in May 2026 for the lottery's 50th anniversary.

Press **START DRAW** to mix all 49 balls inside the rotating crystal globe and draw the
**6 main numbers + 1 extra number**, just like the live televised draw.

**▶ Live: https://garettwong.github.io/mark-six-3d/**

## Authentic details

- **Official 49-ball colour scheme** (verified across multiple Hong Kong sources):
  - 🔴 **Red (17):** 1, 2, 7, 8, 12, 13, 18, 19, 23, 24, 29, 30, 34, 35, 40, 45, 46
  - 🔵 **Blue (16):** 3, 4, 9, 10, 14, 15, 20, 25, 26, 31, 36, 37, 41, 42, 47, 48
  - 🟢 **Green (16):** 5, 6, 11, 16, 17, 21, 22, 27, 28, 32, 33, 38, 39, 43, 44, 49
- **Balls** are solid red/blue/green glossy spheres with the number in black on a white oval
  patch — matching the real physical balls.
- **5th-gen machine** likeness: tall white tower, a transparent bi-directionally-rotating
  crystal globe (gravity-mix), a central lift column, and two white-lit "lightsaber" display
  tubes — **right tube = the 6 drawn numbers, left tube = the extra number**.
- The 6 drawn numbers are displayed **sorted ascending**; the extra number is shown apart.

## Tech

- [Three.js](https://threejs.org/) r184 — PBR materials, `MeshPhysicalMaterial` transmission
  glass, `RoomEnvironment` image-based lighting (no external HDRI), `UnrealBloomPass`,
  ACES tonemapping, HDR multisampled compositing.
- [cannon-es](https://github.com/pmndrs/cannon-es) — real rigid-body physics for the 49
  tumbling balls, with analytic spherical containment.
- WebAudio-synthesised sound effects (no audio assets).
- Single self-contained `index.html`, ES modules via import map from a CDN — no build step.

## Disclaimer

This is an **unofficial, fan-made** simulation created for entertainment and educational
purposes. It is **not affiliated with, endorsed by, or connected to The Hong Kong Jockey
Club**. No real wagering is involved. "Mark Six" and "六合彩" are referenced for descriptive
purposes only.
