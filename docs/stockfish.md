---
title: Setup Stockfish Engine
parent: Help
layout: default
nav_order: 1
---

# Setup Stockfish Engine

By default, ChessBuddy uses the links from [stockfishchess.org](https://stockfishchess.org/download/) to download the stockfish engine in different platforms:

| Platform     | Binary       |
|:-------------|:-------------|
| Windows |stockfish-windows-x86-64-sse41-popcnt|
|MacOS (Apple Silicon)|stockfish-macos-m1-apple-silicon|
| MacOS (Intel)|stockfish-macos-x86-64-sse41-popcnt|

This behaviour can be modified by settings in the file `ChessBuddy.properties` in the ChessBuddy installation folder (`ChessBuddy.app/Contents/MacOS/` on MacOS).

## Download a Different Binary, `stockfish.archive`
Set the value of `stockfish.archive` to the binary. For example, to download [the VNNI512 version](https://github.com/official-stockfish/Stockfish/releases/latest/download/stockfish-windows-x86-64-vnni512.zip), set `stockfish.archive` like this:
```
stockfish.archive = stockfish-windows-x86-64-vnni512.zip
```

## Download Stockfish from a Different Site, `stockfish.url`
Set the value of `stockfish.url` to the binary url that you would like to download. For example, to download stockfish from [sourceforge.net](https://sourceforge.net/projects/stockfish.mirror/files/sf_16.1/), set `stockfish.url` like this:
```
stockfish.url = https://sourceforge.net/projects/stockfish.mirror/files/sf_16.1/stockfish-macos-m1-apple-silicon.tar/download
```
**Meanwhile, `stockfish.archive` must be correctly set to the value from `stockfish.url`**. In this case, `stockfish.archive` should be:
```
stockfish.archive = stockfish-macos-m1-apple-silicon.tar
```

## Notes
1. If `stockfish.url` is NOT set, only zip file binary will be downloaded on Windows and only tar file binary will be downloaded on MacOS.
2. Only zip file is supported to be uncompressed.
3. tar file uncompression is depended on the OS (only works on MacOS and linux).