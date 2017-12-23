
# Required things

 * [SDL2 2.0.0+ Development package](https://www.libsdl.org/release/SDL2-devel-2.0.7-VC.zip) (Windows) / `apt-get install libsdl2-dev`
 * [VLC with libVLC 1.1.1+](http://mirror.atomki.hu/videolan/vlc/2.2.8/win32/vlc-2.2.8-win32.7z) (only 7z version have `sdk` folder) (Windows) / `apt-get install libvlc-dev libvlccore-dev vlc`

# Preparation

Windows:
* Copy contents of SDL2 Development package to `vendor` folder and rename it to `SDL2`
* Copy contents of VLC package from folder `sdk` to folder `vendor` and rename it to `vlc`

# Building

```bash
mkdir build
cmake ../
cmake --build .
```
For Windows:
* Copy from VLC package `libvlc.dll`, `libvlccore.dll` and `plugins` folder into `build/Debug`

For Linux:
```
copy -R /usr/lib/vlc/plugins/ .
```

# Running
```bash
sdl2-libvlc <filename>
```
And there you go!

![alt text](https://cdn.marekkraus.sk/2017-12/sdl2-libvlc_2017-12-23_12-00-51.png "Windows libvlc sdl2 build")
![alt text](https://cdn.marekkraus.sk/2017-12/vmware_2017-12-23_12-00-18.png "Linux libvlc sdl2 build")

