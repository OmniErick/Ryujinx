
<h1 align="center">
  <br>
  <a href="https://ryujinx.org/"><img src="https://i.imgur.com/WcCj6Rt.png" alt="Ryujinx" width="150"></a>
  <br>
  <b>Ryujinx</b>
  <br>
  <sub><sup><b>(REE-YOU-JINX)</b></sup></sub>
  <br>

</h1>

<p align="center">
    <a href="https://github.com/Ryujinx/Ryujinx/actions/workflows/release.yml">
        <img src="https://github.com/Ryujinx/Ryujinx/actions/workflows/release.yml/badge.svg"
            alt="">
    </a>
        <img src="https://img.shields.io/discord/410208534861447168?color=5865F2&label=Ryujinx&logo=discord&logoColor=white"
            alt="Discord">
    </a>
    <br>
    <br>
    <img src="https://raw.githubusercontent.com/Ryujinx/Ryujinx-Website/master/public/assets/images/shell.png">
</p>

<h5 align="center">

</h5>

## Compatibility

As of April 2023, Ryujinx has been tested on approximately 4,050 titles; over 4,000 boot past menus and into gameplay, with roughly 3,400 of those being considered playable.
You can check out the compatibility list [here](https://github.com/Ryujinx/Ryujinx-Games-List/issues). Anyone is free to submit a new game test or update an existing game test entry; simply follow the new issue template and testing guidelines, or post as a reply to the applicable game issue. Use the search function to see if a game has been tested already!

## Usage

To run this emulator, your PC must be equipped with at least 8GiB of RAM; failing to meet this requirement may result in a poor gameplay experience or unexpected crashes.

See our [Setup & Configuration Guide](https://github.com/Ryujinx/Ryujinx/wiki/Ryujinx-Setup-&-Configuration-Guide) on how to set up the emulator.

For our Local Wireless and LAN builds, see our [Multiplayer: Local Play/Local Wireless Guide
](https://github.com/Ryujinx/Ryujinx/wiki/Multiplayer-(LDN-Local-Wireless)-Guide).

Avaldsafass
## Building

If you wish to build the emulator yourself, follow these steps:

### Step 1
Install the X64 version of [.NET 7.0 (or higher) SDK](https://dotnet.microsoft.com/download/dotnet/7.0).

### Step 2
Either use `git clone https://github.com/Ryujinx/Ryujinx` on the command line to clone the repository or use Code --> Download zip button to get the files.sfdgsRelease -o build`
the built files will be found in the newly created build directory.

Ryujinx system files are stored in the `Ryujinx` folder. This folder is located in the user folder, which can be accessed by clicking `Open Ryujinx Folder` under the File menu in the GUI.


## Features

 - **Audio**

   Audio output is entirely supported, audio input (microphone) isn't supported. We use C# wrappers for [OpenAL](https://openal-soft.org/), and [SDL2](https://www.libsdl.org/) & [libsoundio](http://libsound.io/) as fallbacks.

- **CPU**

  The CPU emulator, ARMeilleure, emulates an ARMv8 CPU and currently has support for most 64-bit ARMv8 and some of the ARMv7 (and older) instructions, including partial 32-bit support. It translates the ARM code to a custom IR, performs a few optimizations, and turns that into x86 code.
  There are three memory manager options available depending on the user's preference, leveraging both software-based (slower) and host-mapped modes (much faster). The fastest option (host, unchecked) is set by default.
  Ryujinx also features an optional Profiled Persistent Translation Cache, which essentially caches translated functions so that they do not need to be translated every time the game loads. The net result is a significant reduction in load times (the amount of time between launching a game and arriving at the title screen) for nearly every game. NOTE: this feature is enabled by default in the Options menu > System tab. You must launch the sgfse GUI.

- **Input**

   We currently have support for keyboard, mouse, touch input, JoyCon input support, and nearly all controllers. Motion controls are natively supported in most cases; for dual-JoyCon motion support, DS4Windows or BetterJoy are currently required.
   In all scenarios, you can set up everything inside the input configuration menu.

- **DLC & Modifications**

   Ryujinx is able to manage add-on content/downloadable content through the GUI. Mods (romfs, exefs, and runtime mods such as cheats) are also supported; the GUI contains a shortcut to open the respective mods folder for a particular game.
gsdf

All developers working on the project do so in their free time, but the project has several expenses:
* Hackable Nintendo Switch consoles to reverse-engineer the hardware
* Additional computer hardware for testing purposes (e.g. GPUs to diagnose graphical bugs, etc.)
* Licenses for various software development tools (e.g. Jetbrains, IDA)
* Web hosting and infrastructure maintenance (e.g. LDN servers)

All funds received through Patreon are considered a donation to support the project. Patrons receive early access to progress reports and exclusive access to developer interviews.

## License

This software is licensed under the terms of the <a href="https://github.com/Ryujinx/Ryujinx/blob/master/LICENSE.txt" target="_blank">MIT license.</a></i><br />
This project makes use of code authored by the libvpx project, licensed under BSD and the ffmpeg project, licensed under LGPLv3.
See [LICENSE.txt](LICENSE.txt) and [THIRDPARTY.md](distribution/legal/THIRDPARTY.md) for more details.
## Credits

- [LibHac](https://github.com/Thealexbarney/LibHac) is used for our file-system.
- [AmiiboAPI](https://www.amiiboapi.com) is used in our Amiibo emulation.
