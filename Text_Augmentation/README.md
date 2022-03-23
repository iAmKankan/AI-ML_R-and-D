## Index
![Dark](https://user-images.githubusercontent.com/12748752/159751021-3209cbcd-844e-449e-80b0-232412ca0789.png)
![Light](https://user-images.githubusercontent.com/12748752/159751028-9fad0e97-8cb5-4046-b20d-62bda3fdbf49.png)

### What is Data Augmentation or Training Set Expansion?
* Data augmentation artificially increases the size of the training set by generating many **realistic variants** of each training instance. 
* This **reduces overfitting**, making this a _regularization technique_. 
* The generated instances should be as **realistic** as possible: 
   * ideally, given an image from the augmented training set, a human should not be able to tell whether it was augmented or not. 
* Simply adding **white noise will not help**; the modifications should be learnable (white noise is not). 
* **For example**, you can slightly **shift**, **rotate** and **resize** every picture in the training set by various amounts and add the resulting pictures to the training set.
   * This forces the model to be more **tolerant** to **variations** in the **position**, **orientation** and **size of the objects** in the pictures. 
   * For a model that’s more tolerant of different lighting conditions, you can similarly generate many images with various contrasts. 
* In general, you can also **flip the pictures horizontally** (except for text, and other asymmetrical objects). 
* By combining these transformations, you can greatly increase the size of your training set.

Data augmentation techniques are used to generate additional, synthetic data using the data you have. Augmentation methods are super popular in computer vision applications but they are just as powerful for NLP. 

### Data augmentation for vision vs NLP
In computer vision applications data augmentations are done almost everywhere to get larger training data and make the model generalize better. 
* The main methods used involve:
  * cropping, 
  * flipping, 
  * zooming, 
  * rotation, 
  * noise injection, 
  * and many others.  

In computer vision, these transformations are done **on the go** using _**data generators**_. As a batch of data is fed to your neural network it is randomly transformed (augmented). You don’t need to prepare anything before training.

This isn’t the case with NLP, where data augmentation should be done carefully due to the **grammatical structure** of the text. The methods discussed here are used before training. A new augmented dataset is generated beforehand and later fed into data loaders to train the model.
<img src="https://user-images.githubusercontent.com/12748752/159784407-67a978fe-48cc-4bc4-8536-c5094039c7b7.png" width=50% />




## References
![Dark](https://user-images.githubusercontent.com/12748752/159751021-3209cbcd-844e-449e-80b0-232412ca0789.png)
* [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2nd Edition](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)
* [neptune.ai](https://neptune.ai/blog/data-augmentation-nlp#:~:text=Apply%20data%20augmentation%20to%20your,just%20as%20powerful%20for%20NLP.)
