---
layout: single
title: Neuromorphic Computing for Cybersecurity?
date: 2025-06-27
author_profile: true
read_time: true
tags:
  - neuromorphic
  - cybersecurity
image: /assets/images/brain-with-neuron-node.png
excerpt: An introduction to neuromorphic computing including a brief discussion on its implications for cybersecurity.
---

{% include figure
  image_path="/assets/images/brain-with-neuron-node.png"
  caption="Brain[1]"
  alt="Brain with connected neuron nodes visual"
%}

### What is Neuromorphic Computing?

Neuromorphic computing is the exciting field of developing systems that mimic how the brain works.

You may be familiar with more traditional Artificial Neural Networks (ANNs) that do take inspiration from our brain's Biological Neural Networks (BNNs) and treat computational units as neurons in a network. This approach has led to many breakthroughs including the recent Large Language Model (LLM) boom; names like ChatGPT, Gemini, and Claude have become ubiquitous.

One way that ANNs often differ from BNNs is that in many traditional ANNs such as multi-layer-perceptrons, neurons are densely connected. This combined with the traditional design choice of having every neuron activate in every propagation cycle, means that many connections are active simultaneously which leads to high energy consumption.

One proposed solution to this issue is neuromorphic computing, and specifically developing Spiking Neural Networks (SNNs) which stay more faithful to BNNs. SNNs accumulate input over time and only 'fires' (or 'spikes') once the accumulation reaches a threshold. This is analogous to how in our brain, neurons only activate when they reach a certain electrical excitement threshold. This means that neurons only activate in response to relevant stimuli, leading to event driven computation and energy efficiency.

Neuromorphic hardware designs physical systems that stay true to the human brain. These systems are inherently suited to run SNNs more efficiently. Notable neuromorphic hardware projects include Intel's Loihi Chip, IBM's NorthPole Chip, and the University of Manchester's SpiNNaker Large-Scale Neuromorphic Machine.

{% include figure
  image_path="/assets/images/snn-schematic-with-inhibitory-nodes.png"
  caption="Schematic of a spiking neural network (SNN) with excitatory and inhibitory neurons. Inhibitory neurons work against excitatory neurons, helping regulate neuron activity and prevent unnecessary activation. [2]"
  alt="Spiking neural network with labeled excitatory and inhibitory neurons"
%}

### Advantages of Neuromorphic Computing

- Energy Efficiency: In SNNs since neurons only activate when a spike threshold is reached, the system saves energy. It should be noted that these savings are most notable when SNNs are run on neuromorphic hardware. Otherwise when run on traditional CPUs/GPUs, the gains in energy efficiency may not be significant.
- Low Latency: SNNs are asynchronous and event-based which makes them inherently suited for parallel processing. Since many different operations can be completed concurrently, overall speed improves.
- Time-based Tasks: SNNs naturally encode and process time-based information through spikes, this means tasks that need a sense of temporal dynamics, such as gesture recognition and speech recognition/generation, may be very suited for neuromorphic computing methods.

### Disadvantages of Neuromorphic Computing

- Training Difficulty: Due to being a less mature field than traditional ANNs, SNNs can be difficult to train with less options for tooling and methods. For example, since spiking functions are non-differentiable, standard backpropagation is not possible. However, surrogate gradient descent methods are actively being explored to enable backpropagation-like training.
- Steep Learning Curve: There is a need to understand multiple domains such as neuroscience and computer science deeply to be able to further neuromorphic computing. Because of this, there is a steep knowledge barrier.

### Possible Implications for Cybersecurity

As a cybersecurity enthusiast, I would be remiss not to mention the security implications of neuromorphic computing. They include:

- Threat Detection: It has been shown that neuromorphic computing excels at pattern recognition tasks [3, 4], possibly from the notion that SNNs try to replicate our brain's plasticity. This ability can be applied in the realm of (automated) threat detection.
- Adaptive Access Control: SNNs may be well-suited to learn from user behaviour over time and adjust trust levels based on context like time and location to restrict access behind more layers of authentication.
- Additional Attack Vectors: Although new technologies like SNNs will help defensive systems, malicious actors can also utilise similar technologies to try and develop new angles and methods of attacks. For example, it may be possible for attackers to use neuromorphic computing to simulate human behaviour in order to bypass traditional anomaly detection systems.

### Final Thoughts

Neuromorphic computing brings a wealth of new possibilities and areas to explore, in particular for the kind of mind that enjoys learning about many different fields and trying to combine them. I would like to think of myself as in this category.

This autumn, I will be starting the third year of my Computer Science undergraduate degree at the University of Manchester, home of SpiNNAker, one of the world's most prominent pieces of neuromorphic hardware. I hope to combine neuromorphic computing and cybersecurity for my third year project (more on this in a later post) and cannot be more excited to contribute to these growing and exciting fields.
### References

1. Alex Shuper [Unsplash](https://unsplash.com/photos/a-computer-generated-image-of-a-human-brain-8-zt2nE-vnk)
2. Guo et al. (2020) *Towards Efficient Neuromorphic Hardware: Unsupervised Adaptive Neuron Pruning* [Researchgate](https://www.researchgate.net/publication/342529143_Towards_Efficient_Neuromorphic_Hardware_Unsupervised_Adaptive_Neuron_Pruning)
3. Christophe et al. (2015) *Pattern recognition with Spiking Neural Networks: a simple training method* [Researchgate](https://www.researchgate.net/publication/281846764_Pattern_recognition_with_Spiking_Neural_Networks_a_simple_training_method)
4. Yokouchi et al. (2022) *Pattern recognition with neuromorphic computing using magnetic field–induced dynamics of skyrmions*. [ScienceAdvances](https://www.science.org/doi/10.1126/sciadv.abq5652)







