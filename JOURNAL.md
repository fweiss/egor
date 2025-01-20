# Setup OPI5 Pro
Follow the instructions in the User Manual

## TF Card
- go to ``https://drive.google.com/drive/folders/11tj_ivEBwvJx4vdNtK91YQeGOKDC4JNy``
- download ``Orangepi5pro_1.0.6_ubuntu_jammy_server_linux6.1.43``
- unzip it
- flash to TF Card with balenaEtcher on windows

## Start the OPI5 Pro and lgoin shell
This is from section 2.19

> Assimung that just TF Card is used for boot media

- insert TF Card
- connect ethernet
- connect 5V power

> Red light, then red + double flash green

- connect via ssh
- login orangepi/orangepi
See section 3.4.1

> Took me about 45 min to get ssh, much was skipping over the User Manual material

> lsb_release -a: Ubuntu 22.04.5 LTS jammy
> uname -a: 6.1.43-rockchip-rk3588

Upgrade linux: ``sudo apt upgrade``

## LED excercise
``cd /sys/class/leds/blue_led``
> ``sudo echo heartbeat > trigger`` permission denied

## Using NPU and running LLM
This is in sections 3.37to 3.39

- ``sudo apt-get update``
- ``sudo apt-get install libxslt1-dev zlib1g-dev libglib2.0 libsm6 libgl1-mesa-glx libprotobuf-dev gcc``

> Skipping section 3.37.3.1 as it pertains to CV

> Section 39.1 starts getting into LLM.
> Section 3.39.4.2.1 gets into inference

Goal is to run ``rkllm init start``

## Building RKLLM Toolkit Environment
> section 3.39.3.1

### installing anaconda
- ``git clone https://github.com/airockchip/rknn-llm.git``
- ``wget -c https://mirrors.bfsu.edu.cn/github-release/conda-forge/miniforge/LatestRelease/Miniforge3-Linux-x86_64.sh``
- chmod 777 Miniforge3-Linux-x86_64.sh
- bash Miniforge3-Linux-x86_64.sh

> but miniforge3 is an x86_64 script! line 376 /home/orangepi/miniforge3/_conda
> cannot execute binary file
> FIX: use Miniforge3-Linux-aarch64.sh

- ``source ~/miniforge3/bin/activate``
- ``conda create -n RKLLM-Toolkit python=3.8``
- ``conda activate RKLLM-Toolkit``
- ``pip3 install rknn-llm/rkllm-toolkit/packages/rkllm_toolkit-1.0.1-cp38-cp38-linux_aarch64.whl``

> that doesn't work, 1.0.1 -> 1.4.4, and only x86_64

## altrnate rkllm
- ``cd``
- ``https://github.com/Rockchip-Linux/rklmm.git``
