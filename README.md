# TCS-DLSSV-PART2

## Required

1. **ReShade with add-on support**, and a decent NVIDIA GPU (**RTX 50 series highly recommended**).
2. **Part 1** from my Nexus profile: https://www.nexusmods.com/profile/TheChadSurvivor
3. **RTX 40 or 50 series** — RTX 30 and below run at about **1 FPS**.

---

Stock *Star Wars: Knights of the Old Republic* (and K2) **OpenGL ReShade** pack for DLSS 5 neural rendering. Not reone.

## Installation

1. Install **ReShade with add-on support**. Sell your soul for a good NVIDIA GPU (**50 series highly recommended**).
2. Apply any **widescreen patches** for KotOR 1.
3. Install **Part 1**. Choose the pack for your card and drop the folders inside `contents` into your game folder.  
   https://www.nexusmods.com/profile/TheChadSurvivor
4. Install **Part 2** (this). Choose the pack for your card and drop the folders inside `contents` into your game folder.
5. Run the game. For **KotOR 2**, the resolution can look wrong on first launch — set it again in Options (e.g. 1080p).  
   A small window will pop up. That is the **feeder** (another layer). Leave it.
6. Open the ReShade menu (**Home**), go to **DLSS 5**, enable it and **neural rendering**.
7. Done. Adjust it to your heart's content.

Please note: **RTX 30 series and below will run very, very slow (around 1 FPS).**

Download **one** zip from [Releases](https://github.com/TheChadSurvivor/TCS-DLSSV-PART2/releases):

| Zip | GPU |
| --- | --- |
| `TCS K1-2 DLSS5 RTX 40 and 50 GIT.zip` | RTX 40 / 50 — **use this** |
| `TCS K1-2 DLSS5 RTX 30 GIT.zip` | RTX 30 — ~1 FPS, not recommended |

Unzip, then copy everything **inside** `Move Inside Content to Game Folder - GitHub` (the `contents`) into the folder that contains `swkotor.exe` / `swkotor2.exe`.

Do not mix the two `nvngx_dlssnr.dll` files.

---

## Copyright disclaimer

TCS-DLSSV-PART2 is a packaging and 32-bit OpenGL bridge around existing community work. It is **not** affiliated with, endorsed by, or supported by NVIDIA, BioWare, Lucasfilm, Disney, or the ReShade / RenoDX authors.

NVIDIA DLSS / NGX / Streamline binaries, ReShade, the RenoDX DLSS 5 add-on, and LumeniteFX remain the property of their respective owners and keep their own licenses. This repository’s MIT license does **not** cover those files.

**Heavy credit** to [DLSS5-Feeder](https://github.com/jlrouzies-fr/DLSS5-Feeder) by Jean-Laurent ROUZIES. TCS_DLSS5 is derived from that project (OpenGL 32-bit path + KotOR drop-in).

## Credits

D3D11↔D3D12 shared-texture / fence transport adapted from NIGos' [dlss5-dx11-bridge](https://github.com/NIGos/dlss5-dx11-bridge) (MIT) — not re-hosted here.

Motion vectors: interop happens purely by declaring each provider's output texture identically, so ReShade binds the same resource — the mechanism dh_uber_rt and VORT use. Thanks to [LumeniteFX](https://github.com/umar-afzaal/LumeniteFX) (Umar Afzaal), iMMERSE Launchpad (MartysMods), VORT (MIT), Jakob Wapenhensch's [ReshadeMotionEstimation](https://github.com/JakobPCoder/ReshadeMotionEstimation) (CC BY-NC 4.0), the qUINT ecosystem that established the `texMotionVectors` convention, and [AlucardDH's dh-reshade-shaders](https://github.com/AlucardDH/dh-reshade-shaders) for the provider-switch pattern. No provider's files are bundled or included by this project's shader — install them from their own repositories, under their own licenses.

DLSS 5 neural rendering: the RenoDX community's `renodx-dlss5` add-on.

ReShade add-on API by Patrick Mours.

dgVoodoo2 by Dege — the D3D9 translation layer that makes the DirectX 9 path possible.

D3D12 stability findings independently confirmed by the [Pizzawookiee fork](https://github.com/Pizzawookiee/DLSS5-Feeder)'s diagnostics.

## License

MIT — see [LICENSE](LICENSE). This covers only the TCS packaging and the feeder-derived code in this project. The dependencies above keep their own licenses.
