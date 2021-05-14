<!-- Preamble with CSS style sheet TODO: Find way to put this in external CSS sheet.--> 
<link href="06-may-21-Blockchain-vulnerabilities.css" rel="stylesheet"></link> 

## Table of Contents
- [Introduction](#introduction)
- [Technical Sneak Peek](#technical-sneak-peek)
  - [Shor's Algorithm](#shors-algorithm)
  - [Grover's Algorithm](#grovers-algorithm)
  - [Consensus Mechanisms in Blockchain](#consensus-mechanisms-in-blockchain)
  - [Signature Schemes in Blockchain Networks.](#signature-schemes-in-blockchain-networks)
- [Attacks](#attacks)
  - [A 51 percent attack](#a-51-percent-attack)
  - ['Steal' Attacks](#steal-attacks)
- [Closure](#closure)
  - [Conclusion](#conclusion)
  - [Honorable Mentions](#honorable-mentions)


# Introduction

Today I will be reviewing the , "*Vulnerability of  Blockchain Technologies to Quantum Attacks*". This paper reflects the ethos of I want to do through this series, [**Paper of the Day**](https://isolatedinfo.space/paper-of-the-day). Blockchain is more relevant than quantum systems to the layman. The financial significance of Blockchain through cryptocurrencies warrants a deeper dive into the security of these systems. Adoption of Blockchain further into society will increase in the coming years.  Adopting the principle of *Prevention is better than cure*, it is pertinent to look at the shortfalls in the implementations of blockchain systems. 

In [today's paper][1], the authors *Kierney, Perez-Delgado* discuss the shortfalls of blockchain systems against attacks that leverage cleverly desgined quantum algorithsm that provide speedups for certain problems vis-a-vis a traditional computer. However, it must be noted that these types of attacks are only a subset of the set of all possible attacks and must be protected against those two. The authors mention some articles that give an insight into blockchain vulnerabilities in general. The below table presents these articles discussed therein. 


<table style="width:75%; margin:auto; background-color:crimson; border: 1px solid white; border-radius: 0px; ">
  <tr>
    <th>The Paper</th>
    <th>Attack Type</th>
  </tr>
  <tr>
    <td>Dummy</td>
    <td>Dummy</td>
  </tr>
  <tr>
    <td>Dummy</td>
    <td>Dummy</td>
  </tr>
 <caption style="caption-side:bottom"><b>Table 1</b>:  Articles on various types of Blockchain attacks</caption>
</table>
</br>
<div class="boxed" style="background-color:DarkMagenta"> 
<b>What is a Quantum Attack ?</b></br> 
The use of quantum computing systems that leverage computational speedups achieved through the clever use of inherent properties of a quantum system (Superposition, Entanglement) to break cryptographic protocols that secure a system would constitute a quantum attack. 
</div></br>
  
Prior to looking at the details of some possible attacks let us look at why where the vulnerabilities lie in a blockchain network. For a transaction to be added onto the blockchain network, some conditions must be satisfied by the actors on the networks. We shall refer to the actors with a stake on the transaction as: Sender, Receiver, Miner, Attacker. 


# Technical Sneak Peek
Here on, I shall introduce you to more technical aspects of the quantum algorithms and blockchain schemes. While doing so, it will become clearer on how quantum systems could make blockchain networks vulnerable. Let's start with the a seminal quantum algorithm that accelerated the growth of Quantum Information Science, *Shor's Algorithm*

## Shor's Algorithm
Peter Shor, a mathematcian at MIT, came up with an algorithm in 1994 that leverages quantum computers to speed up the prime factorisation problem. The prime factorisation problem represents a simple example of a [`trapdoor function`](https://en.wikipedia.org/wiki/Trapdoor_function).

<div class="boxed" style="background-color: HotPink">
<b> <u>Trapdoor Function</u></b> : </br>
A *trapdoor function* is a function that is easy to compute in one direction while it's inverse function is very difficult to compute. </br>
<i>Example: </i> Given two large prime numbers, say <code>a = 1039, b = 1039</code>, it is easy to calculate their product <code> c = 10792521</code>. On the other hand, given <code> c </code>, it is difficult to find its prime factors as <code> a and b </code>
</div>

Although this particular number can be factorised in a computer with ease, larger numbers beyond threshold have been found to be unfactorisable in useful time by supercomputers too. 
## Grover's Algorithm 
## Consensus Mechanisms in Blockchain 
## Signature Schemes in Blockchain Networks. 

# Attacks
## A 51 percent attack 
## 'Steal' Attacks

# Closure

## Conclusion

## Honorable Mentions
Every iteration of a post in this series, I select a set of a articles that I would like to write about. Of these, a paper is chosen usually based on my mood at the time of choosing and the rest are just given a cursory glance. For those interested here is a list of the papers, that I considered this week. The papers considerd for this blog are usually from the [`quant-ph`](https://arxiv.org/quant-ph) section of ArXiV. 

<details>
<summary> <a href="https://arxiv.org/abs/2105.01760">Error Mitigation in Quantum Computers through Instruction Scheduling</a></summary>
<div class="deets">
<i>Abstract</i>: 
Current quantum devices suffer from the rapid accumulation of error that prevents the storage of quantum information over extended periods. The unintentional coupling of qubits to their environment and each other adds significant noise to computation, and improved methods to combat decoherence are required to boost the performance of quantum algorithms on real machines. While many existing techniques for mitigating error rely on adding extra gates to the circuit or calibrating new gates, our technique leverages the gates already present in a quantum program and does not extend circuit runtime duration. In this paper, we exploit scheduling time for single-qubit gates that occur in idle windows, scheduling the gates such that their timing can counteract some errors.
Spin-echo corrections act as inspiration for this technique, which can mitigate dephasing, or phase accumulation, that appears as a result of qubit inactivity. Theoretical models, however, fail to capture all sources of noise in near-term quantum devices, making practical solutions necessary that better minimize the impact of unpredictable errors in quantum machines. This paper presents TimeStitch: a novel framework that pinpoints the optimum execution schedules for single-qubit gates within quantum circuits. TimeStitch, implemented as a compilation pass, leverages the reversible nature of quantum computation to improve the success of quantum circuits on real quantum machines. Unlike past approaches that apply reversibility properties to improve quantum circuit execution, TimeStitch boosts fidelity without violating critical path frontiers in either the slack tuning procedures or the final rescheduled circuit. On average, TimeStitch is able to achieve 24% improvement in success rates, with a maximum of 75%, while observing depth criteria.
</div>
</details>

<details>
<summary> <a href="https://arxiv.org/abs/2105.02074">Relating disturbance, information and orthogonality</a></summary>
<div class="deets">
<i>Abstract</i> :
In the general theory of quantum measurement, one associates a positive semidefinite operator on a d-dimensional Hilbert space to each of the n possible outcomes of an arbitrary measurement. In the special case of a projective measurement, these operators are pairwise Hilbert--Schmidt orthogonal, but when n>d, orthogonality is restricted by positivity. This restriction has consequences which are not present from a classical perspective; in particular, we find it allows us to more precisely state the old quantum adage that it is impossible to extract information from a system without disturbance. Restricting attention throughout to the Lüders state updating rule, we consider three properties of a measurement: its disturbance, a measure of how the expected post-measurement state deviates from the input state, its purity gain, a measure of the expected reduction of uncertainty resulting from measurement, and its orthogonality, a measure of the degree to which the measurement operators differ from an orthonormal set. We show that these quantities satisfy a simple algebraic relation amounting to an expression of an information-disturbance trade-off. Finally, we assess several classes of measurements on these grounds and identify symmetric informationally complete quantum measurements as the unique quantum analogs of a perfectly informative and nondisturbing classical ideal measurement.
</div>
</details>

<details>
<summary> <a href="https://arxiv.org/abs/2105.01815
">Vulnerability of Blockchain Technologies to Quantum Attacks</a></summary>
<div class="deets">
<i>Abstract</i> :
Quantum computation represents a threat to many cryptographic protocols in operation today. It has been estimated that by 2035, there will exist a quantum computer capable of breaking the vital cryptographic scheme RSA2048. Blockchain technologies rely on cryptographic protocols for many of their essential sub-routines. Some of these protocols, but not all, are open to quantum attacks. Here we analyze the major blockchain-based cryptocurrencies deployed today -- including Bitcoin, Ethereum, Litecoin and ZCash, and determine their risk exposure to quantum attacks. We finish with a comparative analysis of the studied cryptocurrencies and their underlying blockchain technologies and their relative levels of vulnerability to quantum attacks.
</div>
</details>


<details>
<summary> <a href="https://arxiv.org/abs/2105.00418">QuNet: Cost vector analysis & multi-path entanglement routing in quantum networks]</a></summary>
<div class="deets">
<i>Abstract</i> :
Entanglement distribution will form the backbone of many future distributed quantum
technologies, especially the quantum internet. The act of purifying multiple noisy entangled states into a single one of higher quality has no analogue in classical networking and
as such, this transforms the way in which we will consider future algorithms for routing
entanglement. We outline the differences that arise because of this, demonstrate some
elementary formalisms for ‘multi-path entanglement routing’, and discuss the philosophical differences that arise when comparing this regime to conventional digital network
theory. We also present a software package, QuNet, that uses novel ‘quantum cost-vector
analysis’ to simulate and benchmark routing in multi-user entanglement networks in
a way that is is highly scalable in network size and the number of competing users.
Our software accommodates both ground- and space-based networks, and implements
efficient multi-user time-optimisation for mitigating congestion when quantum memories
are available.
</div>
</details>

<details>
<summary><a href="https://arxiv.org/abs/2105.00080">Entangling Quantum Generative Adversarial Networks
</a></summary>
<div class="deets">
<i>Abstract</i> :
Generative adversarial networks (GANs) are one of the most widely adopted semisupervised and
unsupervised machine learning methods for high-definition image, video, and audio generation. In
this work, we propose a new type of architecture for quantum generative adversarial networks (entangling quantum GAN, EQ-GAN) that overcomes some limitations of previously proposed quantum
GANs. Leveraging the entangling power of quantum circuits, EQ-GAN guarantees the convergence
to a Nash equilibrium under minimax optimization of the discriminator and generator circuits by
performing entangling operations between both the generator output and true quantum data. We
show that EQ-GAN has additional robustness against coherent errors and demonstrate the effectiveness of EQ-GAN experimentally in a Google Sycamore superconducting quantum processor. By
adversarially learning efficient representations of quantum states, we prepare an approximate quantum random access memory (QRAM) and demonstrate its use in applications including the training
of quantum neural networks.
</div>
</details>








[1]:https://arxiv.org/abs/2105.01815

