---
title: "Study Journal: Karpathy's Zero to Hero"
description: My experience in following Andrej Karpathy's "Zero to Hero" YouTube course on neural networks.
date: 2025-09-16
---

Links to the course:
[Webpage](https://karpathy.ai/zero-to-hero.html); 
[YT Playlist](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ)

### sept 16
"As long as you can do the forward pass and the backward pass, it doesn't really matter what the operation is."
The end of "building micrograd" was so so interesting. It was kind of fun in a way to see how Karpathy would implement certain functions, such as division, for this scalar-valued NN library - it almost felt like creating a new language within the framework of Python. After a certain point, we can start utilizing normal functions like `sum` over the neurons but then get out objects that let us run backprop in a way that is much simpler than I would've thought. The loss function itself can be represented as a network of nodes (since, in this example, it is just sum of squares of the distances to the target values) and we can then run backprop on THAT network to find the gradient with respect to the loss value. In trying to predict what he was going to do next, I was thinking that maybe we would have to increment each parameter by the gradient times the distance between each output's predicted value and target value, but this is so much more elegant and logical. Now I finally have a frame of reference for what gradient descent looks like from a programmatic perspective. \
lec 1: complete!!
2.5hrs working : 1hr video len
(๏ᆺ๏υ)

### sept 3
Nevermind, I don't know anything about the multivariable case of the chain rule. So his "easy" fix for solving what to do when a node is referenced multiple times doesn't make that much sense to me (just add together the gradients? what? ... actually, are they just still called derivatives? AP Calc BC is not helping me out too much here 😅) \
Not a lot of progress since yesterday, but progress is progress. \
lec 1: 1:31:42

### sept 2
so far, it's been pretty straightforward. Karpathy makes backpropagation seem so simple. I don't even think it's necessary to think about the chain rule per se in explaining how the gradient is a product of the derivatives (I think that's the proper terminology?), it seems almost intuitive that the way a weight influences the next weight has a multiplicative effect. Hmm. Now that I've written that out, I realize I have a ways to go in being able to *explain* the process to someone else. \
lec 1, 1:15:08