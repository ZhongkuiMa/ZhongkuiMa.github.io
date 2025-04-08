Learn NNV in 3 Minutes
=======================

Neural network verification (NNV) is a process to check whether a neural network model satisfies a given property.
Commonly, we want to check whether the output of a neural network satisfy a given property for a specified set of input data.
For example, you can check whether the output of a neural network is always positive for all perturbed input data.

.. tip::

    Even though the property to verify may also be about inputs with a given output, we only consider the output for a given input in this document, which is also the approach we implemented in our tool.
    There have been some researches on the verification of the input-output relation of neural networks, but it is not the focus of our tool.

.. admonition:: Example

    To understand it, we give a small example of a given function :math:`f(x)` and a set of input :math:`\mathcal{X} = \{ x \mid x \in [-1,1]\}`.
    We want to check whether the output of the function :math:`f(x)` is always positive for all input :math:`x \in \mathcal{X}`.

This is a very simple example, but it is a basic concept of neural network verification.
For the case of neural networks, the function :math:`f` is a neural network model and the input :math:`x` is a data point.
Commonly, the input :math:`x` is a high-dimensional vector and the function :math:`f` is a deep neural network model.
The property we want to check is called a *property* and the set of input data is called an *input domain*.

Difficulties on NNV
~~~~~~~~~~~~~~~~~~~

What makes this problem difficult is that

- the neural network is a high-dimensional non-linear function and
- the input domain is a high-dimensional space containing infinite points.

So, we cannot just check all points in the input domain by brute force.
Instead, we need another analysis method to check the property.

Approaches for NNV
------------------

To solve this problem, sometimes we cannot give a precise answer (what we call *exact approaches*) or it is unnecessary, but an approximate answer (what we call *approximate approaches*) is enough.

One easy approximate approach is to use
`interval arithmetic <https://en.wikipedia.org/wiki/Interval_arithmetic>`_
but it is not enough for deep neural networks especially with non-linear activation and deep layers.
*Bound propagation* is a more advanced approach than interval arithmetic because it considers symbolic variables rather than just scalar values.
Bound propagation has become a popular approach in neural network verification because its high efficiency and scalability.

Further Formalization
---------------------


We talk about the verification on local robustness of neural networks.
**Local robustness** is a property that the output of a neural network does not change much when the input is perturbed slightly.

For *classification tasks*, the local robustness is a property that the output of a neural network does not change its class when the input is perturbed slightly.
The logits of the correct label should be the highest among all labels for all perturbed input data, i.e., the correct label should be greater than all other labels.

.. hint::

   Local robustness is commonly a property to evaluate the effectiveness and efficiency
   of a verification tool because the local robustness

   - considers *all perturbation of the high-dimensional input* and
   - cover all *output properties that can be defined by a linear form*.


For input perturbation, we commonly use the :math:`\epsilon`-ball around the input data :math:`x` as the perturbed input data.
The :math:`\epsilon`-ball is defined as a :math:`l_{\infty}` norm ball with radius :math:`\epsilon` around the input data :math:`x`:

.. math::

    \{ x' \mid \| x' - x \| \leq \epsilon \}.

For a image data, the :math:`l_{\infty}` norm is defined as the maximum absolute difference between the pixel values of two images.
That is to say each pixel value of the perturbed image is within :math:`\epsilon` of the original image.

Then, we can define the property as follows:

.. math::

    f(x) = \arg\max_{i} f_i(x)
    \quad \Rightarrow \quad
    \forall j \neq i, f_i(x) - f_j(x) > 0.

This means that the output of the neural network should be the highest for the correct answer and the difference between the correct answer and the other answers should be positive.