---
layout: post
title: "Transmit Knowledge, not Behaviors: the Primacy Bias and the Evolutionary Value of Death"
mathjax: true
categories:
  - Home
tags:
  - machine learning
  - philosophy
  - evolution
hide: false
---
Reinforcement Learning is about maximizing a reward signal from the environment. Since rewards come from the actions of an agent, reinforcement learning is really about learning reward-maximizing _behaviors_.
But an agent seeking effective behaviors should at the same time acquire _knowledge_ about the environment, in a never-ending cycle: a more interesting behavior potentially leads to new knowledge, that in turn unlocks the possibility to refine existing behaviors or learn new ones.

This back and forth between knowledge and behavior seems to be an important feature of any system that learns by interacting with the world. Thus, it is natural to think that _where_ behaviors and knowledge are stored and _how_ they are updated is a defining property for any, natural or artificial, agent.

Human beings store their behavioral capabilities, or the sensorimotor and decision-making ability to take an action given a state, in their brain. They also store a part of their knowledge about the world in the same place; memories about what they have seen in the past, as well as information about how the world generally works.

It is known, however, that a significant portion of the knowledge of human beings, as well as the one of other animals, is not condemned to stay enclosed into an individual's brain forever.
I am referring to _culture_, knowledge passed from individual to individual, across the boundaries defined by brains or by generations.
In humans, the storage location of knowledge not only overcomes the boundaries of an individual, passing from a brain to the other, but also the physical boundaries of our bodies.
We use paper, pens, hard drives, vinyls to encode and transmit knowledge and make sure that it can flow through time.
This additional storage of knowledge is beneficial for the individual, that can use that to recall more easily and augment its cognition, but more importantly for the entire species, that can take advantage of the knowledge created by potentially very different individuals in potentially very different time frames.

In many modern reinforcement learning algorithms, we find again this separation between "stored knowledge" and behavior.
What is a _control policy_, the artificial neural network that determines the actions to execute in the environment, if not the locus of behaviors? And what is a _replay buffer_, the memory that stores the history of an agent's experiences, if not the main locus of knowledge?
In our recent work, we discovered that when a reinforcement learning agent learns a sub-optimal behavior from an incomplete knowledge of the world, it is difficult for standard algorithms to naturally update this behavior to a better one, even after the state of knowledge has improved.
Despite the locus of knowledge, the replay buffer, contains enough information to update the one present in the locus of behavior, learning algorithms are not able to take advantage of it, resulting in poor long-term performance.
We like to call this effect **the primacy bias** in reinforcement learning, which corresponds to similar phenomena that has been observed in human behavior for a long time.

It is possible to overcome the primacy bias in this class of algorithms through a simple solution: if the knowledge is theoretically sufficient for an improvement, but the combination of learning algorithm and current behavior does not allow it, it would seem natural for an agent to forget part of its behavior and try to learn from existing knowledge right after it. In the context of reinforcement learning, this implies re-initializing at least part of the control policy while still continuing to learn from an intact replay buffer.
A simple reset pattern such as a periodic one is enough for an agent to significantly improve its performance.
Indirectly, this allows an agent to be more efficient, since it can more aggressively extract a behavior from its existing knowledge without significant fear of being affected by the primacy bias.

One might wonder: since humans share part of the separation in loci of behavior and knowledge with this kind of reinforcement learning systems, is there any existing mechanism employed in human learning which reminds us of the one described above?
Forgetting happens in the brain of an individual, but probably not in a style which is as brutal as the one corresponding to the periodic re-initialization of artificial neural networks.
However, there is a more abrupt and extreme forgetting mechanism employed by our species: when a human generates a child and then dies, it naturally propagates a core of behavior through the genetic material, but a large part of it will be learned by the child, the new human, based on the environment.
The new human can infer the correct behaviors from multiple sources. First, from the knowledge naturally collected in the environment; second, from the knowledge transmitted by parents and other individuals; third, from the knowledge stored in physical supports such as books and chips.

Since knowledge accumulates across generations, the new human has access, on average, to a greater amount of knowledge with respect to the one of the parent. Primacy bias effects equivalent to the ones observed in reinforcement learning could mean that the parent is not able to extract a good behavior from the additional information that has been collected during the lifetime; if a child is similar to a partially re-initialized version of a parent, it means that new humans could instead be able to learn useful behaviors from the same information, if correctly transmitted.

If we push this reasoning to its extreme, we can use it as an evolutionary justification to one of the phenomena that intuitively seem against the fundamental principia behind evolution: death by ageeing. Let's take Richard Dawkin's selfish gene perspective, in which the goal of evolution is not the survival of the individual, but of the gene, and let's reflect on the fact that, in a sense or another, every environment is resource-constrained.

As in reinforcement learning with data-intensive updates, primacy effects can be convenient for fast adaptability to new situations with partial knowledge, but they lead to ignoring the new information in the long run. The resource constraints of an environment would push evolution to provide more resources to the younger humans, able to extract behaviors in the most effective way from the knowledge accumulated up to that point across generations.

And which is the most effective way for evolution to give more resources to younger individual, not affected as much as the old ones by the primacy bias? It is to give a finite, not too long, lifespan to humans. Thanks to the primacy bias, parents were very effective at learning from limited interactions; but due to it, they have harder time efficiently improving their behaviors given the new knowledge. Their children can instead learn better behaviors from the same knowledge, and start collecting new knowledge as part of society. At some point, however, they will start to be affected by the negative effects of the primacy bias, becoming incapable of fully leveraging the freshly-generated knowledge. Taking advantage of that is going to be the job of their children.


_Thanks to Evgenii Nikishin for proof-reading an initial version of this blog post. Read our [paper on the primacy bias in reinforcement learning](https://arxiv.org/abs/2205.07802) to learn more about the RL implications of the primacy bias._