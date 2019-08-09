# mnist-experiments
Experiments on MNIST dataset to clear the concepts and achieve something unique.

## Experiments
1. ![experiment1.ipynb](https://github.com/ParikhKadam/mnist-experiments/blob/master/experiment1.ipynb)  
  **Description**: Changed the distribution of training and testing set by **modifying images to size 56x56** and keeping the real **train images** at the **top left of the new images** while keeping the **test images** on the **bottom right**. Now, training a normal CNN on such a dataset will result in random validation accuracy but good training accuracy. **Many Deep Learning Engineers believe it is impossible to train a model on such a dataset** as the network won't see a single digit in bottom right at the time of training. **As all values except the top right part of the image will be zero during training, the gradient flow will be zero in that part.** But I know that **convolutions can detect a pattern in any part of the image**. Hence, training a model on such dataset is possible. I was able to get **96% accuracy** with a **loss value of approx. 0.15** on this dataset. The prototype file is provided which can be integrated with any model.
