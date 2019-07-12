# AML_2019_Group-21
Why is gradient descent important in machine learning?
Gradient Descent is used in machine learning to find parameter values which would minimize the error on any dataset. An error would be defined as the difference between a prediction and an actual output. It can be thought as a blindfolded person going down a valley to reach the lowest point. In this process the person has to apply a trade off between his step size (learning rate) and intended destination (lowest point). A bigger step size could result in missing the lowest point and vice versa.

How does plain vanilla gradient descent work?

Vanilla descent is the pure form of gradient descent. It works by taking small steps in the direction of the gradient. Vanilla descent helps in calculating the error for each of the sample in the data and then updates the same once the output has been calculated.

Two modifications to plain vanilla gradient descent.

a. Momentum
In momentum, past steps are considered before taking the next one. This will help in avoiding the zig zag behaviour (re-routing) or getting stuck at the saddle points. It computes an exponentially weighted average of the gradients which is used to update the weights. It oscillates in and out of minima because it would have accumulated more history by the time it reaches minima resulting in taking larger and larger steps and leads to overshooting the objective. Despite the u-turns, it still converges faster than the vanilla gradient descent. 

Consider a situation where you are going to a newly opened cinema hall and you get help from people on the way. If everyone is pointing you towards the same direction you will go faster and faster in that direction with more confidence.Therefore, the momentum works faster than the pure vanilla gradient descent algorithm.

b. Nesterov’s Accelerated Gradient

Even though momentum can be good algorithm, it can sometimes overpredict (overshoot). If the gradient keeps on getting flatter or is reverses direction ahead, there is a need to slow down. Nesterov’s accelerated Gradient helps us in calculating the gradient someway ahead of where we are now. This method can be viewed as a correction factor for the momentum method. Instead of moving two steps at a time, we first take a small step in the direction ( based on past history) and then update the path based on current location (new gradient)

![image](https://user-images.githubusercontent.com/52764007/61092306-a9308380-a43d-11e9-872b-4eecc6b587ae.png)
![Loss vs Iteration](https://user-images.githubusercontent.com/52764007/61092660-11339980-a43f-11e9-8bd4-ac4899e57b7a.png)
![Camel Hump](https://user-images.githubusercontent.com/52764007/61092661-11cc3000-a43f-11e9-8899-e2d94d7d57f2.JPG)
![Step size vs  Number of iterations](https://user-images.githubusercontent.com/52764007/61092662-11cc3000-a43f-11e9-8df2-7e37f17d71c8.JPG)
![Steps vs Loss](https://user-images.githubusercontent.com/52764007/61092663-11cc3000-a43f-11e9-9d08-a5edb7d9c4ea.JPG)

We can see from the graph that the number of iterations reduce as step size increases as we move faster towards the minima. Also, the loss function approaches a constant value at approximately 1000 iterations. For momentum and accelerated gradients we will reach the minima in fewer iterations.

However, accelerated is the recommended one as it corrects the overshooting aspect of the momentum method.

The visualisation function shows the plot of losses from camel hump function against x and y values.
