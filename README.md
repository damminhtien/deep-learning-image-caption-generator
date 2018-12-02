# Deep Learning Image Caption Generator
> ## Deep Visual-Semantic Alignments for Generating Image Descriptions :smiling_imp:

## Main Idea:
* Combine CNN with LSTM
* Deep CNN as encoder
* Language LSTM as decoder
* End-to-end model I -> S
* Maximize P(S|I)

## Tuning:
> ### Encoder CNN:
* VGG16: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model)
* Resnet50: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model-resnet50)
* **Densenet121**: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model-densenet121)
* Inceptionv3: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model-inceptionv3)

Dataset: [Flickr 8k](https://forms.illinois.edu/sec/1713398)

1. Load images and extract feature by VGG16: [kaggle-kernel](https://www.kaggle.com/damminhtien/flirck-8k-dataset-explore-image)
2. Load text data: [kaggle-kernel](https://www.kaggle.com/damminhtien/text-data-exploxe)
3. Develop model and training: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model)
4. Evaluation model: [kaggle-kernel](https://www.kaggle.com/damminhtien/evaluate-model)
5. Generator caption for new images: [kaggle-kernel](https://www.kaggle.com/damminhtien/generation-caption-for-new-image)

## Model:

<p align="center">
  <img src="https://i.imgur.com/1DxxbyK.png" />
</p>

## Result:

BLEU-1: 0.506709

BLEU-2: 0.265901

BLEU-3: 0.182500

BLEU-4: 0.085222

<p align="center">
  <img src="https://i.imgur.com/uFE7Hkn.png" />
</p>

> ### Report comming soon!
