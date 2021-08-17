---
title: "Notation in Neural Networks"
date: 2021-08-17 00:00:00 +0000
katex: true
---
# Notation in Neural Networks

Reference Video:
<iframe width="1151" height="647" src="https://www.youtube.com/embed/tIeHLnjs5U8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### a usually denotes activation layer node, w - weights, b - bias

To imply **which layer** the particular node is in, we use the superscript.
If the node is in layer L, it's activation may be denoted by \\( a^{(L)} \\) while that of the one before may be \\( a^{(L-1)} \\) .

If the desider output is denoted by y, for that particular activation node, it's cost is \\( C_0 ( \cdots ) = ( a ^{(L)} - y^2 ) \\)

Also \\( a^{(L)} = \sigma ( w ^{(L)} a^{(L-1)} + b^{(L)} ) \\) where b denotes the bias.

For simplicity, \\( w ^{(L)} a^{(L-1)} + b^{(L)} \\) can be denoted by \\( z^{(L)} \\)
so 

\\( a^{(L)} = \sigma( z^{(L)} ) \\)

To imply which particular neuron / node of a particular layer we are referring to, we use the subscript.


