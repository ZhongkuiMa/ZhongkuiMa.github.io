Bound Propagation Approaches in Neural Network Verification
==================================================================

Neural network verification is an exciting field and it essentially frames the verification problem as an *optimization problem*. The core idea? Estimating the possible output range of a neural network given an input range. More precisely, we deal with *over-approximation*, meaning that our estimated output range must fully contain the actual range.

But it doesn't stop at the output—this property must hold for *every neuron*, including those in the intermediate layers. Any approach that guarantees this property is called *sound*, meaning it maintains `soundness <https://en.wikipedia.org/wiki/Soundness>`_. Today, instead of diving deep into verification theory, let's focus on one of the most powerful techniques in this field: **bound propagation**.

Bound Propagation
------------------------

Interval Arithmetic
~~~~~~~~~~~~~~~~~~~~~~~~~~~

The well-known `interval arithmetic <https://en.wikipedia.org/wiki/Interval_arithmetic>`_ is a fundamental form of bound propagation. Think of it as tracking the possible value ranges for each variable and propagating those intervals through the network—hence the term *interval bound propagation*.
Its pros are that it’s simple to implement and works for any type of neural network. However, it has a significant drawback: it can be overly conservative, leading to large intervals that may not accurately reflect the actual output range. This is particularly problematic for deep networks with many layers, where the accumulated error can become substantial.

Zonotope
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Instead of intervals, we can use **zonotopes**, a geometric abstraction commonly used in `affine arithmetic <https://link.springer.com/article/10.1023/B:NUMA.0000049462.70970.b6>`_. This approach originates from `abstract interpretation <https://en.wikipedia.org/wiki/Abstract_interpretation>`_ and has been widely adopted in verification.

.. note::

    Further reading:

    - `An Introduction to Affine Arithmetic <https://scholar.google.com/citations?view_op=view_citation&hl=en&user=mLo7gCEAAAAJ&citation_for_view=mLo7gCEAAAAJ:WF5omc3nYNoC>`_ (2003)
    - `Fast and Effective Robustness Certification <https://proceedings.neurips.cc/paper_files/paper/2018/hash/f2f446980d8e971ef3da97af089481c3-Abstract.html>`_ (NIPS 2018)

Symbolic Bound Propagation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Rather than using explicit numerical intervals, we can track *symbolic expressions* (typically linear) that represent bounds in terms of input variables. This method, *symbolic bound propagation*, offers a much tighter estimation because it takes into account *term cancellation*.
Much tighter bounds than interval arithmetic!

However, all these methods have one thing in common: they *propagate bounds forward*. What if we could achieve even tighter approximations? That’s where **back-substitution** comes into play!

.. note::

    Further reading:

    - `Formal Security Analysis of Neural Networks using Symbolic Intervals <https://www.usenix.org/conference/usenixsecurity18/presentation/wang-shiqi>`_ (Usenix Security 2018)


Bound Propagation with Back-Substitution
------------------------------------------

Bound propagation with back-substitution extends symbolic bound propagation, but instead of moving **forward**, it works **backward**—hence the name *backward bound propagation*.

Forward vs. Backward Bound Propagation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- **Forward:** Start with input variables and propagate bounds layer by layer toward the output.
- **Backward:** Start with the output variables and back-propagate their symbolic expressions toward the input.

This shift in direction allows us to refine bounds at earlier layers, leading to **tighter estimates**. But to make it work, we need one crucial ingredient: **relaxation** of nonlinear functions.

Handling Nonlinearities
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Neural networks contain nonlinear functions, such as activation functions. Since bound propagation relies on linear expressions, we need to approximate these nonlinear functions with **two linear bounds**—one upper and one lower. When propagating bounds, we carefully choose which bound to apply based on weight signs to maintain the soundness property.

.. note::

    Further reading:

    - `Towards Fast Computation of Certified Robustness for ReLU Networks <https://proceedings.mlr.press/v80/weng18a.html?utm_source=miragenews&utm_medium=miragenews&utm_campaign=news>`_ (PMLR 2018) This is *FastLin* and it is the ReLU version of CROWN.
    - `Efficient Neural Network Robustness Certification with General Activation Functions <https://proceedings.neurips.cc/paper/2018/hash/d04863f100d59b3eb688a11f95b0ae60-Abstract.html>`_ (NIPS 2018) This is *CROWN* and it has become the basic technique for the state-of-the-art in neural network verification (`ab-CROWN <https://github.com/Verified-Intelligence/alpha-beta-CROWN>`_). This paper also introduces the linear bounds with optimizable linear bounds by introducing some parameters by taking the linear bounds with learnable parameters.
    - `An abstract domain for certifying neural networks <https://dl.acm.org/doi/abs/10.1145/3290354>`_ (POPL 2019) This is *DeepPoly* that is formulated by the theory of abstract interpretation. There is some tiny difference between DeepPoly and CROWN, but they are basically the same. This difference is that the DeepPoly will update the bounds during the back-substitution with each preceding layers' bounds but CROWN only calculate the bounds until back-substitution to the input layer, which is a tiny point and only shown in the code. Also, there is no theory to showing that such a difference really brings a better bound but some cases confirm such a difference (e.g., two adjacent non-linear layer like MaxPool after ReLU).

Why Use Bound Propagation?
-----------------------------

- **Efficiency**: Bound propagation is *fast*, thanks to parallel computing. Most operations are basic linear algebra operations, which are heavily optimized in modern libraries and can be accelerated using GPUs.
- **Scalability**: Unlike other verification approaches that require solving complex optimization problems, bound propagation works efficiently on large networks.



Comparing Different Bound Propagation Methods
-----------------------------------------------

Bound propagation is a powerful tool in neural network verification. While interval arithmetic is simple and fast, it’s often too loose to be practical. More advanced techniques like zonotope-based and symbolic methods offer much better approximations, with backward symbolic bound propagation being among the tightest available methods.
There's no formal proof ranking these methods in terms of tightness, but we have some general observations:

- **Interval arithmetic** is the most conservative.
- **Forward symbolic bound propagation** is tighter than interval arithmetic but still somewhat conservative.
- **Zonotope-based approaches** can sometimes achieve similar tightness to backward symbolic bound propagation because it require parallel lower and upper linear bounds, but they come with high memory costs.
- **Backward symbolic bound propagation** generally provides the tightest bounds, though it has higher computational complexity.

Backward symbolic bound propagation is generally **the most accurate**, but it comes at the cost of increased computational effort due to repeated back-substitutions.

.. list-table::
   :header-rows: 1

   * - Approach
     - Tightness
     - Memory Usage
     - Time Complexity (for layer number)
   * - Interval Arithmetic
     - Loose
     - Low
     - Fast (Linear)
   * - Forward Symbolic
     - Moderate
     - Low
     - Fast (Linear)
   * - Zonotope
     - Good
     - High
     - Fast (Linear)
   * - Backward Symbolic
     - Best
     - Moderate
     - Slower (Quadratic)

Final Thoughts
-------------------

Is there any proof to guarantee the tightness of the bound propagation?