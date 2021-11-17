# MNT
Dataset link - http://www.manythings.org/anki/
[hin-eng.zip](https://github.com/ishikkkkaaaa/MNT/files/7543582/hin-eng.zip)

 
## The encoder
Layers of recurrent units where, in each time step, an input token is received, collecting relevant information and producing a hidden state. This depends on the type of RNN; in our example, a LSTM, the unit mixes the current hidden state and the input and returns an output, discarded, and a new hidden state.
## The encoder vector
The encoder vector is the last hidden state of the encoder, and it tries to contain as much of the useful input information as possible to help the decoder get the best results. It’s the only information from the input that the decoder will get.
## The decoder
Layers of recurrent units — e.g., LSTMs — where each unit produces an output at a time step t. The hidden state of the first unit is the encoder vector, and the rest of the units accept the hidden state from the previous unit. The output is calculated using a softmax function to obtain a probability for every token in the output vocabulary.

 
## Tokenization:
As a neural network requires numerical data to process, it becomes necessary to convert our string input to a numerical list. One way of doing this is to use Tokenizer provided by keras-preprocessing library.
Also, remember it is mandatory to have an equal length of all input sequences in sequence-to-sequence models
 
## Sigmoid activation function
Activation functions are used to introduce nonlinearity to models, which allows deep learning models to learn nonlinear prediction boundaries.
Generally, the rectifier activation function is the most popular.
Sigmoid is used in the output layer while making binary predictions. Softmax is used in the output layer while making multi-class predictions.
 
## LSTM Networks
<b>Long Short Term Memory networks</b> – usually just called “LSTMs” – are a special kind of RNN, capable of learning long-term dependencies. They were introduced by Hochreiter & Schmidhuber (1997), and were refined and popularized by many people in following work.1 They work tremendously well on a large variety of problems, and are now widely used.
LSTMs are explicitly designed to avoid the long-term dependency problem. Remembering information for long periods of time is practically their default behavior, not something they struggle to learn!
All recurrent neural networks have the form of a chain of repeating modules of neural network. In standard RNNs, this repeating module will have a very simple structure, such as a single tanh layer.


## BLEU

- BLEU, or the Bilingual Evaluation Understudy, is a score for comparing a candidate translation of text to one or more reference translations.
Although developed for translation, it can be used to evaluate text generated for a suite of natural language processing tasks.

- The Bilingual Evaluation Understudy Score, or BLEU for short, is a metric for evaluating a generated sentence to a reference sentence.
A perfect match results in a score of 1.0, whereas a perfect mismatch results in a score of 0.0.
The score was developed for evaluating the predictions made by automatic machine translation systems. It is not perfect, but does offer 5 compelling benefits:

- PROS
    - It is quick and inexpensive to calculate.
    - It is easy to understand.
    - It is language independent.
    - It correlates highly with human evaluation.
    - It has been widely adopted.
- Cons
    - It doesn't consider meaning.
    - It doesn't directly consider sentence structure.
    - It doesn't handle morphologically rich languages well.
    - It doesn't map well to human judgements.
 

## ANN 
- ANN-based computing primarily aims to design advanced mathematical algorithms that allow Artificial Neural Networks to learn by imitating the information processing and knowledge acquisition functions of the human brain.
Components of Artificial Neural Networks 
- ANNs are comprised of three core layers or phases – an input layer, hidden layer/s, and an output layer.  
    - Input Layer: The first layer is fed with the input, that is, raw data. It conveys the information from the outside world to the network. In this layer, no computation is performed – the nodes merely pass on the information to the hidden layer.
    - Hidden Layer: In this layer, the nodes lie hidden behind the input layer – they comprise the abstraction part in every neural network. All the computations on the features entered through the input layer occur in the hidden layer/s, and then, it transfers the result to the output layer.
    - Output Layer: This layer depicts the results of the computations performed by the network to the outer world.

    
## Attention Mechanism
- The major drawback of encoder-decoder model in sequence to sequence recurrent neural network is that it can only work on short sequences. It is difficult for the encoder model to memorize long sequences and convert it into a fixed-length vector. Moreover, the decoder receives only one information that is the last encoder hidden state. Hence it's difficult for the decoder to summarize large input sequence at once. So, how do we overcome this problem?
- How about if we give a vector representation from every encoder step to the decoder model!
- Now, this is where the concept of ‘Attention Mechanism’ comes. The major intuition about this is that it predicts the next word by concentrating on a few relevant parts of the sequence rather than looking on the entire sequence.
<I>In layman terms it can be described as an interference between encoder and decoder which extracts useful information from encoder and transmits it back to the decoder.</I>
