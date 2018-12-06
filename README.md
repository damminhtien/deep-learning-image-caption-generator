# Deep Learning Image Caption Generator
> ## Deep CNN-LSTM for Generating Image Descriptions :smiling_imp:

#### Abstract
Image Captioning is a very interesting problem in machine learning. With the development of deep neural network, deep learning approach is the state of the art of this problem. The main mission of image captioning is to automatically generate an image's description, which requires our understanding about content of images. There are some end-to-end models which were introduced such as: GoogleNIC (show and tell), MontrealNIC (show attend and tell),  LRCN, mRNN,... Simplified from GoogleNIC, our model uses ConvNet as the image encoder and LSTM as the language decoder with few layers, which reduces computational cost compared with above models and is suitable for students whose limited resources.

### I. Main Idea:
* Combine CNN with LSTM
* Deep CNN as encoder
* Language LSTM as decoder
* End-to-end model I -> S
* Maximize P(S|I)

### II. Dataset: 
[Flickr 8k](https://forms.illinois.edu/sec/1713398). 
The definitive description of the dataset is in the paper “Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics” from 2013.

The authors describe the dataset as follows:

*"We introduce a new benchmark collection for sentence-based image description and search, consisting of 8,000 images that are each paired with five different captions which provide clear descriptions of the salient entities and events … The images were chosen from six different Flickr groups, and tend not to contain any well-known people or locations, but were manually selected to depict a variety of scenes and situations."*

— [Framing Image Description as a Ranking Task: Data, Models and Evaluation Metrics, 2013](https://www.jair.org/media/3994/live-3994-7274-jair.pdf).

### III. Baseline Model:

<p align="center">
  <img src="https://i.imgur.com/1DxxbyK.png" />
</p>

### IV. Implement:
1. Load images and extract feature by VGG16: [kaggle-kernel](https://www.kaggle.com/damminhtien/flirck-8k-dataset-explore-image)
2. Load text data: [kaggle-kernel](https://www.kaggle.com/damminhtien/text-data-exploxe)
3. Develop model and training: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model)
4. Evaluation model: [kaggle-kernel](https://www.kaggle.com/damminhtien/evaluate-model)
5. Generator caption for new images: [kaggle-kernel](https://www.kaggle.com/damminhtien/generation-caption-for-new-image)

### V. Tuning:
> ### Encoder CNN:
* VGG16: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model)
* Resnet50: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model-resnet50)
* **Densenet121**: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model-densenet121)
* Inceptionv3: [kaggle-kernel](https://www.kaggle.com/damminhtien/development-model-inceptionv3)

### VI. Result:
+ BLEU-1: 0.542805
+ BLEU-2: 0.301714
+ BLEU-3: 0.207351
+ BLEU-4: 0.095704

<p align="center">
  <img src="https://i.imgur.com/uFE7Hkn.png" />
</p>

> ### Report comming soon!

### Reference
+ [[1](https://arxiv.org/pdf/1502.03044.pdf)] Kelvin Xu, Jimmy Lei Ba, Ryan Kiros, Kyunghyun Cho, Aaron Courville, Ruslan Salakhutdinov, Richard S. Zemel, Yoshua Bengio. Show, Attend and Tell: Neural Image Caption Generation with Visual Attention. arXiv preprint arXiv:1502.03044, 2016.
+ [[2](https://cs.stanford.edu/people/karpathy/deepimagesent/)] Andrej Karpathy, Li Fei-Fei Deep Visual-Semantic Alignments for Generating Image Descriptions. arXiv preprint arXiv:1412.2306, 2015.
+ [[3](https://arxiv.org/pdf/1411.4555.pdf)] O. Vinyals, A. Toshev, S. Bengio, and D. Erhan. Show and tell: A neural image caption generator. arXiv preprint arXiv:1411.4555, 2014.
+ [[4](https://vision.cornell.edu/se3/wp-content/uploads/2018/03/1501.pdf)] Yin Cui, Guandao Yang, Andreas Veit, Xun Huang, Serge Belongie. Learning to Evaluate Image Captioning.
+ [[5](https://arxiv.org/pdf/1410.1090.pdf)] Junhua Mao, Wei Xu, Yi Yang, Jiang Wang, Alan L. Yuille. Explain Images with Multimodal Recurrent Neural Networks. arXiv preprint arXiv:1410.1090, 2014.
+ [[6](https://arxiv.org/pdf/1411.4389.pdf)] Jeff Donahue, Lisa Anne Hendricks, Marcus Rohrbach, Subhashini Venugopalan, Sergio Guadarrama, Kate Saenko, Trevor Darrell. Long-term Recurrent Convolutional Networks for Visual Recognition and Description. arXiv preprint arXiv:1411.4389, 2016.
+ [[7](https://arxiv.org/pdf/1411.4389.pdf)] Xinlei Chen, C. Lawrence Zitnick. Learning a Recurrent Visual Representation for Image Caption Generation. arXiv preprint arXiv:1411.5654, 2016.


