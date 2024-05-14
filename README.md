# emscripten-dev-environment README

emscripten Developer Container Environment for Visual Studio Code.

Author: David González Zornoza

## Features

Project to set up a development environment for emscripten, in a visual studio code dev-container.
<https://emscripten.org/index.html>

## Requirements

- installed visual studio code dev-container extension:
  [https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers](vscode-remote.remote-containers)

- Docker environment

## How to use

https://floooh.github.io/2023/11/11/emscripten-ide.html


emcc -c src/sdl_1_2_sample.cpp -o obj/sdl_1_2_sample.o
emcc obj/sdl_1_2_sample.o -o public/sdl_1_2_sample.html

// una sola linea
EMCC_DEBUG=1 emcc src/sdl_1_2_sample.cpp -o public/sdl_1_2_sample.html


- Download repository
- Set the folder name to the desired project name
- Open folder with Visual Studio Code
- Press F1, then execute `Dev Containers: Reopen in container`
- Wait for install container and recomended extensions
- Execute build task Ctrl + Shift + B (Build)
- All ready to develop your project

(optional for build tap file with loader + screen + code)

- Press F1 and select 'Run Task' -> 'Build with PASMO'
- use build/main-output.tap in any emulator

## Remarks

Container name is created based in folder project name, you can create other folders based on this repository with other names for more projects.
The first time it download docker hub image with the sjasmplus sources from 2023-009-05 and PASMO 0.5.5

Source code sample is from Juan Antonio Rubio García book 'Ensamblador para ZX Spectrum: ¿Hacemos un juego?'

www: <https://espamatica.com/>

## Links of interest

- emscripten: <https://emscripten.org/index.html>

- My Github account: <https://github.com/dgzornoza>

## Releases

### 1.0.0

Initial release emscripten 3.1.59

**Enjoy!**
