---
title: "3b1bNN1"
date: 2021-08-08 00:00:00 +0000
katex: true
---
# But What is a Neural Network

### Here we take example of handwriting recognition to detect Numbers

Couple of layers
Each layer contains nodes that take care of a part of the number. So each of these functions sort fo drives or pushes the output towards on enumber, which on adding up end up predicting one particular number at the end.

Basically it is calculating weighted sum, while squishing the whole number line in between 0-1, so that the numbers are easier to process, and is anologous to probability.
So the final function for one node of the NN looks something like

\\( \sigma ( w_1 a_1 + w_2 a_2 + w_3 a_3 + ...  + w_n a_n - \phi ) \\)

where \\( \phi \\) is a bias added to the function to assign how much importance that part is to the final output.

\\( w_i \\) can be considered like knobs that can be slowly tweaked and manipulated to reach desired results.

\\( a_i \\) are the results coming in from the previous layer!

Basically the work of the computer is to tweak all of these knobs to  find the perfect setting to output what we want.
