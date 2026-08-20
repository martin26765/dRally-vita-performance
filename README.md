# Death Rally Vita - Performance & Control Edition

An optimized performance and control fork of **Death Rally** for the PlayStation Vita.

## 👥 Credits & Acknowledgments
This project is a performance-focused fork and would not be possible without the incredible work of the original developers:
* **Original PS Vita Port:** Developed by **Enrique Somolinos** ([@enriquesomolinos](https://github.com)). Check out the original repository here: [enriquesomolinos/dRally-vita](https://github.com/dRally-vita).
* **Open Source Engine:** Based on the source code reconstruction by **urxp** ([urxp/dRally](https://github.com)).

---

## 👥 Créditos y Agradecimientos
Este proyecto es una versión optimizada enfocada en el rendimiento y no habría sido posible sin el increíble trabajo de los desarrolladores originales:
* **Puerto Original de PS Vita:** Desarrollado por **Enrique Somolinos** ([@enriquesomolinos](https://github.com)). Puedes ver su repositorio original aquí: [enriquesomolinos/dRally-vita](https://github.com/dRally-vita).
* **Motor de Código Abierto:** Basado en la reconstrucción de código de **urxp** ([urxp/dRally](https://github.com)).


🛠️ Changelog / Implemented Improvements:True Vertical Fullscreen (Letterbox Removed): Completely removed the legacy MS-DOS -DDR_LETTERBOX flag. Races now utilize the full vertical height of the PS Vita screen through automatic hardware scaling (960x544), eliminating the top and bottom black bars.Vectorized Math Optimizations (NEON Instructions): Compiled using aggressive performance flags (-Ofast, -mfpu=neon, and -mcpu=cortex-a9). This forces the Vita's ARM CPU to compute vehicle physics, rotation, and missile trajectories vectorially and simultaneously, stabilizing frame pacing.Input Lag Elimination (MS-DOS Delays Removed): Disabled legacy artificial frame timers (SDL_Delay) within the main update loop (__GET_FRAME_COUNTER). The CPU now processes frame rendering freely, ensuring buttons and direction inputs respond instantly to touch.Fluent & Continuous D-Pad Steering Fix: Completely rewrote the horizontal axis tracking logic inside events.c. This permanently fixes the native bug that caused the car to only "tap-steer" short distances. Vehicles now drift and turn smoothly and continuously as long as the D-Pad direction is held down.Ergonomic Control Remapping:Associated the MS-DOS Y (Yes) key to the Square (□) button as a dual action during races. This provides an immediate shortcut to accept race retirement inside the pause overlay, preventing players from getting trapped in that screen.Modern Code Toolchain Compatibility (C23 Standard): Fixed a syntactic conflict in db_ipx.c by removing a redundant boolean redefinition (typedef int bool), adapting the codebase flawlessly to the latest VitaSDK toolchain revisions.
