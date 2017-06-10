## Multilabel classification using BP-MLL (Backpropagation for Multilabel Learning, [Zhang et. al](http://ieeexplore.ieee.org/document/1683770/))
In Multilabel classification each data point is associated with a set of labels whose size is not fixed. The number of all possible labels is known but not the size of label set associated with each data point. 
An example of such type of problem could be *keyword extraction for news articles*. A news article can be associated with a number of possible keywords in the keywords universe and the number of such keywords may not be known *apriori*. A simple way of solving such problem would be to devise a binary classification problem by training ```n``` independent binary classifiers each predicting whether or not a news article belongs to a certain class (has a certain keyword). One of the downsides of such method is that ```n``` seperate models need to be trained which is computationally expensive both during training and inference. The other downside of such approach is that correlation information between labels are completely ignored, which may not be desirable in most cases. 

Turns out a simple modification of loss function while training a neural network allows us to learn multilabel classification effeciently.

<img src="https://github.com/krsapkota/multilabel_classification/blob/master/multilabel_loss_function.png" width="380">

