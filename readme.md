# CLIPxGPT Captioner

## Description

**`CLIPxGPT Captioner`** is Image Captioning Model based on [OpenAI's](https://openai.com/) [CLIP](https://openai.com/blog/clip/) and [GPT-2](https://openai.com/blog/better-language-models/). The Model uses a Mapping module to "translate" CLIP embeddings ​​to GPT-2. The model is trained on the [Flickr30k](https://shannon.cs.illinois.edu/DenotationGraph/) dataset, downloaded from [Kaggle](https://www.kaggle.com/datasets/hsankesara/flickr-image-dataset)

**The goal** of the project was to find out about the possibility of CLIP + GPT-2 connection and to check whether, with a relatively short training time and a small dataset, the model will be able to recognize situations in the pictures. The model achieved satisfactory results.

The Model uses prefixes as in the [ClipCap](https://arxiv.org/abs/2111.09734) paper. In my original idea, the length of the prefix was 1, but after reading publication, the length of the prefix was changed to 4, thanks to which the performance increased.

The Model was trained with a frozen CLIP, a fully trained Mapping Module (5-6x Transformer Encoder Layers) and with partially frozen GPT-2 (the first and last 14 layers were trained).

The training process was carried out using the [Kaggle](https://www.kaggle.com/) P100 GPU.

## Example results

![Example1](./examples/23012796-RS.jpg)
![Example2](./examples/36979-RS.jpg)
![Example3](./examples/89407459-RL.jpg)

