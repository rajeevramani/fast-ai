# Lesson 2 questions

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
