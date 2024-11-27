---
aliases:
  - template1
up:
  - [[AI-concept]]
---
up:  [[AI-concept#Quantization]]  ; see: [[Quantization-mlops|Quantization (MLOps)]]
# Quantization
Техника уменьшения точности весов модели
 [[Quantization-mlops|Quantization (MLOps)]] - конкретные рецепты, опции CLI

Quantization is the technique of lowering the precision of the model’s weights and/or activations.. Convert the high precision numbers, typically used in neural networks, to lower precision formats. For example, 32-bit floating point could be converted to 16-bit. (from [[#AI Building a LLM but want to keep computational costs down? Deep Dive into Quantization (article)]])



##### Quantization is method of optimization
See: [[#Quantization]]
### Articles / Info
##### AI: Building a LLM but want to keep computational costs down? Deep Dive into Quantization (article)
https://adaptalent.com/ai-deep-dive-into-quantization/

The range of values is divided into equal-sized intervals. This is simple and efficient but may not be optimal for all data distributions.
==Non-Uniform Quantization== : Intervals are varying sizes, often based on the data distribution, providing better precision for more frequently occurring values.
==Post-Training Quantization== : Quantization is applied after the model has been trained by reducing the precision of weights and/or activations.
==Dynamic Quantization== : Only weights are quantized, while activations are computed at higher precision and quantized dynamically during inference.
==Static Quantization== : Both weights and activations are quantized. A calibration step using a representative dataset is performed to determine the optimal quantization ranges.
==Quantization-Aware Training (QAT)== : In this method, the model is trained with quantization in mind, simulating low-precision arithmetic during the forward and backward  passes to adapt the model to the quantized domain.

##### What is quantization?
https://www.ibm.com/think/topics/quantization

##### Absolute max quantization
To calculate the mapping between the floating-point number and its corresponding INT8 number in absolute max quantization, you have to first divide by the absolute maximum value of the tensor and then multiply by the total range of the data type.

For example, we will apply the absolute max quantization algorithm to the following vector [1.6, -0.7, -3.4, 1.7, -2.9, 0.5, 2.3, 6.2]. You extract the absolute maximum of it, which is 6.2 in this case. INT8 has a range of [-127, 127], so we divide 127 by 6.2 and obtain 20.5 for the scaling factor. Therefore, multiplying the original vector by it gives the quantized data vector [33, -14, -70, 35, -59, 10, 47, 127]. Due to these numbers being rounded, there will be some precision loss. 5  

##### Affine quantization
To implement the affine quantization algorithm, we will define our range of 32-bit floating point values as [a, b]. The affine quantization algorithm is as follows:

𝑥𝑞 = _round ((1/𝑆)𝑥+𝑍)_

**- 𝑥𝑞** is the quantized INT8 value that corresponds to the 32-bit floating point value x.

**- S** is an FP32 scaling factor and is a positive 32-bit floating point.

**- Z** is the zero-point. This will be the INT8 value that corresponds with zero in the 32-bit floating point field.

_**- round**_ is referring to the rounding of the resulting value to the closest integer.

To next establish the [min, max] of our 32-bit floating point values we need to take into account any outliers. Overlooking these outliers can lead to them being mapped as either min or max and potentially skewing the accuracy of the quantized model. To counter this, the model can be quantized in blocks. The weights can be broken up into groups of either 64 or 128. Then these groups are quantized to account for outliers and minimize the risk of lowered precision. 6

##### Efficient LLM Training: Memory & Compute Optimization (article) 
[[ELLMTrai-MCOptimization@a#1. Quantization|Efficient LLM Training: Memory & Compute Optimization (article) -> 1. Quantization]]




