# LSTM_IMDB_Reviews_Sentiment_Analysis

Below is the architecture of **LSTM (Long Short Term Memory)** </br>
![image](https://github.com/ravi0dubey/LSTM_IMDB_Reviews_Sentiment_Analysis/assets/38419795/b0985854-9e68-4583-aa59-07d3a1c4418c)
 
 It is neural network which has three componenents/boxes and each box has different functionality. Once the input sequence is passed from three boxes then the output generated is feeded again as input.
 This cycle continues till we achieve better accuracy. </br>

 Weights of each boxes are determined/updated using Backward Propagation as it is a neural network. </br>
 
 First Box is **Forget Gate** </br>
 Second Box is **Input or Memory Gate** </br>
 Third Box is **Output Gate** </br>

 **Forget gate** -> It takes input from the corpus and then apply **sigmoid activation** on top of it. Output of Sigmoid Activation range from **0 to 1**. If value is closer to 0 then it will forget less context of the input data.
 If value is closer to 1 then it will forget more of the input context. </br>

 **Input or Memory Gate** -> It takes input from the corpus and then apply **sigmoid** activation on top of it. It also applies **tanh** activation on top of input. tanh activation output ranges from -1 to 1. Output of both the activation are **multiplied**. Purpose is to determine how much of _input context needs to be stored in the memory channel_. Reason is we donot need to remember entire text to determine the analysis we are doing on the text. If the combined output of both the channels are closer to 0 then it will save lesser context in the memory channel while if the output is closer to 1 then it will save more in the memory channel.</br>
 
 **Output Gate** -> It takes input from the input from the corpus and then apply **sigmoid activation** on top of it. It takes input from the memory channel and apply **tanh activation** on top of it. Output of both channels are multiplied to give the output. </br>

 
 
 



