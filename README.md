# Deep Learning Image Caption Generator
> ## Deep CNN-LSTM for Generating Image Descriptions :smiling_imp:
**Key words**: Image captioning, image description generator, explain image, merge model, deep learning, long-short term memory, recurrent neural network, convolutional neural network, word by word, word embeding, bleu score.

**Related works**: Deep model for computer vision and natural language, Image-sentence retrieval, Generating novel sentence descriptions for images.

#### Abstract
Image captioning is a very interesting problem in machine learning. With the development of deep neural network, deep learning approach is the state of the art of this problem. The main mission of image captioning is to automatically generate an image's description, which requires our understanding about content of images. In the past, there are some end-to-end models which were introduced such as: GoogleNIC ([show and tell](https://arxiv.org/pdf/1411.4555.pdf)), MontrealNIC ([show attend and tell](https://arxiv.org/pdf/1502.03044.pdf)), [LRCN](https://arxiv.org/pdf/1411.4389.pdf), [mRNN](https://arxiv.org/pdf/1410.1090.pdf), they are called inject-model with idea is give image feature throught RNN. In 2017, Marc Tanti, et al. introduce their [paper](https://arxiv.org/pdf/1708.02043.pdf) **What is the Role of Recurrent Neural Networks (RNNs) in an Image Caption Generator?** with merge-model. The main idea of this model is separate CNN and RNN, with only merge their ouput at the end and predicted by softmax layer. Base on it, we develop our model to generate image caption. 

### I. Main Idea:
* Combine ConvNet with LSTM
* Deep ConvNet as image encoder
* Language LSTM as text encoder
* Fully connected layer as decoder
* End-to-end model I -> S
* Maximize P(S|I)

### II. Dataset: 
[Flickr 8k](https://forms.illinois.edu/sec/1713398), train/val/test 6:1:1.

The definitive description of the dataset is in the paper “Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics” from 2013.

The authors describe the dataset as follows:

*"We introduce a new benchmark collection for sentence-based image description and search, consisting of 8,000 images that are each paired with five different captions which provide clear descriptions of the salient entities and events … The images were chosen from six different Flickr groups, and tend not to contain any well-known people or locations, but were manually selected to depict a variety of scenes and situations."*

— [Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics, 2013](https://jair.org/index.php/jair/article/view/10833/25854).

### III. Baseline Model:

<p align="center">
  <img src="https://i.imgur.com/rDGYTBH.png" />
</p>

### IV. Implement code:
1. Load images and extract feature: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model-resnet50)
2. Load text data: [kaggle-kernel](https://www.kaggle.com/damminhtien/text-data-exploxe)
3. Develop model and training: [kaggle-kernel](https://www.kaggle.com/damminhtien/visualization-development-model-resnet50)
4. Evaluation model: [kaggle-kernel](https://www.kaggle.com/damminhtien/evaluate-model)
5. Generator caption for new images: [kaggle-kernel](https://www.kaggle.com/damminhtien/generation-caption-for-new-image)

### V. Tuning hyperparameters:
> ### Encoder ConvNet:
* VGG16
* **Resnet50**
* Densenet121
* Inceptionv3

> ### Optimizer
* **Adam**: 
* Nadam: 
* RMSprop: 
* Sgd:

### VI. Evaluation and result:
> **We use BLEU-score which is evaluate metric:**
+ BLEU-1: 0.542805
+ BLEU-2: 0.301714
+ BLEU-3: 0.207351
+ BLEU-4: 0.095704

> **Caption of new images:**
<p align="center">
  <img src="https://i.imgur.com/uFE7Hkn.png" />
</p>

> ### Report comming soon!

### Reference
+ [[1](https://arxiv.org/pdf/1703.09137.pdf)] Marc Tanti, Albert Gatt. Where to put the Image in an Image Caption Generator. arXiv preprint arXiv:1703.09137, 2018.
+ [[3](https://arxiv.org/pdf/1708.02043.pdf)]Marc Tanti, Albert Gatt, Kenneth P. Camilleri. What is the Role of Recurrent Neural Networks (RNNs) in an Image Caption Generator? arXiv preprint arXiv:1708.02043, 2017.
+ [[3](https://arxiv.org/pdf/1502.03044.pdf)] Kelvin Xu, Jimmy Lei Ba, Ryan Kiros, Kyunghyun Cho, Aaron Courville, Ruslan Salakhutdinov, Richard S. Zemel, Yoshua Bengio. Show, Attend and Tell: Neural Image Caption Generation with Visual Attention. arXiv preprint arXiv:1502.03044, 2016.
+ [[4](https://cs.stanford.edu/people/karpathy/deepimagesent/)] Andrej Karpathy, Li Fei-Fei Deep Visual-Semantic Alignments for Generating Image Descriptions. arXiv preprint arXiv:1412.2306, 2015.
+ [[5](https://arxiv.org/pdf/1411.4555.pdf)] O. Vinyals, A. Toshev, S. Bengio, and D. Erhan. Show and tell: A neural image caption generator. arXiv preprint arXiv:1411.4555, 2014.
+ [[6](https://vision.cornell.edu/se3/wp-content/uploads/2018/03/1501.pdf)] Yin Cui, Guandao Yang, Andreas Veit, Xun Huang, Serge Belongie. Learning to Evaluate Image Captioning.
+ [[7](https://arxiv.org/pdf/1410.1090.pdf)] Junhua Mao, Wei Xu, Yi Yang, Jiang Wang, Alan L. Yuille. Explain Images with Multimodal Recurrent Neural Networks. arXiv preprint arXiv:1410.1090, 2014..
+ [[8](https://arxiv.org/pdf/1411.4389.pdf)] Xinlei Chen, C. Lawrence Zitnick. Learning a Recurrent Visual Representation for Image Caption Generation. arXiv preprint arXiv:1411.5654, 2016.


> ### Happy trainning :tada: and please vote :star: if it help! 
