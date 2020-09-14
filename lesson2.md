# Lesson 2 questions

* What is a p value?
  * p value is a threshold which 

* `What is a prior?`

* Provide an example of where the bear classification model might work poorly in production, due to structural or style differences in the training data.
  * It may not work in live places where a video feed uses the model to a bear detection alert.

* Where do text models currently have a major deficiency?
  * In generating correct responses

* What are possible negative societal implications of text generation models?
  * Bias.
  
* In situations where a model might make mistakes, and those mistakes could be harmful, what is a good alternative to automating a process?
  * A manual or human supervised process.
  
* What kind of tabular data is deep learning particularly good at?
  * Recommendation systems

* What's a key downside of directly using a deep learning model for recommendation systems?
  * that they only tell you what products a particular user might like, rather than what recommendations would be helpful for a user

* What are the steps of the Drivetrain Approach?
  * Define the objetive
  * Define levers we can control.
  * What data is required and what can be collected.
  * Create models and see what is the effect of the levers on the objective.

* How do the steps of the Drivetrain Approach map to a recommendation system?
  * Objective: Surprise customers with recommendations that delight them thus resulting in increased sales.
  * lever: Ranking the recommendations.
  * Collect data: Conduct randomised experiments to collect data about recommendations.
  * Model: Create multiple models based on seeing/not seeing recommendations.

* Create an image recognition model using data you curate, and deploy it on the web.
  * Done.

* What is DataLoaders?
  * Is a class that stores all DataLoader instances passes to it and makes them available as train and validation sets.

* What four things do we need to tell fastai to create DataLoaders?
  * What kinds of data we have
  * where to get the list of items
  * how to label the items.
  * How to create a validation set.

* What does the splitter parameter to DataBlock do?
  * Randomly splits the data into training and validation sets.
  
* How do we ensure a random split always gives the same validation set?
  * By passing a number to the `seed` parmeter in the `splitter` function.

* What letters are often used to signify the independent and dependent variables?
  * `x` --> independent variable
  * `y` --> dependent variable

* What's the difference between the crop, pad, and squish resize approaches? When might you choose one over the others?
  * `crop` --> removal of features.
  * `pad` --> Filling empty space in image while resizing with 0.
  * `squish` --> changes the shape of the picture
  * Each resizing technique has its own problem. One option would randomly crop a part of the image at each epoch.
  * I will probably choose randomResizedCrop. 

* What is data augmentation? Why is it needed?
  * Augmentation - creating random variations of data so that they appear different but do change the meaning of the data.
  * Is a way to create new data when there is not enough variation in the input data.

* What is the difference between item_tfms and batch_tfms?
  * `item_tfms` - runs transformation on each individual item.
  * `batch_tfms` - runs transforms on batch on GPU. Happens to a batch a time and is much faster.

* What is a confusion matrix?
  * Is a matrix where the daigoal boxes represent the correct classification by the model and the off diagoal represent incorrect classification.

* What does export save?
  * Saves the model (combination of architecture and parmeters)

* What is it called when we use a model for getting predictions, instead of training?
* What are IPython widgets?
  * They are GUI components that bring js to python in web browser.

* When might you want to use CPU for deployment? When might GPU be better?
  * When doing heavy batch processing with user input GPU is better.
  * When dealing with 1 user input at a time CPU is better.

* What are the downsides of deploying your app to a server, instead of to a client (or edge) device such as a phone or PC?
  * Latency
  * Sensitive data transmission over the internet.
  
* What are three examples of problems that could occur when rolling out a bear warning system in practice?
  * Angles of the photo.
  * Not enough light.
  * Moving image will capture bear at different angles and the system may not recognise it.

* What is "out-of-domain data"?
  * Data in production very different from the data the model was trained on.

* What is "domain shift"?
  * Data in production changes over time.

* What are the three steps in the deployment process?
  * Manual process.
  * Limited scope deployment.
  * Gradual expansion.
