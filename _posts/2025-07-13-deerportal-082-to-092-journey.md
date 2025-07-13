---
layout: single
title:  "DeerPortal: The Journey from 0.8.2 to 0.9.2"
date:   2025-07-13 18:00:00 +0100
categories: development gamedev deerportal sfml
---

DeerPortal version 0.8.2 was released in October 2019. When SFML 3.0 was released, I stopped development due to lack of time for the migration effort. After a six-year hiatus, version 0.9.2 was released in July 2025.

The primary challenge was migrating from SFML 2.x to SFML 3.0.1. The project was recently migrated, which required rewriting rendering code and implementing C++17 features with smart pointers. Code formatting was standardized to LLVM style, I replaced std::exit() calls with proper error handling, and the build system was updated to use modern CMake practices.

Following user feedback about lack of understanding of the game's core rules, a card notification system was added. When computer players pick up cards, an overlay displays the card texture and a message. The overlay remains visible for 4 seconds.

Performance improvements focused on rendering optimization. Diamond rendering was optimized using VertexArray. I batched 112 sprites into a single draw call, reducing draw calls by 99.1%. Performance testing shows 20-80% FPS improvement on older hardware.

Visual enhancements included a basic intro shader animation implemented using GLSL. I wrote the shader to reveal the game field through a grid-based animation with pseudo-random unveiling sequence. This feature will be developed further in future releases.

The development workflow was modernized through CI/CD pipeline rebuilding. DeerPortal now builds automatically for Linux, Windows, and Apple Silicon Macs. Each platform receives appropriate packaging: DMG for macOS, NSIS installer for Windows, and multiple formats for Linux.

Documentation was created in HANDBOOK.tex, which converts to PDF for each release.

Version 0.9.2 includes a timing fix where computer players wait 4 seconds after picking cards, plus a fix for the Windows build.