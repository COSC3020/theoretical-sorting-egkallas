[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

One approach to verify this claim is timing the algorithm while increasing the size of the lists it sorts. If the amount of time it takes to sort increases when the size of the list increases, one could infer that it is in fact sorting in linear time. Included in this testing would be sorted lists of increasing size, reverse sorted lists of increasing size, and random lists of increasing size, analyzing the timing for all of these options. 

Though all of these tests may indicate that the algorithm is in fact $O(n)$. In terms of its possible correctness, as dicussed in class, the general sorting problem has a lower bound of $\Omega(nlogn)$ because every comparison based sorting algorithm MUST be able to generate all permuations of a list, the number of which is $n!$. If it doesn't do this, it isn't sorting correctly. Therefor according to the theoretical bounds of comparison based sorting, this algorithm cannot be sorting correctly if it is $O(n)$. 
