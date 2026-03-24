# Neural Network Assessment — Student Overview

**FOOP 5N0541 · MIT 5N18396 (Assignment 2 Part B) · CM 5N0554**
Individual assessment · Three days · 64 marks total

---

## What We Are Building Together

Over the next three days we are going to build a neural network from scratch. No machine learning libraries, no shortcuts — just Python, mathematics, and our own thinking. By the end of Day 2 we will have a working `NeuralNetwork` class that can be trained on handwritten digit images, and on Day 3 we will run three experiments to explore what different design choices actually do to a network's ability to learn.

The reason we are building it this way, rather than importing a library that does it for us, is that understanding each piece — what a weighted sum is, why a loss function works the way it does, what backpropagation is actually changing — is far more valuable than knowing how to call a function we have never looked inside.

This assessment counts simultaneously toward three modules. FOOP is interested in how we write and organise code. Maths for IT is interested in whether we can apply mathematical ideas — dot products, logarithms, piecewise functions, rates of change — in a real context. Computational Methods is interested in whether we can reason about an algorithm as a whole. Several parts of the assessment earn marks from more than one module at once, because the work genuinely involves more than one kind of thinking at the same time.

---

## The Shape of the Three Days

Day 1 lays the mathematical foundations. We will write the functions that initialise the network's weights, compute weighted sums, apply activation functions (ReLU for the hidden layers, softmax for the output), and pass an input forward through every layer. By the end of Day 1 we will have a working forward pass.

Day 2 adds the learning half. We will write a loss function to measure how wrong our predictions are, read and reflect on a provided backpropagation function, write the training loop that ties everything together, and finally assemble all of our functions into a `NeuralNetwork` class. The class assembly is the centrepiece of Day 2 — it is where everything we built in isolation comes together as a coherent system.

Day 3 is investigative. We train three networks of very different sizes on the same data and compare what we see. The questions on Day 3 do not ask us to write new code; they ask us to look at what happened and explain it. Those written responses carry real marks, and they are worth investing in.

---

## What Will Make This Challenging

The scale is the main thing. We are not writing one function in isolation — we are building a set of functions that depend on each other, and then assembling them into a class. If an early function has a subtle problem, it may only surface several parts later, when something else produces unexpected output. Keeping each piece small, well-named, and tested before moving on is the best defence against this.

There will likely be a moment, probably in Day 2, when several things feel unfamiliar at once — the loss function, the backpropagation function, and the class structure all in the same session. That feeling is normal. It does not mean we are lost. It means we are at the edge of what we already know, which is exactly where learning happens. Working methodically through the test cells, one function at a time, is a reliable way through it.

---

## Some Approaches That Help

**Name things clearly.** When a variable is called `pre_activation_values` rather than `x`, both we and anyone reading the code know immediately what it holds. Meaningful names also help us catch our own mistakes — if a variable called `output_probs` contains negative values, we notice at once. Throughout this assessment, let us choose names that say what a value represents.

**Write before we code.** Each function in the notebook comes with a docstring describing what it should do. Before writing any Python, it is worth writing a few lines in plain English underneath describing how we plan to approach it. Something like: *for each node in this layer, compute the dot product of its weights with the inputs, add the bias, collect all those values into a list, then apply the activation function.* That sentence is the algorithm. The code is a translation of it. Students who write this kind of plan first tend to write cleaner code and debug it much more easily.

**Fall back on language.** We have been using language to make sense of things since we were very young. Mathematics and code are newer, and it is normal to find them less natural. When something is confusing, writing about it — even just describing what we understand so far and where exactly we get stuck — is often the most effective way of getting unstuck. The reflection questions in Days 2 and 3 are an invitation to do exactly this, and they are assessed on the quality of the reasoning, not on whether the phrasing is perfectly precise.

**When given code is confusing, poke at it.** The backpropagation function in Day 2 is provided because deriving it from scratch would require more calculus than we have covered. But reading and understanding it is part of the assessment. One of the most effective ways to understand code we did not write is to add print statements, change a value and observe what breaks, or add a comment to each line saying in our own words what it does. This is not a shortcut — it is a genuine reading strategy.

**Test small before testing large.** Every function has a test cell underneath it with small, hand-checked examples. Running those tests as we go means that when something goes wrong, we can be confident the problem is in the function we just wrote, not somewhere deeper in the network.

**We are welcome to use all our resources from class.** Notes, worksheets, the module handbook, and online documentation are all available. If there is a worksheet on dot products or logarithms, we can refer to it. The only restriction is AI assistants.

---

## If Things Go Wrong

Getting stuck is part of the process. If a function is producing unexpected output, one of the most reliable paths forward is to make the test case smaller. Instead of testing with a full 784-value input, test with three values. Work out the expected answer by hand, then check whether the function agrees. The gap between what we expected and what we got is exactly the information we need.

If we reach Day 3 with the class not fully working, that is worth noting but not worth stopping for. Day 3 marks come from running experiments and writing about what we observe. A partially broken network still produces output. That output is still worth discussing.

The goal across all three days is not a flawless implementation. It is a notebook that shows we understand what we are building.

---

## Mark Summary

| Module | Day 1 | Day 2 | Day 3 | Total |
|:-------|------:|------:|------:|------:|
| FOOP 5N0541 | 12 | 8 | — | **20** |
| MIT 5N18396 | 8 | 9 | 7 | **24** |
| CM 5N0554 | 8 | 8 | 4 | **20** |
| **Day total** | **28** | **25** | **11** | **64** |

Several parts earn marks from more than one module. The full breakdown is in the grading guide.

| Grade | Percentage |
|:------|:----------:|
| Distinction | 80% and above |
| Merit | 65–79% |
| Pass | 50–64% |
| Unsuccessful | Below 50% |

Grade boundaries apply to each module's total independently.
