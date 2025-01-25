# Models

## simple test
- build ``llm_demo`` with cmake/make
- download

``https://huggingface.co/c01zaut/dolphin-2.9.2-qwen2-7b-rk3588-1.1.1/blob/main/dolphin-2.9.2-qwen2-7b-rk3588-w8a8-opt-0-hybrid-ratio-0.0.rkllm``

- ``ulimit -HSn 102400``
- ``orangepi@orangepi5pro:~/rknn-llm/examples/rkllm_api_demo/build$ ./llm_demo /tmp/dolphin-2.9.2-qwen2-7b-rk3588-w8a8-opt-0-hybrid-ratio-0.0.rkllm 4096 4096``
- segmentation fault

```

orangepi@orangepi5pro:~/rknn-llm/examples/rkllm_api_demo/build$ ./llm_demo llm 1024 1024
rkllm init start
W rkllm: Warning: Your rknpu driver version is too low, please upgrade to 0.9.7.

I rkllm: rkllm-runtime version: 1.1.4, rknpu driver version: 0.9.6, platform: RK3588

E RKNN: [00:27:50.144] failed to allocate handle, ret: -1, errno: 14, errstr: Bad address
E RKNN: [00:27:50.144] failed to malloc npu memory, size: 4059037696, flags: 0x2
E RKNN: [00:27:50.149] load model file error!
rknn_init fail! ret=-1
rkllm init success
```
