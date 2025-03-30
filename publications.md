---
layout: page
title: Publications
sidebar_link: True
sidebar_sort_order: 1
---

You can find a complete list beyond this selection on [Google Scholar](https://scholar.google.it/citations?user=AuVp7pkAAAAJ&hl=en).

<style>
    .rounded-box {
        background-color: #f0f0f0;
        padding: 16px;
        margin-bottom: 10px;
        border-radius: 8px;
    }

  summary {
    cursor: pointer;
  }


    br {
   display: block;
   margin: 4px 0;
    }

</style>

## AI-assisted Agent Design

<div class="rounded-box">
    <strong><a href="https://openreview.net/forum?id=or8mMhmyRV" target="_blank">MaestroMotif: Skill Design from Artificial Intelligence Feedback
</a></strong><br>
    Martin Klissarov, Mikael Henaff, Roberta Raileanu, Shagun Sodhani, Pascal Vincent, Amy Zhang, Pierre-Luc Bacon, Doina Precup, Marlos C Machado*, Pierluca D'Oro* <br>
    <em>ICLR (oral) </em>, 2025. <br>
  <!-- <details>
    <summary> <b> Behind the scenes </b> </summary>
  </details> -->
</div>

<div class="rounded-box">
    <strong><a href="https://arxiv.org/abs/2310.00166" target="_blank">Motif: Intrinsic Motivation from Artificial Intelligence Feedback</a></strong><br>
    Martin Klissarov*, Pierluca D’Oro*, Shagun Sodhani, Roberta Raileanu, Pierre-Luc Bacon, Pascal Vincent, Amy Zhang, Mikael Henaff <br>
    <em>ICLR</em>, 2024. <br>
  <!-- <details>
    <summary> <b> Commentary </b> </summary>
    <p> <i> At the beginning of summer 2023, a wave of research works applied Large Language Models to sequential decision-making. This caused both excitement and confusion in me, about which I wrote about in a <a href="https://www.scienceofaiagents.com/p/to-keep-doing-rl-research-stop-calling" target="_blank">blog post</a> that was pivotal for me. Seriously, I wanted to know whether there was something really interesting behind the hype. When Martin joined Meta as an intern, during many days of intense brainstorming, we enumerated the possible ways to use LLMs for decision-making. I got pretty convinced that extracting a reward function from them was the most promising of all. In that particularly long, rainy and confusing summer in Montreal, we pushed ourselves out of our comfort zone and witnessed the potential of LLMs for creating AI agents.  </i> </p>
  </details> -->
</div>

## Reinforcement Learning + Neural Networks

<div class="rounded-box">
    <strong><a href="https://openreview.net/forum?id=OpC-9aBBVJe" target="_blank">Sample-Efficient Reinforcement Learning by Breaking the Replay Ratio Barrier</a></strong><br>
    Pierluca D'Oro*, Max Schwarzer*, Evgenii Nikishin, Pierre-Luc Bacon, Marc G. Bellemare, Aaron Courville <br>
    <em>ICLR (oral)</em>, 2023. <br>

  <!-- <details>
    <summary> <b> Commentary </b> </summary>
    <p> <i>  As the paradigm of increasing performance by scaling the amount of computation was being established in the rest of the machine learning community, we were looking for a way to generalize this to reinforcement learning. Guided by some preliminary evidence we had shown in the primacy bias paper, we thought a way to do it was to increase the amount of updates per environment interaction. I had fun doing some research in which the main goal was not to develop a totally new method or to show good performance really, but to go deep with analyses and to try to empirically understand the implications of different aspects of a complex system. </i> </p>
  </details> -->
</div>

<div class="rounded-box">
    <strong><a href="https://arxiv.org/abs/2205.07802" target="_blank">The Primacy Bias in Deep Reinforcement Learning</a></strong><br>
    Evgenii Nikishin*, Max Schwarzer*, Pierluca D'Oro*, Pierre-Luc Bacon, Aaron Courville <br>
    <em>ICML</em>, 2022. <br>
  <!-- <details>
    <summary> <b> Behind the scenes </b> </summary>
    <p> <i> Evgenii had shared some interesting results on how resetting parameters in neural networks was sometimes giving unexpected performance gains. In a fun scientific sprint, we tried to understand how general the improvements provided by resets were and where they were coming from. Through this project, I understood the huge power of deeply collaborative research and of intuition-guided empirical science. </i> </p>
  </details> -->
</div>

<div class="rounded-box">
  <strong><a href="https://arxiv.org/abs/2309.14597" target="_blank">Policy Optimization in a Noisy Neighborhood: On Return Landscapes in Continuous Control</a></strong><br>
  Nate Rahn*, Pierluca D'Oro*, Harley Wiltzer, Pierre-Luc Bacon, Marc G. Bellemare <br>
  <em>NeurIPS</em>, 2023. <br>
  <!-- <details>
    <summary> <b> Behind the scenes </b> </summary>
    <p> <i> Motivated by new discoveries about the empirical science of deep reinforcement learning, we started discussing techniques for discovering other phenomena and advancing our understanding of neural network-based agents. After some attempts and after building an appropriate experimental framework, we came to the conclusion that the lens of the return landscape was a good one for our goal. Funnily enough, we found some new interesting phenomena right when we stopped searching for them. I learned a lot about how to do understanding-oriented science. </i> </p>
  </details> -->
</div>


## World Models

<div class="rounded-box">
    <strong><a href="https://arxiv.org/abs/2402.05290" target="_blank">Do Transformer World Models Give Better Policy Gradients?</a></strong><br>
    Michel Ma*, Tianwei Ni, Clement Gehring, Pierluca D'Oro*, Pierre-Luc Bacon <br>
    <em>ICML</em>, 2024. <br>
  <!-- <details>
    <summary> <b> Behind the scenes </b> </summary>
    <p> <i> At the beginning of my Master's research work, I really had to learn the hard way how to precisely formalize problems and think in math, since I had realized my drawings of boxes on a whiteboard were not enough anymore to express my scientific self. We had in mind the general goal to learn a model of the dynamics that was tailored to its use in reinforcement learning. We ponderer about what that meant exactly, and got inspired by the ideas of Amir-massoud Farahmand on <a href="https://proceedings.mlr.press/v54/farahmand17a.html" target="_blank">decision-aware model learning</a>. I spent several months staring at a whiteboard and thinking about math for most of my time.
 </i> </p>
  </details> -->
</div>

<div class="rounded-box">
    <strong><a href="https://arxiv.org/abs/2004.14309" target="_blank">How to Learn a Useful Critic? Model-based Action-Gradient-Estimator Policy Optimization</a></strong><br>
    Pierluca D'Oro, Wojciech Jaśkowski <br>
    <em>NeurIPS</em>, 2020. <br>
  <!-- <details>
    <summary> <b> Behind the scenes </b> </summary>
    <p> <i> While living with a daily commute between the wonderful lake city of Como and Switzerland, I tried a bunch of mostly theoretical ideas during my time at NNAISENSE. We found out at some point with my host Wojciech that the ideas I had been thinking about for my master thesis were actually generalizable to actor-critic methods: it implied a simple theory-backed deep reinforcement learning algorithm that yielded good results out-of-the-box. I have established in that occasion, synthesizing my previous experience with what I learned from Wojciech, the core of what would have been my research taste in subsequent years.   </i> </p>
  </details> -->
</div>


<div class="rounded-box">
    <strong><a href="https://arxiv.org/abs/1909.04115" target="_blank">Gradient-Aware Model-based Policy Search</a></strong><br>
    Pierluca D'Oro*, Alberto Maria Metelli*, Andrea Tirinzoni, Matteo Papini, Marcello Restelli <br>
    <em>AAAI</em>, 2020. <br>
  <!-- <details>
    <summary> <b> Behind the scenes </b> </summary>
    <p> <i> At the beginning of my Master's research work, I really had to learn the hard way how to precisely formalize problems and think in math, since I had realized my drawings of boxes on a whiteboard were not enough anymore to express my scientific self. We had in mind the general goal to learn a model of the dynamics that was tailored to its use in reinforcement learning. We ponderer about what that meant exactly, and got inspired by the ideas of Amir-massoud Farahmand on <a href="https://proceedings.mlr.press/v54/farahmand17a.html" target="_blank">decision-aware model learning</a>. I spent several months staring at a whiteboard and thinking about math for most of my time.
 </i> </p>
  </details> -->
</div>

