# 🖼️ LLaVA Local Vision Tower Support ✨

This repository extends the original LLaVA model with the capability to load vision tower models from local paths.

## ✅ Features

- Added support for loading vision tower models from local paths in `llava/model/builder.py`
- Provided a simplified `inference.py` script for easy model inference

## 🚀 Usage

To use the model with a local vision tower:

```bash
CUDA_VISIBLE_DEVICES=0 python inference.py \
    --model-path /path/to/your/llava-next-interleave-qwen-7b \
    --images image1.jpg \
    --prompt "Describe this image in detail." \
    --vision-tower-path /path/to/your/siglip-so400m-patch14-384
```

## 🔧 Installation

```bash
conda create -n llava-next-inference python=3.10 -y
conda activate llava-next-inference
pip install --upgrade pip  # Enable PEP 660 support.
pip install -e ".[train]"
```

## 🔍 Implementation Details

The key modification is in `llava/model/builder.py`, where we've added functionality to load vision tower models from local paths instead of only from Hugging Face's model hub.

## 🙏 Acknowledgements

This project builds upon the [LLaVA](https://github.com/haotian-liu/LLaVA) project.
