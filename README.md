# mnist-experiments
Experiments on MNIST dataset to clear the concepts and achieve something unique.

## Experiments
1. [experiment1.ipynb](https://github.com/ParikhKadam/mnist-experiments/blob/master/experiment1.ipynb)
   - **Goal**: Train a CNN on data with different distributions of training and tesing set but with same patterns.
   - **What I did**: built differnet training and testing set by **modifying images to size 56x56**, placing the real **train images** in the **top left of new images** and placing the **test images** on the **bottom right**.
   - **Hypothesis**: Training a normal CNN on such a dataset will result in random validation accuracy but good training accuracy. **Many Deep Learning Engineers believe it is impossible to train a model on such a dataset** as the network won't see a single digit in bottom right at the time of training. **As all values except the top right part of the image will be zero during training, the gradient flow will be zero in that part.**
   - **Extra Information**: I know that **convolutions can detect a pattern in any part of the image**. You can tweak the model once you **know the difference in training and testing set distributions**. With the help of MaxPool, I made this possible. Hence, training a model on such dataset is possible (but not always). I was able to get **96% accuracy** with a **loss value of approx. 0.13** on this dataset. The prototype file is provided which can be integrated with any model.
