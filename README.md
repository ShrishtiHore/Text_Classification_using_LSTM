# Text_Classification_using_LSTM
This project is made to classify sentiments in IMDB movie reviews. 

**Step 1: Data Preprocessing**
**(a) Loading the Data**

Call imdb.load_data() function for the imdb reviews dataset.

**(b) Converting the Raw Labels into Categorical Vectors**

We convert the raw labels ie. y_train and y_test to categorical vectors 

*   If label = 0 then vector = { 1 , 0 }
*   If label = 1 then vector = { 0 , 1 }

**(c) Padding the Sequences to Fixed length**

Padding is a form of Tokenization of words to fixed length in sequences.

Here we pad the sequences of text data of a fixed length of 120 integers.

So that every emotion can be tokenized later.

**Tokenization**

Tokenization is a way of separating a piece of text into smaller units called tokens. Here, tokens can be either words, characters, or subwords. Hence, tokenization can be broadly classified into 3 types – word, character, and subword (n-gram characters) tokenization.

**Step 2: Defining and Compiling the Model**

Define the Hyperpararmeters for our LSTM model and compile it.

1. Categorical Crossentropy Loss Function
2. Adam Optimizer

**Categorical Cross-Entropy loss**

Also called Softmax Loss. It is a Softmax activation plus a Cross-Entropy loss. If we use this loss, we will train a CNN to output a probability over the C classes for each image. It is used for multi-class classification.
In the specific (and usual) case of Multi-Class classification the labels are one-hot, so only the positive class Cp keeps its term in the loss. There is only one element of the Target vector t which is not zero ti=tp. So discarding the elements of the summation which are zero due to target labels, we can write:

**Adam Optimizer**
Adam is a replacement optimization algorithm for stochastic gradient descent for training deep learning models. Adam combines the best properties of the AdaGrad and RMSProp algorithms to provide an optimization algorithm that can handle sparse gradients on noisy problems.


**Step 3: Training the Model**
Now train the above model over the training dataset with a batch size of 1000 samples.

**References**
1. https://gombru.github.io/2018/05/23/cross_entropy_loss/
2. https://machinelearningmastery.com/adam-optimization-algorithm-for-deep-learning/#:~:text=Adam%20is%20a%20replacement%20optimization,sparse%20gradients%20on%20noisy%20problems.
3. https://medium.com/predict/creating-a-chatbot-from-scratch-using-keras-and-tensorflow-59e8fc76be79
4. analyticsvidhya.com/blog/2020/05/what-is-tokenization-nlp/
