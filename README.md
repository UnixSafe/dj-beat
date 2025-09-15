
<div align="center"><img style="display:inline-block" width='150' src="./assets/logo.png"/><p>
    <span style="font-size: 14px">Version: 0.5.0</span><br>
    <span>"A Simple Beat Time Marks Generator"</span><br>
    <span style="font-size: 12px;color= #95dafc">-- Created by <a>Kevin T. Lee</a> --</span>
    </p>
    <a href="./LICENSE"><img alt="MIT" src="https://img.shields.io/github/license/mashape/apistatus.svg?&url=LICENSE&longCache=true&style=for-the-badge"></a>
        <a href="http://lidengju.com"><img alt="Code" src="https://img.shields.io/badge/Code%20with-Love-red.svg?longCache=true&style=for-the-badge"></a>
    <a href="https://github.com/kevinleeex/dj-beat/"><img alt="Version" src="https://img.shields.io/badge/Version-0.5.0-blue.svg?longCache=true&style=for-the-badge"></a>
</div>

# DJ-beat

Dj-beat is an easy-to-use generator that automatically detects audio beats and generates time markers for FCPX and Adobe Premiere*.

> P.S. why the tool is called DJ beat? DJ is from my chinese first name of course...

## :headphones: Overview

A good music-driven video requires a perfect combination of sound and picture. Think about you're using the video editing software like Final Cut Pro X, you need to manually mark the place on the soundtrack that denotes the beat. Now, you have the **DJ-beat**, which can help you handle such a boring thing, mark, mark, mark...While it may do better than us. 

Dj-beat is a simple tool developed based on python3 and audio ML libraries, supports operating via command line and graphical interface*. As of 0.5.0 it is Apple Silicon (arm64) friendly: it uses librosa by default for beat tracking and will use madmom when available for parity with older versions.

Learn more about **beat tracking**:

- for Chinese readers click [here](https://github.com/kevinleeex/dj-beat/blob/master/post/beat_tracking_in_mir.ipynb). 

- for English readers click [here](https://www.analyticsvidhya.com/blog/2018/02/audio-beat-tracking-for-music-information-retrieval/).

### Preview

![preview](./assets/preview.png)

## :beer: Installation 
### Requirements (0.5.0+)
- numpy>=1.22
- scipy>=1.10
- librosa>=0.10
- audioread>=3.0.0
- tqdm>=4.60
- pyfiglet>=0.8
- urllib3>=1.26

Optional for legacy accuracy parity:
- madmom (if installed, will be used automatically)

```bash
cd ./djbeat
pip install -r requirements.txt
```

### Use pip (Recommended)
> make sure you have add your virtual environment **bin** path to the PATH, thus to use the command line tool.
 
```bash
pip install dj-beat
```

### Locally

```bash
$ git clone https://github.com/kevinleeex/dj-beat.git
$ cd dj-beat
$ pip install .
```

## :star2: Usage

### Command-Line Tool

```bash
$ djbeat -f ./test/treasure-trimed.wav -r 30
```

Supported input formats: wav, mp3, m4a
Note: On some systems, m4a decoding requires a system codec (e.g., ffmpeg). On macOS, CoreAudio usually handles it out of the box.

#### Arguments

```
-h, --help           Display this help message and exit.
-v,                  Display the version.
-V,                  Display the beat time list in terminal.
-p, --platform       The platform, fcpx or pre, default='fcpx'.
-f, --filepath       The filepath of the input audio.
-s, --fps FPS        The sample rate of the music, a integer number, default='100'.
-r, --frame_rate     The frame rate of your video setting, choose from {23.98,24,25,29.97,30,50,60}, default='30'.
```

### Graphic User Interface

[TO-DO]

## :heart: Support me

If this project helps you, you can support me to do better.  
<a href="https://paypal.me/kevinleeex"><img alt="Coffee" src="https://img.shields.io/badge/PayPal_me_a-Coffee-7A501E.svg?longCache=true&style=for-the-badge"></a>

Or click <a href="http://lidengju.com/donate">Donete me</a> with Wechat or Alipay

## :zzz: TO-DO

- [x] Distribution
- [ ] Support the GUI
- [ ] Support generate marks for PRE
- [ ] Model research about beat tracking


## :paperclip: License

Copyright © 2018 [Kevin T. Lee](http://lidengju.com). All rights reserved. 

The project is licensed under the MIT license. See [LICENSE](./LICENSE) for more details.
