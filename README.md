# PaliGemma Inference Comparison: vLLM vs Standard Transformers
This repository contains two Jupyter notebooks comparing PaliGemma inference performance using standard Transformers library versus vLLM optimization framework.

## 📚 Notebooks

paligemma_without_vllm_inference.ipynb - Standard Transformers implementation <br>
paligemma_vllm_inference.ipynb - vLLM optimized implementation

**vLLM provides 35% faster inference(based on the example chosen in the notebook) with identical model quality, making it the preferred choice for production deployments where the initialization overhead can be amortized across multiple inference requests**

## vLLM Requirements without Flash Attention
```
## Essential dependencies only

### Core PyTorch with CUDA 12.1 support
torch>=2.0.0,<3.0.0
torchvision>=0.15.0
torchaudio>=2.0.0

### vLLM core (install without dependencies to avoid flash-attn)
vllm>=0.2.7

### Transformers and model handling
transformers>=4.36.0,<5.0.0
tokenizers>=0.15.0
accelerate>=0.24.0

### Hugging Face integration
huggingface-hub>=0.19.0
safetensors>=0.4.0

### Image processing for multimodal models
pillow>=9.0.0

### HTTP and utilities
requests>=2.28.0

### Alternative attention mechanism (faster to install than flash-attn)
xformers>=0.0.22

### Numerical computing
numpy>=1.24.0
```
