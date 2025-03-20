# Fast AI's Part 1 - summary

At first, machine learning feels like black magic, but [this course](https://course.fast.ai/Lessons/lesson8.html) does an incredible job of distilling the concepts and gradually building intuition about how things work. Below, you’ll find an eclectic mix of ML concepts, definitions, and approaches covered throughout the material.

## ML approaches covered
1. CV model - e.g: resnet
2. Transformers - NLP model like Deberta
3. Model from scratch 
/ gradient descent, ReLU
4. Random forests
//interpreting random forests to better understand the data - feature importance
//works for tabular data
5. Collaborative filtering
//any type of recommendation system
6. CNNs //popular for CV use cases

## Problems solved
1. CV - is it a cat? 
2. Titanic dataset - predictions of who survived?
3. Phrase-to-phrase matching (US Patent competition)
//using HF transformers, Deberta
4. California housing dataset - covers correlation between median income and house prices
// concept: correlation of coefficients, r (-1 perfect inverse, 1 perfect correlation)
5. Paddy rice disease
6. Movie recommendations


## Concepts

## How to think of input datasets?
* Tabular data (spreadsheets and databases) 
* Image data (CV)
* Text data (NLP) //structured or unstructured
* Time-series data //stock prices, vehicle logs
* Audio-data //waveforms or spectograms
* Video-data //sequence of images with temporal relationships
* Graph-data //automotive system architecture, social networks
* Multi-modal //combination of categories, e.g video with audio, images with text descriptions

### Some vocabulary

- **Label**: The data that we're trying to predict, such as "dog" or "cat.” Also known as the dependent variable.
- **Architecture**: The _template_ of the model that we're trying to fit; the actual mathematical function that we're passing the input data and parameters to.
- **Model**: The combination of the architecture with a particular set of parameters.
- **Parameters**: The values in the model that change what task it can do and are updated through model training.
- **Fit**: Update the parameters of the model such that the predictions of the model using the input data match the target labels.
- **Train**: A synonym for _fit_.
- **Pretrained model**: A model that has already been trained, generally using a large dataset, and will be fine-tuned.
- **Fine-tune**: Update a pretrained model for a different task.
- **Loss**: A measure of how good the model is, chosen to drive training via SGD (stochastic gradient descent).
- **Metric**: A measurement of how good the model is, using the validation set, chosen for human interpretation.
- **Validation set**: A set of data held out from training, used only for measuring how good the model is.
- **Training set**: The data used for fitting the model; does not include any data from the validation set.
- **Precision**: Measures how many of the predicted positive items are truly positive.
- **Recall**: Measures how many of the actual positive items the model correctly predicts as positive.
- **F1-score**: The harmonic mean of precision and recall, balancing both metrics.
- **Epoch**: One complete pass through the entire dataset during training.
- **Inference**: The process of using a trained model to generate predictions.
- **Out-of-domain data**: Data that differs significantly from the training set but retains the same meaning.
- **Confusion matrix**: A table used to evaluate model performance by showing true and false positives and negatives.
- **Overfitting**: Training a model in such a way that it _remembers_ specific features of the input data, rather than generalizing well to data not seen during training.
- **Data augmentation** (Computer Vision, NLP): A technique to create variations of input data to improve model generalization.  
  - In **Computer Vision (CV)**, this includes transformations like rotations, brightness adjustments, and cropping.  
  - In **Natural Language Processing (NLP)**, it can involve synonym replacement, back-translation, or word shuffling.
- **Tensor** (Deep Learning): A multi-dimensional array used to store and process data in deep learning.  
- **CNN**: Convolutional neural network; a type of neural network that works particularly well for computer vision tasks. Very good at interpreting spatial hierarchies, detecting edges, forms, and patterns.
- **Transfer learning**: Using a pre-trained model that gets fine-tuned for the use case.
- **Gradient descent**: an essential optimisation method where parameters are set and evaluated against a target set, from where the notion of “loss” is getting derived. It is an iterative process with the goal of reducing the loss.
- **Rectified Linear Units**: Simple mathematical function defined as f(x) = max(0,x) which means it returns 0 when x is negative and x when x is positive. It serves as an activation function directly attached to neurons in a neural network, where the neuron's weighted sum passes through the ReLU to determine its output. If the input is negative, the output is 0 (i.e neuron is not activated); if the input is positive, the output is equal to the input (the neuron is activated).
- **Tokenisation**: The process of splitting the input into tokens and generating an array containing the position of each token in the vocabulary.
- **Underfit**: Insufficient complexity in the model for the objective.
- **Pearson correlation coefficient**: A measure of the degree of relationship between two variables. It usually takes values between -1 and 1, where -1 indicates a perfect inverse correlation, and 1 indicates a perfect positive correlation.
- **Tensors**: Can be an array or a matrix.
  - **Attribute of tensors** → Its shape!
  - **Shape** = Number of rows and number of columns.
  - **Length of a tensor** = Number of axes a tensor has:
    - **Scalar** → Rank 0  
    - **Vector** → Rank 1  
    - **Matrix** → Rank 2  
- **Normalisation**:  
  - A pre-processing technique where data is scaled to prevent some data points from dominating the ML algorithm.  
  - In tabular data parsing, attributes such as age or price (which can have high sparsity) can be divided by their maximum value for min-max scaling.
- **Random forest**:  
  - A machine learning algorithm based on **decision trees**.  
  - Uses a **binary split** approach to partition the data.  
- **Embeddings**: A way to represent data; they store latent factors in a compact, numerical form in a high-dimensional space.
- **Latent factors**: Hidden properties stored inside embeddings.
- **Biases**: A general tendency in the dataset that is not captured by the embeddings.  
  - Example: A user may not like old detective movies, but they might like *LA Confidential*.  
- **PCA (Principal Component Analysis)**: A technique that finds the most important factors in embeddings.
- **Convolution**: Performing linear transformation on the input and filtering to extract features such as edges, textures.

Kudos and thank you to the Fast AI team and Jeremy for making this gem available for free!



