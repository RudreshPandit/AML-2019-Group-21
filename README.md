# AML_2019_Group-21
Why is gradient descent important in machine learning?
Gradient Descent is used in machine learning to find parameter values which would minimize the error on any dataset. An error would be defined as the difference between a prediction and an actual output. It can be thought as a blindfolded person going down a valley to reach the lowest point. In this process the person has to apply a trade off between his step size (learning rate) and intended destination (lowest point). A bigger step size could result in missing the lowest point and vice versa.
How does plain vanilla gradient descent work?
Vanilla descent is the pure form of gradient descent. It works by taking small steps in the direction of the gradient. Vanilla descent helps in calculating the error for each of the sample in the data and then updates the same once the output has been calculated.
Two modifications to plain vanilla gradient descent.
a. Momentum
In momentum, past steps are considered before taking the next one. Using the momentum, we would generally avoid the zig zag behaviour and also avoids getting stuck at the saddle points. It helps in computing an exponentially weighted average of the gradients which would then be used to update the weights. Momentum-based gradient descent oscillates in and out of minima because it would have accumulated more history by the time it reaches minima resulting in taking larger and larger steps evidently leads to overshooting the objective. Despite the u-turns, it still converges faster than the vanilla gradient descent.
consider a situation where you are going to a newly opened cinema hall and you get help from people on the way. If everyone is pointing you towards the same direction you will go faster and faster in that direction with more confidence.In effect, the momentum works faster than the pure vanilla gradient descent algorithm.
b. Nesterov’s Accelerated Gradient
Even though momentum can be good algorithm, it can sometimes overshoot. If the gradient keeps on getting flatter or is reverses direction ahead, there is a need to slow down. Nesterov’s Accelerated Gradient helps us in calculating the gradient someway ahead of where we are now. This method can be viewed as a correction factor for the momentum method.

