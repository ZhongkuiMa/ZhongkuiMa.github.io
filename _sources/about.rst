.. image:: imgs/personal_photo.png
  :alt: My personal photo
  :height: 200px
  :align: center

About
======

I'm a second-year PhD student at
`the University of Queensland <https://www.uq.edu.au/>`_ (UQ).
I'm fortunate to be supervised by A/Prof.
`Guangdong Bai <https://baigd.github.io/>`_.

My current research focuses on **neural network verification**, especially verifying neural networks by over-approximating convex hulls, i.e., constructing linear constraints for the non-linear neural networks.

I'm a one hundred percent math amateur, and I'm interested in various mathematical models, especially those related to neural networks.

You can learn more about my work by the following links:

:bdg-link-info:`Google Scholar <https://scholar.google.com.au/citations?user=r2Z7bCMAAAAJ>`,
:bdg-link-info:`LinkedIn <https://www.linkedin.com/in/zhongkui-ma-3276442a8/>`,
:bdg-link-info:`ResearchGate <https://www.researchgate.net/profile/Zhongkui_Ma>`,
:bdg-link-info:`ORCID <https://orcid.org/0000-0002-2392-3751>`,
:bdg-link-info:`Semantic Scholar <https://www.semanticscholar.org/author/Zhongkui-Ma/2267035345>`.

My Study Life
----------------------

2025
~~~~~

This is my third year of PhD study.
My friend `Zihan Wang <https://www.zihan.com.au/>`_ and I published a paper called `Model Modulation with Logits Redistribution <https://www.zihan.com.au/assets/files/WWW25AIM.pdf>`_ on `WWW'25 <https://www2025.thewebconf.org/>`_. It's really a great honor for me to be a co-author of this paper.

Currently, I have not finished my software yet, but I have made some progress.
I'm currently working on some exciting tools that I'm thrilled to share with you:

- `shapeonnx <https://github.com/ZhongkuiMa/shapeonnx>`_: A tool to **infer the shape of an ONNX model** when the official tool is down. It's a simple yet powerful tool that helps you understand the dimensions of your model's inputs and outputs! 📏

- `slimonnx <https://github.com/ZhongkuiMa/slimonnx>`_: A tool to **optimize and simplify your ONNX models** by removing redundant operations and resolving version issues. It makes ONNX files cleaner, more efficient, and ready for action! 🚀

- `torchonnx <https://github.com/ZhongkuiMa/torchonnx>`_: A tool for **converting ONNX models** to **PyTorch models** (``.pth`` for parameters, ``.py`` for structure). It's simple, lightweight, and designed for seamless model conversion 🔄.

- `torchvnnlib <https://github.com/ZhongkuiMa/torchvnnlib>`_: A tool to **convert VNN-LIB files** (``.vnnlib``) to **PyTorch tensors** (``.pth`` files) for efficient neural network verification. Take full advantage of the PyTorch ecosystem! 🚀

- `propdag <https://github.com/ZhongkuiMa/propdag>`_: A **bound propagation framework** for **neural network verification**. It supports any **DAG (Directed Acyclic Graph)** structure, covering both **feedforward** and **backward** propagation patterns for verification. This tool allows researchers to focus on their algorithms without worrying about complex computation graphs! 💪


You can lean more about them in my `Github <https://github.com/ZhongkuiMa>`_.
Please expect my software in recent future.


2024
~~~~

This is my second year of PhD study.
I have began to develop our verification tool for some time, which is mainly implemented by `Pytorch <https://pytorch.org/>`_, I hope it can be released in the end of 2024.
In May of the second year, our paper
(`Zihan Wang <https://www.zihan.com.au/>`_ as the first author)
`CORELOCKER: Neuron-level Usage Control <https://www.computer.org/csdl/proceedings-article/sp/2024/313000a222/1WPcYMh3F1C>`_
about model version control has been accepted by
`S&P'24 <https://sp2024.ieee-security.org/accepted-papers.html>`_.
This work states a critical idea of how large weights affect the model performance.
In Aug of the second year, our paper (Xinguo Feng as the first author)
`Uncovering Gradient Inversion Risks in Practical Language Model Training <?>`_
about gridient inversion attack (GIA) has been accepted by
`CCS'24 <https://www.sigsac.org/ccs/CCS2024/program/accepted-papers.html>`_.
This work uses beam search to invert the text tokens in the language model, which is really a hard work.

2023
~~~~~

I began my PhD study in January, 2023.
I am happy to be supervised by A/Prof.
`Guangdong Bai <https://baigd.github.io/>`_.
I focus on neural network verification, specifically verifying neural networks by over-approximating convex hulls.
I also collaborate with my colleague, `Zihan Wang <https://www.zihan.com.au/>`_ on neuron level usage control, and Xinguo Feng on *gradient inversion attack* (GIA).
I'm very interested in theoretical proofs about neural networks on any topic.
In November of the first year, our paper `ReLU Hull Approximation <https://dl.acm.org/doi/10.1145/3632917>`_ about neural network verification is accepted by `POPL'24 <https://popl24.sigplan.org/room/POPL-2024-venue-kelvin-lecture>`_.
*This is real a great honor for me because you know it is hard.*
This shows a critical idea of how to construct the **function hull**.
This work make an effort on the theoretical proof of the convex hull of a function in `computational geometry <https://en.wikipedia.org/wiki/Computational_geometry>`_.
Our implementation is based on the functions provided by
`pycddlib <https://pycddlib.readthedocs.io/>`_
(`double description algorithm <https://link.springer.com/chapter/10.1007/3-540-61576-8_77>`_)
(many thanks to the authors of pycddlib).


2021 - 2022
~~~~~~~~~~~

I started studying for my master's degree at Queensland University (UQ), majoring in Information Technology.
My main focus was on course study, and I learned Java programming and algorithms in depth.
(Until that time, Java is still my main programming language.)

In the second year, I completed my master's thesis about verifying neural networks by
`abstract interpretation <https://en.wikipedia.org/wiki/Abstract_interpretation>`_,
leveraging polyhedral abstract domains and programming methods specifically based on the following work,
`DeepPoly (POPL'19) <https://dl.acm.org/doi/pdf/10.1145/3290354>`_,
`k-relu (NIPS'19) <https://proceedings.neurips.cc/paper_files/paper/2019/file/0a9fdbb17feb6ccb7ec405cfb85222c4-Paper.pdf>`_,
`PRIMA (POPL'22) <https://dl.acm.org/doi/pdf/10.1145/3498704>`_.
I focused on propagation-based models and LP
(`linear programming <https://en.wikipedia.org/wiki/Linear_programming>`_)-based models.
*This is a start point for me to study neural network verification.*
Even though I began with from the view of *abstract interpretation* of *software verification* and It is a good start, I think it changes to the view of *optimization* and *computational geometry* after that.
(After that, I think *neural network verification* has been transformed into an *optimization* problem with taking the advantage of *automatic differentiation* of modern deep learning frameworks like `Pytorch <https://pytorch.org/>`_ with GPU power.)
Actually, I have finished the main part fo the first paper `ReLU Hull Approximation <https://dl.acm.org/doi/10.1145/3632917>`_ in my master's thesis and it is later accepted by POPL'24 in my PhD study.


2018 – 2020
~~~~~~~~~~~

I taught myself machine learning, especially deep learning.
I had thought deeply about deep learning principles and have a certain understanding
of various models.
This was inspired by my best friend, Shupeng Geng.

During this period, I also taught myself various introductory courses on algebraic geometry, including commutative algebra, homology algebra, algebraic geometry, computational algebraic geometry, algebraic topology, and algebraic number theory.
*Because I think this is my obsession before my post-graduate studying*.
This is my "gap" in my life and I think it is worth mentioning and memorable.
I think I have some understanding of the life.

2014 – 2018
~~~~~~~~~~~

In the first two years,
I started studying for my undergraduate degree at
`Zhengzhou University <http://www.zzu.edu.cn>`_,
majoring in marketing.
I taught myself undergraduate mathematics and statistics introductory courses, including
*mathematical analysis*,
*advanced algebra*,
*advanced geometry*,
*ordinary differential equations*,
*complex functions*,
*functional analysis*,
*probability theory*,
*mathematical statistics*,
*stochastic processes*,
*time series*,
*discrete math*,
*operations research*
and so on and so on.
I taught myself various basic mathematical models and mathematical software (many
software including the `MATLAB <https://www.mathworks.com>`_,
`R <https://www.r-project.org/>`_,
`SPSS <https://www.ibm.com/spss>`_,
`LINGO <https://www.lindo.com/index.php>`_, etc.)
I just learned the basic usage of these software, not the advanced usage in that time.
I started participating in various mathematical modeling competitions and won various
awards (*I think they are not worth mentioning but this is a real experience for me*).

In the last two years,
I was honored to follow my supervisor,
Dr. `Haixin Ding <http://www7.zzu.edu.cn/glxy/info/1501/5201.htm>`_
(`ORCID <https://orcid.org/0000-0002-6438-7908>`__),
at `Zhengzhou University <http://www.zzu.edu.cn>`_.
*I still memorize that night when I was told that he could be my supervisor.*
This is a *turning point* in my life.
During this period, I began to learn about
`system dynamics <https://en.wikipedia.org/wiki/System_dynamics>`_
(`Vensim <https://vensim.com/>`_),
`agent-based models (ABM) <https://en.wikipedia.org/wiki/Agent-based_model>`_
(`Repast Simphony <https://repast.github.io/>`_),
`structural equations modeling <https://en.wikipedia.org/wiki/Structural_equation_modeling>`_
(`R <https://www.r-project.org/>`_),
and
`factor analysis <https://en.wikipedia.org/wiki/Factor_analysis>`_
(`R <https://www.r-project.org/>`_).
Also, affected by my supervisor, I read many books on sociology and philosophy, most of
which involved communication, sociological research methods, and metaphysics.
*This is really very important for me.*
I believe in the metaphysics.

My undergraduate thesis researched consumer perception using factor analysis and web
crawling methods.
This thesis is supervised by Prof. Shuyun Du, the head of our school.
I'm very grateful to complete such a thesis.

In this period, I began to love research and I hoped to become a PhD.


My Hobbies
----------

I collect stamps, coins, and such things from when I was about 10 years old.
I liked to collect various kinds of things when I was a child.

I was also the best
`Yoyo <https://en.wikipedia.org/wiki/Yo-yo>`_
player in my city when I was a child.
I won many times champion in my city
(`Nanyang <https://en.wikipedia.org/wiki/Nanyang,_Henan>`_)
and I'm very proud to have that time.

I was also a good
`pen spinning <https://en.wikipedia.org/wiki/Pen_spinning>`_
player from when I was in senior high school.

I also played skateboard, roller skating, and scooter, when I was in high school.

Philosophers and their works that impressed me include
`Karl Popper <https://en.wikipedia.org/wiki/Karl_Popper>`_
(`The Logic of Scientific Discovery <https://en.wikipedia.org/wiki/The_Logic_of_Scientific_Discovery>`_),
`Thomas Kuhn <https://en.wikipedia.org/wiki/Thomas_Kuhn>`_
(`The Structure of Scientific Revolutions <https://en.wikipedia.org/wiki/The_Structure_of_Scientific_Revolutions>`_),
`Imre Lakatos <https://en.wikipedia.org/wiki/Imre_Lakatos>`_
(`The Methodology of Scientific Research Programmes <https://en.wikipedia.org/wiki/Research_program>`_),
`Vladimir Lenin <https://en.wikipedia.org/wiki/Vladimir_Lenin>`_
(`The State and Revolution <https://en.wikipedia.org/wiki/The_State_and_Revolution>`_),
`Karl Marx <https://en.wikipedia.org/wiki/Karl_Marx>`_
(`Marx's Economic and Philosophic Manuscripts of 1844 <https://en.wikipedia.org/wiki/Economic_and_Philosophic_Manuscripts_of_1844>`_),
`Ludwig Wittgenstein <https://en.wikipedia.org/wiki/Ludwig_Wittgenstein>`_
(`Tractatus Logico-Philosophicus <https://en.wikipedia.org/wiki/Tractatus_Logico-Philosophicus>`_).

My favorite novels includes
`Faust <https://en.wikipedia.org/wiki/Faust>`_,
`The Great Gatsby <https://en.wikipedia.org/wiki/The_Great_Gatsby>`_,
`The Lady of the Camellias <https://en.wikipedia.org/wiki/The_Lady_of_the_Camellias>`_.

My favorite movies includes
`Once Upon a Time in High School <https://en.wikipedia.org/wiki/Once_Upon_a_Time_in_High_School>`_,
`Initial D <https://en.wikipedia.org/wiki/Initial_D_(film)>`_,
`A Beautiful Mind <https://en.wikipedia.org/wiki/A_Beautiful_Mind_(film)>`_,
`The Man Who Knew Infinity <https://en.wikipedia.org/wiki/The_Man_Who_Knew_Infinity>`_,
`Amadeus <https://en.wikipedia.org/wiki/Amadeus_(film)>`_.


I liked music includes pop, rock, electronic, rap music, and more.
In recent years, I'm a big fan of
`KPOP <https://en.wikipedia.org/wiki/K-pop>`_,
especially
`Aespa <https://en.wikipedia.org/wiki/Aespa>`_,
`ITZY <https://en.wikipedia.org/wiki/Itzy>`_,
`LE SSERAFIM <https://en.wikipedia.org/wiki/Le_Sserafim>`_,
`NMIXX <https://en.wikipedia.org/wiki/Nmixx>`_,
`NewJeans <https://en.wikipedia.org/wiki/NewJeans>`_,
`Kiss of Life <https://en.wikipedia.org/wiki/Kiss_of_Life_(group)>`_,
`BlackPink <https://en.wikipedia.org/wiki/Blackpink>`_
`Izna <https://en.wikipedia.org/wiki/Izna>`_,
and mores.



.. raw:: html

    <br>

    <p style="
        font-style: italic;
        text-align: center;
        display: block;
    ">
    “真常应物，真常得性；常应常静，常清静矣。” ——《清静经》
    </p>