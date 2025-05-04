# Runs RKLLM model on Raxda Rock 5T NPU
This repo tries to make RKNN LLM usage easier for people who don't want to read through Rockchip's docs.

Main repo is a fork of https://github.com/Pelochus/ezrknn-llm, with fixes to enable stable inference and deployment.

## Requirements
Keep in mind this repo is focused for:
- RKLLM V1.1.2
- High-end Rockchip SoCs, mainly the RK3588
- Linux, not Android
- Linux kernels from Rockchip (as of writing 5.10 and 6.1 from Rockchip should work, if your board has one of these it will very likely be Rockchip's kernel)
- Using https://github.com/Lemon1151/ubuntu-rockchip/releases as the OS

## Quick Install
First clone the repo:

```bash
git clone https://github.com/Pelochus/ezrknn-llm
```

Then run:

```bash
cd ezrknn-llm && bash install.sh
```

## Test
Run (assuming you are on the folder where your `.rkllm` file is located):

```bash
rkllm Llama-3.2-1B-rk3588-w8a8-opt-1-hybrid-ratio-0.0.rkllm 100 100 # Or any other model you like
```

## Fixing hallucinating LLMs
Check this reddit post if you LLM seems to be responding garbage:

https://www.reddit.com/r/RockchipNPU/comments/1cpngku/rknnllm_v101_lets_talk_about_converting_and/





# Support Models
Link to working Huggingface collection (1.1.2 compatible models): https://huggingface.co/collections/ThomasTheMaker/a-rock-and-a-hard-place-681522c99d9b100d11cfe4e7

# Model Performance Benchmark

Link to active performance testing: https://halved-meat-bd8.notion.site/Raxda-Rock-5T-1e8c100a4313809eaa51cb76486a3658


- This performance data were collected based on the maximum CPU and NPU frequencies of each platform with version 1.1.2. 
- The script for setting the frequencies is located in the scripts directory.
