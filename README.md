# Traditional Bangladeshi Sports Video Classification Using Deep Learning Method
Traditional Bangladeshi sport is a genre of sports that bears the cultural significance of Bangladesh. This dataset used for training the model consists of traditional Bangladeshi sports videos belonging to five classes: Kabaddi, Boli Khela, Kho Kho, Lathi Khela, and Nouka Baich, collected from Youtube. The main concern of this work is to classify five traditional Bangladeshi sports categories using Convolutional Neural Network and LSTM. Besides, this work is the flask deployment of a part of [this](https://www.mdpi.com/2076-3417/11/5/2149) research work.  

Furthermore, the two most prominent deep learning networks, i.e., **Convolutional Neural Network (CNN)** and **Recurrent Neural Network (RNN)**, are utilized as they can capture the spatial and temporal features, respectively, from videos that are obligatory for correctly classifying the video classes. In this regard, the transfer learning approach with the fine-tuned VGG19 and LSTM is used for the classification task. This model exposes impressive performance by showing 99% average accuracy on the dataset.

## Feature Extraction
- **Spatial Features:**

In videos, spatial features or elements can be defined as the characteristics relevant to the context of the scenes. For extracting the spatial features from traditional Bangladeshi sports videos, a TimeDistributed CNN architecture has been constructed. The input dimension of a TimeDistributed CNN layer is *(samples, frames per video, height, width, channels)*. This architecture employs the same layer of this architecture to all the picked frames of each video one by one through sharing same weights and thus finally produces feature maps for the frames.

- **Temporal Features**:

There remains temporal connectivity across sequential frames in sports videos. The recurrent neural network may play a crucial role in this regard. However, traditional RNN suffers from short term memory, i.e., it is incompetent in retaining information for longer periods. In this regard, **LSTM**, i.e., **Long Short Term Memory**, was developed as a remedy to short-term memory and vanishing gradient problems. Here, the extracted spatial features of sequential frames by CNN are fed to an LSTM layer for analyzing them in order.

## Deep Neural Network Architecture:
![Alt text](images/gui1.png?raw=true "Title")