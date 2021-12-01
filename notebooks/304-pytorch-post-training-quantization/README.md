# Optimizing PyTorch models with Neural Network Compression Framework of OpenVINO by 8-bit quantization.

This tutorial demonstrates how to use [NNCF](https://github.com/openvinotoolkit/nncf) 8-bit quantization in post-training mode (without the fine-tuning pipeline) to optimize a 
[PyTorch](https://pytorch.org/) model for the high-speed inference via [OpenVINO Toolkit](https://docs.openvinotoolkit.org/). 
For more advanced usage refer to these [examples](https://github.com/openvinotoolkit/nncf/tree/develop/examples).

This notebook is based on 'ImageNet training in PyTorch' [example](https://github.com/pytorch/examples/blob/master/imagenet/main.py).
To make downloading and validating fast, we use an already pretrained [ResNet-50](https://arxiv.org/abs/1512.03385) model on the 
[Tiny ImageNet](http://cs231n.stanford.edu/reports/2015/pdfs/leonyao_final.pdf) dataset.

It consists of the following steps:
- Transform the original FP32 model to INT8
- Export optimized and original models to ONNX
- Compare the perfomance of the obtained FP32 and INT8 ONNXs

## Installation Instructions

If you have not done so already, please follow the [Installation Guide](../../README.md) to install all required dependencies.