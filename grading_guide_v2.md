# Neural Network Assessment — Integration and Grading Guide

**Cross-modular individual assessment**
FOOP 5N0541 · MIT 5N18396 (Assignment 2 Part B) · CM 5N0554
64 marks total · Three days

---

## For the External Examiner

This assessment integrates three QQI Level 5 modules through a single sustained task. Students build a feedforward neural network from scratch in pure Python and use it to investigate how architecture affects learning. The work is individual and completed over three supervised sessions. Students may use static resources — notes, worksheets, documentation — but not AI assistants.

Several parts earn marks from more than one module simultaneously, reflecting the fact that, for example, implementing `weighted_sum` correctly requires both sound function design (FOOP) and accurate application of a mathematical operation (MIT). The mark columns in the table below show this split directly: where a part has marks in two columns, the student earns those marks independently, one toward each module total.

Day 3 contains no new implementation. All marks in Day 3 are for running provided helpers, producing experimental output, and writing analytical responses. Where a student's class is incomplete, Day 3 marks may still be awarded for coherent written reasoning about the experiments.

---

## Complete Marks Breakdown

Parts 1 and 2 are unassessed context-setting and do not contribute to any total.

| Part | Description | FOOP | MIT | CM | Total |
|:-----|:------------|:----:|:---:|:--:|------:|
| **Day 1** | | | | | |
| 1–2 | Data inspection, network structure | — | — | — | — |
| 3 | `random_matrix`: correct dimensions, values in range, tested | 3 | — | — | 3 |
| 4 | `weighted_sum`: dot product and bias, hand-checked test | 2 | 3 | — | 5 |
| 5a | `relu`: correct for positive, negative, and zero input | — | 2 | — | 2 |
| 5b | `softmax`: outputs sum to 1, numerical stability addressed | — | 3 | — | 3 |
| 6 | `make_network`: weight matrices and bias vectors, correct shapes | 3 | — | 2 | 5 |
| 7 | `describe_network`: parameter count correct, output readable | — | — | 2 | 2 |
| 8 | `forward_layer`: pre- and post-activation both returned | 4 | — | — | 4 |
| 9 | `forward`: all layers traversed, correct activation per layer | — | — | 4 | 4 |
| | **Day 1 subtotals** | **12** | **8** | **8** | **28** |
| **Day 2** | | | | | |
| 10 | `predict`: argmax over output, tested on examples | — | — | 2 | 2 |
| 11 | `cross_entropy_loss`: correct formula, log(0) guard, tested | — | 4 | — | 4 |
| 12a | Backprop reading: structure and key steps demonstrated | — | 2 | 1 | 3 |
| 12b | Reflection Q1: explains why weights must be saved first | — | 2 | — | 2 |
| 12c | Reflection Q2: gradient value when prediction is confident | — | 1 | — | 1 |
| 13 | `train`: loop correct, loss and accuracy tracked per example | — | — | 4 | 4 |
| 14 | Random-input sanity check: output inspected and described | — | — | 1 | 1 |
| 15 | `NeuralNetwork` class: all methods present, `__init__` and `__str__` correct | 8 | — | — | 8 |
| | **Day 2 subtotals** | **8** | **9** | **8** | **25** |
| **Day 3** | | | | | |
| Exp. | Three networks trained, curves plotted, output produced | — | — | 3 | 3 |
| Curves | Loss curve questions: rate of change and early stopping linked | — | 4 | — | 4 |
| Gap | Training vs test accuracy compared across three architectures | — | 1 | 1 | 2 |
| Overfit | Overfitting, underfitting, and generalisation discussed | — | 2 | — | 2 |
| | **Day 3 subtotals** | **—** | **7** | **4** | **11** |
| | **Module totals** | **20** | **24** | **20** | **64** |

---

## Learning Outcome Mapping

### FOOP 5N0541

| Parts | Learning outcome |
|:------|:----------------|
| 3, 8 | LO3 — Write, test, and document functions with appropriate parameters and return values |
| 6 | LO5 — Design and implement a data structure appropriate to the problem |
| 4 (partial) | LO3 — Write a function implementing a mathematical operation correctly |
| 15 | LO6, LO7 — Define a class with attributes and methods; instantiate and use objects |

### MIT 5N18396

| Parts | Learning outcome |
|:------|:----------------|
| 4 | 1.1 — Apply arithmetic operations in an algebraic context (dot product and bias) |
| 5a | 3.5 — Define and evaluate a piecewise function (ReLU) |
| 5b | 5.6 — Express a set of values as a probability distribution (softmax) |
| 11 | 3.6 — Apply logarithmic functions in a computational context |
| 12a–c | 3.7 — Interpret the chain rule; evaluate a gradient expression at boundary values |
| Day 3 curves | 3.5, 3.7 — Interpret rate of change in a training context; relate to early stopping |
| Day 3 gap, overfit | 5.12, 6.3 — Compare statistical measures; analyse output of a computational experiment |

### CM 5N0554

| Parts | Learning outcome |
|:------|:----------------|
| 6 (partial) | LO1 — Describe the computational structure of a solution |
| 7 | LO1 — Describe parameter counts and layer structure |
| 9 | LO7 — Implement a sequential algorithmic process |
| 10 | LO8 — Apply a decision rule within an algorithm |
| 12a (partial) | LO8 — Interpret the structure of a provided algorithm |
| 13 | LO10 — Design and implement an iterative computational process |
| 14 | LO11 — Verify behaviour using a controlled test case |
| Day 3 | LO12 — Plan, conduct, and interpret a computational investigation |

---

## Grade Boundaries

Applied to each module's raw total independently.

| Grade | Percentage |
|:------|:----------:|
| Distinction | 80% and above |
| Merit | 65–79% |
| Pass | 50–64% |
| Unsuccessful | Below 50% |

---

## Marking Notes

**Day 1 functions** are awarded primarily for correctness against the test case. Partial credit is appropriate where the approach is clearly sound but there is a minor error — an off-by-one in a loop, a missing return statement, an incorrectly ordered argument. These are different from conceptual gaps and should be treated differently.

**Day 2 reflections (12b and 12c)** are looking for genuine understanding expressed in the student's own words. A response that restates the question without showing reasoning should not receive full marks. A response that shows real thought — even if imprecisely worded — should be rewarded. The marks here are for evidence of understanding, not grammatical precision.

**Day 3** is entirely written and experimental. A student whose class from Day 2 is incomplete may still earn marks here by reasoning clearly about the experiments they were able to run, or by describing what they would expect to happen and why. Partial credit for coherent written reasoning is appropriate and encouraged.

**The class in Part 15** is the capstone of Day 2. If a student's standalone functions from Day 1 are correct but the class methods are not working, it is worth checking whether the error is a translation mistake — forgetting `self.` before an attribute, for instance — rather than a conceptual one. A student who understands what a method should do but has a syntactic slip deserves a different reading than one who has misunderstood the relationship between the class and its data.

---

*Module totals and learning outcome references should be confirmed against current QQI module descriptors and the cross-modular assessment agreement before issue to external examiners.*
