joshua riek
ubuntu-24.04-preinstalled-server-arm64-orangepi-5-pro.img.xz

- original ubuntu/ubuntu
- changed ubuntu/orangepi
- RKNPU driver: v0.9.7
-  6.1.0-1025-rockchip
--cc --version 13.3.0

> orangepi-config was not included. reason being that the old tool
> was for a fork of armbian https://github.com/Joshua-Riek/ubuntu-rockchip/issues/530

- ``python --version`` = not found
- ``python3 --version`` = 3.12.3

- ``sudo apt-get update``
- ``sudo apt-get install libxslt1-dev zlib1g-dev libglib2.0 libsm6 libgl1-mesa-glx libprotobuf-dev gcc`` ???
- ``git clone https://github.com/airockchip/rknn-toolkit2 -b v1.5.2``

skip to 3.39.3.1

- ``wget https://huggingface.co/c01zaut/dolphin-2.9.2-qwen2-7b-rk3588-1.1.1/resolve/main/dolphin-2.9.2-qwen2-7b-rk3588-w8a8-opt-0-hybrid-ratio-0.0.rkllm``

- ``sudo apt-get install cmake``
- ``sudo apt-get update && sudo apt-get install build-essential``

- ``git clone https://github.com/airockchip/rknn-llm.git``
- ``cd ~/rknn-llm/examples/rkllm_api_demo``
-- ``ln ~/dol... llm
- ``mkdir build``
- ``cd build``
-- ``cmake ..``
- ``make``

> uint8 does not name a type in rkllm.h, change to unsigned char

- `` ./llm_demo llm 1024 1024
- how many days in a year
- what does the christian name frank mean

> on the latter it repeats itself, had to ctrl-c

- `` ./llm_demo llm 4096 4096

> hangs after init, no it just takes a long time, but also repeats
> maybe it's the model

Performance is pretty good except for init. But it starts response right away
and outputd at the rate of about 3 words pre second. Thats running off an
SDard.

> the chip does get pretty hot maybe 67 c




