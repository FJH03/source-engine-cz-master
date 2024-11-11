# Source Engine
[![GitHub Actions Status](https://github.com/nillerusr/source-engine/actions/workflows/build.yml/badge.svg)](https://github.com/nillerusr/source-engine/actions/workflows/build.yml) [![GitHub Actions Status](https://github.com/nillerusr/source-engine/actions/workflows/tests.yml/badge.svg)](https://github.com/nillerusr/source-engine/actions/workflows/tests.yml)
 Discord: [![Discord Server](https://img.shields.io/discord/672055862608658432.svg)](https://discord.gg/hZRB7WMgGw)
 

Information from [wikipedia](https://wikipedia.org/wiki/Source_(game_engine)):

Source is a 3D game engine developed by Valve.
It debuted as the successor to GoldSrc with Half-Life: Source in June 2004,
followed by Counter-Strike: Source and Half-Life 2 later that year.
Source does not have a concise version numbering scheme; instead, it was released in incremental versions

Source code is based on TF2 2018 leak. Don't use it for commercial purposes.

This project is using waf buildsystem. If you have waf-related questions look https://waf.io/book

# Current tasks
- Need fix crouch anim state bugs in Android
- Need fix thirdperson cam render

# What this?
- czero character and design
- source-engine protocol 26

# How to Build?
- [Building instructions(EN)](https://github.com/nillerusr/source-engine/wiki/Source-Engine-(EN))
- [Building instructions(RU)](https://github.com/nillerusr/source-engine/wiki/Source-Engine-(RU))

## Dedicated Server for Counter-Strike Condition Zero Source:
###  Windows: 
    waf configure -T release --prefix ./build_server --build-games=cstrike -4 -d --disable-warns
###  Linux: 
    python3 waf configure -T release --prefix ./build_server --build-games=cstrike -4 -d --disable-warns

## Game for Counter-Strike Condition Zero Source:
###  Windows: 
    waf configure -T release --prefix ./build_game --build-games=cstrike -4 --disable-warns
###  Linux: 
    python3 waf configure -T release --prefix ./build_game --build-games=cstrike -4 --disable-warns
###  Android: 
    export ANDROID_NDK_HOME="/home/fjh03/android-ndk-r10e" export PATH="/home/fjh03/clang+llvm-11.1.0-x86_64-linux-gnu-ubuntu-16.04/bin:$PATH";CFLAGS="-O2" CXXFLAGS="-O2" LDFLAGS="-s -flto" python3 waf configure -T release --build-games=cstrike --togles --android=aarch64,host,21 --prefix=./cstrike_build --disable-warns
