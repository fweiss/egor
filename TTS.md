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