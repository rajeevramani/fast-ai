# Lesson 1 questions

* Do you need these for deep learning?
  * Lots of math `F`
  * Lots of data `F`
  * Lots of expensive computers `F`
  * A PhD `F`

* Name five areas where deep learning is now the best in the world.
  * NLP
  * computer vision
  * Medicine
  * Image generation
  * Playing games.

* What was the name of the first device that was based on the principle of the artificial neuron?
  * Mark 1 perceptor

* Based on the book of the same name, what are the requirements for parallel distributed processing (PDP)?
  * A set of processing units
  * A state of activation.
  * An output function for each unit
  * A pattern of connectivity among units
  * A propogation rule to propogate patterns of activities through the network.
  * An activiation rule for combiniting inputs impinging on a unit
  * A learning rule by which the patterns of activity are modified by experience.
  * An environment within which the system must operate

* What were the two theoretical misunderstandings that held back the field of neural networks?
  * They showed that a single layer of these devices was unable to learn some simple but critical mathematical functions (such as XOR)
  * The additional layers would allow any computation but in practice such networks were often too big and too slow to be useful.

* What is a GPU?
  * Graphical processing unit to run parallel computation.

* Open a notebook and execute a cell containing: 1+1. What happens?

* Follow through each cell of the stripped version of the notebook for this chapter. Before executing each cell, guess what will happen.

* Complete the Jupyter Notebook online appendix.

* Why is it hard to use a traditional computer program to recognize images in a photo?

* What did Samuel mean by "weight assignment"?
  * He meant variables with particular choice of values.

* What term do we normally use in deep learning for what Samuel called "weights"?
  * Parameters.

* Draw a picture that summarizes Samuel's view of a machine learning model.

* Why is it hard to understand why a deep learning model makes a particular prediction?
  * Because of the data on which prediction is made is different from data on which training was done.

* What is the name of the theorem that shows that a neural network can solve any mathematical problem to any level of accuracy?
  * Parallel distributed processing.

* What do you need in order to train a model?
  * Labeled data sets.

* How could a feedback loop impact the rollout of a predictive policing model?
  * A positive feedback loop may create a bias in the model.

* Do we always have to use 224×224-pixel images with the cat recognition model?
  * No, the size can change. Size will determine the speed vs accuracy argument.

* What is the difference between classification and regression?
  * Classification will result in a label. While a regression will result in a number.

* What is a validation set? What is a test set? Why do we need them?
  * Validation set is used after the training.
  * Test set is a completely separate data that used after training and validation.
  * Making sure our model can perform accurately agains data that it has not never seen before.

* What will fastai do if you don't provide a validation set?
  * Will create a validation set.
  
* Can we always use a random sample for a validation set? Why or why not?
  * Yes we can split the data randomly into validation and training sets
  * Once we have this split the training and validation sets should stay the same.
  
* What is overfitting? Provide an example.
  * If you train your data for too long, with not enough data and possibly with too many parameters the performance of the model may degragde.
  
* What is a metric? How does it differ from "loss"?
  * Metric is a mesure of how well the model is doing against a model for human consumption
  * Loss is  how good a model is and used by the algorithm to train itself

* How can pretrained models help?
  * A model that has already been trained. The model will be fine tuned.

* What is the "head" of a model?
  * The last part of the model is called the head. It is the last layer of the cnn

* `What kinds of features do the early layers of a CNN find? How about the later layers?`
  
* Are image models only useful for photos?
  * No, along with photos they have also shown demonstration of use in the area of virus identification.

* What is an "architecture"?
  * The template of the model.

* What is segmentation?
  * A model that can recognise the content of every individual pixel in an image.

* What is y_range used for? When do we need it?
  * Its the range of the target.

* What are "hyperparameters"?
  * They are parameters about parameteres.

* What's the best way to avoid failures when using AI in an organization?
  * Using manual process to keep check on the AI.
  * Human supervised deployment models.
  * Gradual expansion
