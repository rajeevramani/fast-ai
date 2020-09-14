# Lesson 4 questions

* How is a grayscale image represented on a computer? How about a color image?
  * Any image is represented on the computer as a number.
* How are the files and folders in the MNIST_SAMPLE dataset structured? Why?
  * /train/{number}
  * /valid/{number}
  * keep training and validation data separate.
* Explain how the "pixel similarity" approach to classifying digits works.
  * it works by
    * caculating the average of pixels of all 3s (for example).
    * Taking each image and checking to see if the average of a image is closer to ideal average of all 3 or all 7 
* What is a list comprehension? Create one now that selects odd numbers from a list and doubles them.

  ```python
  odd_sqr = [x**2 for x in range(1,10) if x%2 != 0]
  print(odd_sqr)
  ```

* What is a "rank-3 tensor"?
  * A rank-3 tensor is a tensor with three axis.
* What is the difference between tensor rank and shape? How do you get the rank from the shape?
  * Shape is the size of each axis.
  * The len(shape) gives you the rank of the tensor.
  * Rank is also called a dimension
* What are RMSE and L1 norm?
  > The difference between the pixels will have to be positive. If not the the + and - difference will average out to 0.
  * L1 norm - mean absolute difference. Make the difference positive.
  * RMSE - Square root of the difference of squares. Also called `L2 Norm`
* How can you apply a calculation on thousands of numbers at once, many thousands of times faster than a Python loop?
  * By using broadcasting.
* Create a 3×3 tensor or array containing the numbers from 1 to 9. Double it. Select the bottom-right four numbers.

```python
a = tensor([[1,2,3],[4,5,6],[7,8,9]])
c = (a * 2)
c.shape,c[1:,1:]

```

* What is broadcasting?
  * Broadcasting is the ability of pytorch to perform math functions like addition and subtraction on arrays and tensors of different sizes.
* Are metrics generally calculated using the training set, or the validation set? Why?
  * metrics are generally calculated using the validation set because we are interested in undersating how well our model performs with data it has not seen before.
* What is SGD?
  * Stochastic gradient descent.
* Why does SGD use mini-batches?
* What are the seven steps in SGD for machine learning?
  1. Initialise
  2. Predict
  3. Loss
  4. Gradient
  5. Step
  6. Repeat from 2(gradient and step untill no further improvement results)
  7. Stop
* How do we initialize the weights in a model?
  * The intial weights of the weights are random.
* What is "loss"?
  * loss is a number that gives us the effectiveness of the weight assignment.
  * Loss will be small when the prediction is closer to target.
* Why can't we always use a high learning rate?
  * Because if we step too far then we will be bouned around.
* What is a "gradient"?
  * It is the slope of the tangent at any point on a curve.
* Do you need to know how to calculate gradients yourself?
  * Nope
* Why can't we use accuracy as a loss function?
  * accuracy is the difference in prediction when very small changes are made to the weights. These changes will reult in near 0 gradients so our step will be 0 which means we cant really calculate the loss.
* Draw the sigmoid function. What is special about its shape?
  * Sigmoid function has a `S` like shape that keep the value between `0` and `1`.
* What is the difference between a loss function and a metric?
  * Mteric is unit used by humans to understand the accuracy of the model
  * loss function is used by the model to calculate the gradient.
* What is the function to calculate new weights using a learning rate?
  * gradient function.
* What does the DataLoader class do?
  * Dataloader class takes the inputs and creates batches and shuffels each batch
* Write pseudocode showing the basic steps taken in each epoch for SGD.
  * predict
  * calculate loss
  * calculate gradient
  * step
  * set parameter gradient to 0 or None
  * repeat
* Create a function that, if passed two arguments [1,2,3,4] and 'abcd', returns [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]. What is special about that output data structure?

```python
a = [1,2,3,4]
b = 'abcd'
c = list(zip(a,b))
c
```

* What does view do in PyTorch?
  * View coverts a matrix to a list of vector or rank-2 tensor.
* What are the "bias" parameters in a neural network? Why do we need them?
  * a linear equation $\ w * x\  will be 0 for all pixels which are 0. Hence we need another term to represent the line which is where b comes.
* What does the @ operator do in Python?
  * @ does matrix multiplication.
* What does the backward method do?
  * Its is called backpropagation and calculates the derivative of the function.
* Why do we have to zero the gradients?
  * loss.backward() adds the gradients to existing ones therefore the current ones need to be set to 0.
* What information do we have to pass to Learner?
  * dataloaders
  * model
  * loss_function
  * optimising function
  * metric.
* Show Python or pseudocode for the basic steps of a training loop.

```python
for xb, yb in some_data_loader:
  calculate_gradient(xb,yb,model)
  for p in parameters:
    p.data -= p.grad * learning_rate
    p.grad = None
```

* What is "ReLU"? Draw a plot of it for values from -2 to +2.
  * ReLU `Rectified linear unit`. Its return 0 for any negative number.
  
  ```python
  plot_function(F.relu)
  ```

* What is an "activation function"?
  * the non linear function in between two linear functions is called activation function.
* What's the difference between F.relu and nn.ReLU?
  * nn.RelU creates module that can used in sequential function.
  * F.RelU is an API that calls the nn.RelU.
* The universal approximation theorem shows that any function can be approximated as closely as needed using just one nonlinearity. So why do we normally use more?
  * With deeper models we dont need as many parameters.
