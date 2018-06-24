# tf_Globally_and_Locally_Consistent_Image_Completion
implementation of Globally_and_Locally_Consistent_Image_Completion on Tensorflow

# Reference

most of the works are moved from:

https://github.com/shinseung428/GlobalLocalImageCompletion_TF

Please check it! He has realy done a interesting inference.

The paper:

Globally and Locally Consistent Image Completion

http://hi.cs.waseda.ac.jp/~iizuka/projects/completion/en/

# What's different?

- Use High Level API (tf.layers/tf.contrib)
- add batch normalisation after dilated CNN
![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/BN.png)

- This model run on 64*64 images
- The structure of model has been changed a liitle bit since the smaller size image
- Add the sigmoid function in the last layer of Completion


# Paper Structure

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/PaperStructure.png)

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/PaperC.png)

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/PaperD.png)


# Paper optimization
![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/Optim.png)


# The structure for this model

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/Sructure.png)


# The result after only 20 steps (5 minutes) <- I mean 5 min on CPU...

The generator has started to do something we want. 

![](https://github.com/mike820808/tf_Globally_and_Locally_Consistent_Image_Completion/blob/master/Photo/20%20epoch%20result.png)

