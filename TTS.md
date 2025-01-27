# Links
- https://github.com/rhasspy/piper
- https://github.com/neonbjb/tortoise-tts
- https://github.com/coqui-ai/TTS
- https://github.com/snakers4/silero-models

## Piper
- run with .py or as binary

## play
Play is part of sox

- ``sudo apt install sox``

-- ``aplay -l``
- ES8388
- ``set AUDIODEV=/dev/dsp2``

``aplay -D hw:2,0 /usr/share/sounds/alsa/audio.wav`` WORKS

``aplay -D hw:2,0 ~welcom.wav``
> Playing WAVE 'welcome.wav' : Signed 16 bit Little Endian, Rate 22050 Hz, Mono
> aplay: set_params:1349: Channels count non available
> The welcome.wav does play on Windows

cases:
> aplay -D hw:2,0 /usr/share/sounds/alsa/audio.wav
> Playing WAVE '/usr/share/sounds/alsa/audio.wav' : Signed 16 bit Little Endian, Rate 44100 Hz, Stereo

> aplay -D hw:2,0 ./welcome.wav
> Playing WAVE './welcome.wav' : Signed 16 bit Little Endian, Rate 22050 Hz, Mono
> aplay: set_params:1349: Channels count non available

## OPI5 Pro hardware
just puttin this here for a while maybe

- chip: ES8388
- headphone/mic jack
- on board 

## output signal path
- to jack via n-channel mosfet WNM2016-3/TR
- mosfet gate connected to PHONE_CTL via 200K
- mosfet input is via drain
- outpput from chip ROUT1 and LOUT1
- return is GND

> The chip ROUT2 and LOUT2 are not connected.
> Looks like an I2S breakout witll be needed.


## Links and references
[Waveshare audio hat for RPI](https://www.waveshare.com/wiki/WM8960_Audio_HAT) ~$15-20

