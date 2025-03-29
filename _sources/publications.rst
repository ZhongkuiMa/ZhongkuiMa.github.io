Publications
===============

Conference Papers
-----------------

2025
~~~~

.. dropdown:: "AI Model Modulation with Logits Redistribution".
    Zihan Wang, **Zhongkui Ma**, Xinguo Feng, Zhiyang Mei, Zhiyong Ma, Derui Wang, Jason Xue, Guangdong Bai.
    *2025, the ACM Web Conference 2025 (WWW'25)*,
    Sydney, Australia.
    :bdg-link-info:`OpenReview <https://openreview.net/forum?id=lOSomJvrc5#discussion>`
    :bdg-link-info:`PDF <https://www.zihan.com.au/assets/files/WWW25AIM.pdf>`
    :bdg-link-info:`GitHub <https://github.com/UQ-Trust-Lab/AIM>`

    **Abstract:**
    The substantial data and resource consumption of training deep neural networks has rendered the large-scale training accessible only to organizations with necessary infrastructure and massive datasets. Once these models are developed, they are typically adapted to meet the diverse requirements of model owners and users through techniques like early exiting and fine-tuning. However, maintaining multiple specialized versions of the established model is inefficient and unsustainable in the long run. In response to this challenge, we propose AIM, a novel model modulation paradigm that enables a single model to exhibit diverse behaviors meeting the specific needs of stakeholders. AIM enables two key modulation modes: utility and focus modulation. The former provides model owners with dynamic control over output quality to deliver varying utility levels from the same model, the latter offers users precise control to shift model's focused features of inputs.

    AIM introduces a logits redistribution strategy for modulating model behaviors. It operates in a training data-agnostic and retraining-free manner by directly manipulating off-the-shelf pre-trained networks, facilitating AIM's seamless integration across diverse neural network architectures. To mathematically guarantee that our modulation achieves a precise regulation of model behavior, we establish a formal foundation grounded in the statistical properties of logits ordering via joint probability distributions. Our evaluation spans across diverse applications, including image classification, semantic segmentation, and text generation, utilizing prevalent architectures such as ResNet, SegFormer, and Llama. Experimental results confirm the efficacy of our approach, demonstrating the practicality and versatility of AIM in realizing AI model modulation. AIM provides both theoretical and system-level tools to empower a single model to meet diverse needs of both model owners and users, paving the way for scalable, accessible, and efficient AI deployment.


    .. code-block:: bibtex

        @inproceedings{
          wang2025ai,
          title={{AI} Model Modulation with Logits Redistribution},
          author={Zihan Wang and Zhongkui Ma and Xinguo Feng and Zhiyang Mei and Zhiyong Ma and Derui Wang and Jason Xue and Guangdong Bai},
          booktitle={THE WEB CONFERENCE 2025},
          year={2025},
          url={https://openreview.net/forum?id=lOSomJvrc5}
        }

2024
~~~~

.. dropdown:: "Uncovering Gradient Inversion Risks in Practical Language Model Training".
    Xinguo Feng, **Zhongkui Ma**, Zihan Wang, Eu Joe Chegne, Mengyao Ma, Alshrif Abuadbba, and Guangdong Bai.
    *2024, the 31th ACM Conference on Computer and Communications Security (CCS'24)*,
    Salt Lake City, USA.
    :bdg-link-info:`PDF <https://dl.acm.org/doi/pdf/10.1145/3658644.3690292>`
    :bdg-link-info:`GitHub <https://github.com/UQ-Trust-Lab/GRAB>`

    **Abstract:**
    The gradient inversion attack has been demonstrated as a significant privacy threat to federated learning (FL), particularly in continuous domains such as vision models. In contrast, it is often considered less effective or highly dependent on impractical training settings when applied to language models, due to the challenges posed by the discrete nature of tokens in text data. As a result, its potential privacy threats remain largely underestimated, despite FL being an emerging training method for language models. In this work, we propose a domain-specific gradient inversion attack named GRAB (<u>gra</u>dient inversion with hy<u>b</u>rid optimization). GRAB features two alternating optimization processes to address the challenges caused by practical training settings, including a simultaneous optimization on dropout masks between layers for improved token recovery and a discrete optimization for effective token sequencing. GRAB can recover a significant portion (up to 92.9% recovery rate) of the private training data, outperforming the attack strategy of utilizing discrete optimization with an auxiliary model by notable improvements of up to 28.9% recovery rate in benchmark settings and 48.5% recovery rate in practical settings. GRAB provides a valuable step forward in understanding this privacy threat in the emerging FL training mode of language models.

    .. code-block:: bibtex

        @inproceedings{10.1145/3658644.3690292,
          author = {Feng, Xinguo and Ma, Zhongkui and Wang, Zihan and Chegne, Eu Joe and Ma, Mengyao and Abuadbba, Alsharif and Bai, Guangdong},
          title = {Uncovering Gradient Inversion Risks in Practical Language Model Training},
          year = {2024},
          isbn = {9798400706363},
          publisher = {Association for Computing Machinery},
          address = {New York, NY, USA},
          url = {https://doi.org/10.1145/3658644.3690292},
          doi = {10.1145/3658644.3690292},
          booktitle = {Proceedings of the 2024 on ACM SIGSAC Conference on Computer and Communications Security},
          pages = {3525–3539},
          numpages = {15},
          location = {Salt Lake City, UT, USA},
          series = {CCS '24}
        }

.. dropdown:: "CoreLocker: Neuron-level Usage Control".
    Zihan Wang, **Zhongkui Ma**, Xinguo Feng, Ruoxi Sun, Hu Wang, Minhui Xue,
    Guangdong Bai.
    *2024, the 45th IEEE Symposium on Security and Privacy (S&P'24)*,
    San Francisco, USA.
    :bdg-link-info:`PDF <https://www.computer.org/csdl/proceedings-article/sp/2024/313000a222/1WPcYMh3F1C>`
    :bdg-link-info:`GitHub <https://github.com/CoreLocker/CoreLocker>`
    :bdg-link-info:`Profile <https://www.zihan.com.au/SP24CoreLocker.html>`
    :bdg-link-info:`Live Video <https://www.youtube.com/watch?v=I9IYVI73odM>`

    **Abstract:**
    The growing complexity of deep neural network models in modern application domains necessitates a complex training process that involves extensive data, sophisticated design, and substantial computation. The trained model inherently encapsulates the intellectual property owned by the model developer (or the model owner). Consequently, safeguarding the model from unauthorized use by entities who obtain access to the model (or the model controllers), i.e., preserving the fundamental rights and proprietary interests of the model owner, has become a critical necessity.In this work, we propose CORELOCKER, employing the strategic extraction of a small subset of significant weights from the neural network. This subset serves as the access key to unlock the model’s complete capability. The extraction of the key can be customized to varying levels of utility that the model owner intends to release. Authorized users with the access key have full access to the model, while unauthorized users can have access to only part of its capability. We establish a formal foundation to underpin CORELOCKER, which provides crucial lower and upper bounds for the utility disparity between pre- and post-protected networks. We evaluate CORELOCKER using representative datasets such as Fashion-MNIST, CIFAR-10, and CIFAR-100, as well as real-world models including VggNet, ResNet, and DenseNet. Our experimental results confirm its efficacy. We also demonstrate CORELOCKER’s resilience against advanced model restoration attacks based on fine-tuning and pruning.

    .. code-block:: bibtex

        @inproceedings{wang2024corelocker,
          title={CoreLocker: Neuron-level Usage Control},
          author={Wang, Zihan and Ma, Zhongkui and Feng, Xinguo and Sun, Ruoxi and Wang, Hu and Xue, Minhui and Bai, Guangdong},
          booktitle={2024 IEEE Symposium on Security and Privacy (SP)},
          pages={222--222},
          year={2024},
          organization={IEEE Computer Society}
        }

.. dropdown:: "ReLU Hull Approximation".
    **Zhongkui Ma**, Jiaying Li, Guangdong Bai.
    *2024, the 51st ACM SIGPLAN Symposium on Principles of Programming Languages
    (POPL'24)*,
    London, UK.
    :bdg-link-info:`PDF <docs/papers/popl24_relu_hull_approximation.pdf>`
    :bdg-link-info:`GitHub <https://github.com/UQ-Trust-Lab/WraLU>`
    :bdg-link-info:`Profile <24popl_relu_hull.html>`
    :bdg-link-info:`Live Video <https://youtu.be/dcF6T7y4xkU?t=24061>`

    **Abstract:**
    Convex hulls are commonly used to tackle the non-linearity of activation functions in the verification of neural networks. Computing the exact convex hull is a costly task though. In this work, we propose a fast and precise approach to over-approximating the convex hull of the ReLU function (referred to as the ReLU hull), one of the most used activation functions. Our key insight is to formulate a convex polytope that ”wraps” the ReLU hull, by reusing the linear pieces of the ReLU function as the lower faces and constructing upper faces that are adjacent to the lower faces. The upper faces can be efficiently constructed based on the edges and vertices of the lower faces, given that an n-dimensional (or simply nd hereafter) hyperplane can be determined by an (n−1)d hyperplane and a point outside of it. We implement our approach as WraLU, and evaluate its performance in terms of precision, efficiency, constraint complexity, and scalability. WraLU outperforms existing advanced methods by generating fewer constraints to achieve tighter approximation in less time. It exhibits versatility by effectively addressing arbitrary input polytopes and higher-dimensional cases, which are beyond the capabilities of existing methods. We integrate WraLU into PRIMA, a state-of-the-art neural network verifier, and apply it to verify large-scale ReLU-based neural networks. Our experimental results demonstrate that WraLU achieves a high efficiency without compromising precision. It reduces the number of constraints that need to be solved by the linear programming solver by up to half, while delivering comparable or even superior results compared to the state-of-the-art verifiers.

    .. code-block:: bibtex

        @article{ma2024relu,
          title={ReLU Hull Approximation},
          author={Ma, Zhongkui and Li, Jiaying and Bai, Guangdong},
          journal={Proceedings of the ACM on Programming Languages},
          volume={8},
          number={POPL},
          pages={2260--2287},
          year={2024},
          publisher={ACM New York, NY, USA}
        }

2023
~~~~

.. dropdown:: "Verifying Neural Networks by Approximating Convex Hulls". (Doctoral Symposium).
    **Zhongkui Ma**.
    *2023, International Conference on Formal Engineering Methods (ICFEM'23)*,
    Brisbane, Australia.
    :bdg-link-info:`PDF <https://link.springer.com/chapter/10.1007/978-981-99-7584-6_17>`

    **Abstract:**
    The increasing prevalence of neural networks necessitates their verification in order to ensure security. Verifying neural networks is a challenge due to the use of non-linear activation functions. This work concentrates on approximating the convex hull of activation functions. An approach is proposed to construct a convex polytope to over-approximate the ReLU hull (the convex hull of the ReLU function) when considering multi-variables. The key idea is to construct new faces based on the known faces and vertices by uniqueness of the ReLU hull. Our approach has been incorporated into the state-of-the-art PRIMA framework, which takes into account multi-neuron constraints. The experimental evaluation demonstrates that our method is more efficient and precise than existing ReLU hull exact/approximate approaches, and it makes a significant contribution to the verification of neural networks. Our concept can be applied to other non-linear functions in neural networks, and this could be explored further in future research.

    .. code-block:: bibtex

        @inproceedings{ma2023verifying,
          title={Verifying Neural Networks by Approximating Convex Hulls},
          author={Ma, Zhongkui},
          booktitle={International Conference on Formal Engineering Methods},
          pages={261--266},
          year={2023},
          organization={Springer}
        }

.. dropdown:: "Formalizing Robustness Against Character-Level Perturbations for Neural Network Language Models".
    **Zhongkui Ma**, Xinguo Feng, Zihan Wang, Shuofeng Liu, Mengyao Ma, Hao Guan,
    Mark Huasong Meng.
    *2023, International Conference on Formal Engineering Methods (ICFEM'23)*,
    Brisbane, Australia.
    :bdg-link-info:`PDF <https://link.springer.com/chapter/10.1007/978-981-99-7584-6_7>`
    :bdg-link-info:`GitHub <https://github.com/UQ-Trust-Lab/PdD>`


    **Abstract:**
    The remarkable success of neural networks has led to a growing demand for robustness verification and guarantee. However, the discrete nature of text data processed by language models presents challenges in measuring robustness, impeding verification efforts. To address this challenge, this work focuses on formalizing robustness specification against character-level perturbations for neural network language models. We introduce a key principle of three metrics, namely probability distribution, density, and diversity, for generalizing neural network language model perturbations and meanwhile, formulate the robustness specification against character-level perturbed text inputs. Based on the specification, we propose a novel approach to augment existing text datasets with specified perturbations, aiming to guide the robustness training of language models. Experimental results demonstrate that the training with our generated text datasets can enhance the overall robustness of the language model. Our contributions advance the field of neural network verification and provide a promising approach for handling robustness challenges in neural network language models.

    .. code-block:: bibtex

        @inproceedings{ma2023formalizing,
          title={Formalizing Robustness Against Character-Level Perturbations for Neural Network Language Models},
          author={Ma, Zhongkui and Feng, Xinguo and Wang, Zihan and Liu, Shuofeng and Ma, Mengyao and Guan, Hao and Meng, Mark Huasong},
          booktitle={International Conference on Formal Engineering Methods},
          pages={100--117},
          year={2023},
          organization={Springer}
        }

Journal Papers
--------------

Early Works
~~~~~~~~~~~

The following early works are about
`Social Simulation <https://en.wikipedia.org/wiki/Social_simulation>`_
and
`Agent-based Models <https://en.wikipedia.org/wiki/Agent-based_model>`_
(ABM, implemented by
`Repast Simphony <https://repast.github.io/>`_), supervised by Dr.
`Haixin Ding <http://www7.zzu.edu.cn/glxy/info/1501/5201.htm>`_
[`ORCID <https://orcid.org/0000-0002-6438-7908>`_]
and published during my undergraduate period
(2014-2018).

.. dropdown:: "Does Truthfully-Stating Strategy Really Have its Reward? — Research on the Communication Strategies of Innovation Quality" (Chinese Full Text).
    Haixin Ding, Li Xie, **Zhongkui Ma**.
    2018.
    *Technology Intelligence Engineering*.
    :bdg-link-info:`PDF <#docs/papers/Does Truthfully-Stating Strategy Really Have its Reward.pdf>`

    **Abstract:**
    A multi-phase and multi-state model is constructed at micro level for modeling the diffusion of innovation, and typical innovation quality communication strategies are proposed. Moreover, an Agent-based modeling and simulation technique is also employed to investigate the effects of different innovation quality communication strategies under various settings. The results show that (1) the intuitively appealing truthfully-stating strategy is not rewarding as expected, and from the perspective of specific transaction, over-stating strategy should be adopted, and (2) the dominant satisfaction paradigm in the mainstream marketing is misleading for the choice of innovation quality communication strategies.

.. dropdown:: "Model of Weibo Negative Public Opinion Communication in Colleges and Universities  Based on Double-layer Network" (Chinese Full Text).
    **Zhongkui Ma**.
    2018.
    *Journal of Jiamusi Vocational Institute*.
    :bdg-link-info:`PDF <#docs/papers/Model of Weibo Negative Public Opinion Communication in Colleges and Universities Based on Double-layer Network.pdf>`
    **Abstract:**
    The main body of Weibo students in colleges and universities makes public opinion on and off the line have strong communication power, in order to verify the necessity of implementing offline strategy. In this paper, a negative public opinion propagation model is constructed on the mixed two-layer network structure of WS small-world network and BA scale-free network. The research shows that the implementation of offline strategy helps to reduce the scope and speed of negative public opinion diffusion, and offline strategy should also pay attention to strengthening implementation.


