---
title: "Notation in Neural Networks"
date: 2021-08-17 00:00:00 +0000
katex: true
---
# Notation in Neural Networks

### a usually denotes activation layer node, w - weights, b - bias

To imply **which layer** the particular node is in, we use the superscript.
If the node is in layer L, it's activation may be denoted by\\( a^(L) \\) while that of the one before may be \\( a^(L-1) \\) .

If the desider output is denoted by y, for that particular activation node, it's cost is \\( C_0 ( \hdots ) = ( a^(L) - y^2 \\)

Also \\( a^(L) = \sigma ( w^(L) a(L-1) + b(L) \\) where b denotes the bias.

For simplicity, \\( w^(L) a(L-1) + b(L) \\) can be denoted by \\( z^(L) \\)
so \\( a^(L) = \sigma( z^(L) ) \\)
