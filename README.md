# Globally_and_Locally_Consistent_Image_Completion
implementation of Globally_and_Locally_Consistent_Image_Completion on both Pytorch and Tensorflow

# Reference

most of the works are moved from:

https://github.com/shinseung428/GlobalLocalImageCompletion_TF

Please check it! He has realy done a interesting inference.

The paper:

Globally and Locally Consistent Image Completion

http://hi.cs.waseda.ac.jp/~iizuka/projects/completion/en/

# What's different?

1. Move the model to Pytorch
2. Using High Level API (tf.layers/tf.contrib)
3. add batch normalisation after dilated CNN

<img src="https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/BN.png" alt="img" width="500" height="150">

4. This model run on 64*64 images
5. The structure of model has been changed a liitle bit since the smaller size image
6. Add the sigmoid function in the last layer of Completion


# Paper Structure

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/PaperStructure.png)
<img src="https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/PaperC.png" alt="img" width="325" height="300">
<img src="https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/PaperD.png" alt="img" width="350" height="300">



# Paper optimization
<img src="https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/Optim.png" alt="img" width="350" height="300">


# The structure for this model

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/Sructure.png)


# The result after only 20 steps (5 minutes) 

<- Yeah .. I mean 5 min on CPU...

The generator has started to do something we want. The reason may be the reconstructed loss, which enables us to train it as a decoder.

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/20%20epoch%20result.png)

And, the paper they trained

<img src="https://github.com/mike820808/Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/Training_time.png" alt="img" width="500" height="60">


# Still wondering

Which way of initialization will be better for this model?
