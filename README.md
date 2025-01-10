# S2SLLM on Orange Pi 5
A speech-to-speech LLM on Orange Pi 5 with RK3588

## Goals
- run a modest LLM locally
- use the RK3588 NPU
- form prompts with speech to text
- present responses with text to speech
- assess performance

> Because of resource constraints, try using usage-specific models which use less
> memory and provide higher precision for a limited subject area.

## Subject areas
- zoo: describe animals and their care, recommend exhibits
- chill chatbot: provides personal attention and has a friendly personality
- jokester: peppers a casual conversation with light-hearted humour
- nerd: stimulates curiousity on science topics
- nanny: sympathetic and provides tips for good behavior
- guidance counselor: conversations like "what do you want to be when you grow up"
- math tutor: conversations about math with quizzes

> These can be stored locally and updated from online.

## Dev board
Orange Pi 8 Plus
- 16 GB
- RK3588S
- quad-core A76 + quad-core A55
- 400 Mhz/2.4 GHz
- Mali-G610 GPU
- 16 GB embedded NPU supports INT4/INT8/INT16 mixed computing
- up to 6TOPS
- TDP 8 W, peak 12 W

## NPU
- max 6 tops
- 3 cores
- integer 4, integer 8, integer 16, float 16, Bfloat 16 and tf32 operation
- Embedded 384KBx3 internal buffer

## RK3588 vs RK3588S
- RK3588: more I/Os, PCIe 3.0, 20 W
- RK3588S: lower power, about 80%

## Links and references
[How To RUN ChatGPT Like LLMs On Raspberry Pi 5 With OLLAMA (TinyLLaMA, PHI & More)](https://www.youtube.com/watch?v=P7BcpLU-PC4)

[Another how to run LLM on RK3588](https://www.youtube.com/watch?v=sTHNZZP0S3E)
