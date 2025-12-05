# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

Lab Summary
In this lab, I learned how to use Karnaugh maps (KMaps) to simplify logic equations by grouping adjacent terms together. By applying both the Sum of Products (SOP) and Product of Sums (POS) forms, I saw how the same function can be expressed in different simplified ways. I also verified the simplifications by implementing the designs on the Basys3 board and confirming that the output behavior matched the expected truth tables. This helped reinforce the connection between the theory of logic simplification and practical digital design.

Lab Questions
Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?
The edges of a KMap “wrap around” because the map is based on a Gray code sequence, where only one variable changes between adjacent cells. This makes the left and right edges (and the top and bottom edges) adjacent as well. By grouping across edges, we can create larger power-of-2 groups that lead to simpler expressions in the minimized equation.

Why are the names Sum of Products and Products of Sums?
Sum of Products (SOP): Each group in the KMap corresponds to a product term (AND of variables). The final equation is formed by summing (ORing) these product terms together.


Product of Sums (POS): Each group corresponds to a sum term (OR of variables). The final equation is formed by multiplying (ANDing) these sums together.
 The names come directly from the structure of the final Boolean expressions.



Could you open the test? v file – how are we able to check that the signals match using XOR?
The XOR gate outputs a 0 when both inputs are the same and a 1 when they are different. By XORing the output of the design with the expected signal, we can test for correctness: if the result is always 0, then the signals match for all input cases. If we see a 1, it means there is a mismatch for that input.

