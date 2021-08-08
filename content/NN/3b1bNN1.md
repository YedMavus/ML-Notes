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

---
 Matrix Representation

The first layer's first node is represented as 

\\( a_0 ^(1) = \sigma ( w_0,0 a_0 ^(0) + w_0,1 a_1 ^(0) + w_0,2 a_2 ^(0) + ...  + w_0,n a_n ^(0) - \b_0 ) \\)


 where \\( \sigma() refers to the [sigmoid function](https://en.wikipedia.org/wiki/Sigmoid_function) and \\( b_0 \\) is the bias.
 
\\( 
\begin{bmatrix}
w_{00} & w_{01} & \cdots & w_{0n} \\ 
w_{10} & w_{11} & \cdots & w_{1n} \\
\vdots & \vdots & \ddots & \vdots \\
w_{k0} & w_{k1} & \cdots & w_{kn} \\
\end{bmatrix}
\begin{bmatrix}
a_{0} ^0 \\ 
a_{1} ^0 \\
\vdots  \\
a_{0} ^n
\end{bmatrix}
+
\begin{bmatrix}
b_{0} \\ 
b_{1}   \\
\vdots \\
b_{0} 
\end{bmatrix}
\\)
