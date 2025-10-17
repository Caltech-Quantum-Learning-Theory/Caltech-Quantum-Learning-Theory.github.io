---
layout: default
---

# Ph 220: Quantum Learning Theory (Fall 2025)

**Class meetings:** Monday & Wednesday, 1:00pm-2:20pm in Hameetman Auditorium, Cahill Center for Astronomy and Astrophysics.

---

## Overview

This course covers quantum learning theory, a contemporary field at the intersection of quantum mechanics, quantum computing, statistical learning theory, and machine learning. The fundamental questions explored include: how to efficiently learn quantum many-body systems? When can quantum machines learn and predict better than classical machines? What physical phenomena can quantum machines learn and discover? The course aims to develop rigorous theoretical foundations for understanding how scientists, machines, and future quantum computers can learn and discover new phenomena in our quantum-mechanical universe.

---

## Instructor & TAs

#### Instructor
* **Hsin-Yuan (Robert) Huang**
* **Email:** `hsinyuan@caltech.edu`
* **Office hours:** Monday 2:20pm-2:50pm & Wednesday 12:30pm–1:00pm

#### Teaching Assistant
* **Haimeng Zhao**
* **Email:** `haimeng@caltech.edu`
* **Office hours:** Wednesdays 4:00pm-5:00pm in East Bridge 307 (on weeks when homework is due), or by appointment.

---

## Topics to be Covered

* From quantum sensing to quantum learning (sensing magnetic field, standard quantum limit, Heisenberg limit)
* Review of quantum many-body physics (local Hamiltonians, ground states, Gibbs states, tensor network, short-range entangled states)
* Random unitaries (t-designs, Weingarten calculus, path-recording oracle)
* Learning the description of a quantum state (randomized measurements, pretty good measurements, sample-optimal tomography)
* Predicting properties of a quantum state (classical shadow, matrix multiplicative weight, online learning, quantum threshold search)
* Learning special families of states
* Hardness of learning (pseudorandom states, pseudorandom unitaries, hardness of classifying phases of matter)
* Quantum advantage in learning (learning tree formalism, lower bounds, predicting properties, quantum PCA)
* Quantum neural networks (barren plateau, generative quantum advantage)

---

## Course Timeline & Materials 🗓️

### **Week 1**

#### **Lecture 1: Introduction to Sensing & Learning (Mon, Sep 29)**
* **Summary:** We introduced the fundamental problem of sensing a magnetic field with a spin sensor, which serves as a simple model for understanding the core principles of quantum learning.
* **Lecture Notes:** [Digitized Notes: From Quantum Sensing to Learning](./materials/Note_From_Quantum_Sensing_to_Learning.pdf)
* **Reading & Resources:**
    - **Background Reading:** To begin, please read the [Preface](./materials/Preface.pdf) and [Ch. 1: Sneak Peek](./materials/Chapter-SneakPeek.pdf). For a refresher on quantum mechanics, review [Ch. 2: Quantum Mechanics](./materials/Chapter-QuantumMechanics.pdf).
    - **Concentration Inequalities:** A good starting point is [Markov's inequality](https://en.wikipedia.org/wiki/Markov%27s_inequality), which leads to more powerful tools like [Hoeffding's inequality](https://en.wikipedia.org/wiki/Hoeffding%27s_inequality).
    - **Inequalities Cheat Sheet:** A useful reference for inequalities can be found [here](https://www.lkozma.net/inequalities_cheat_sheet/ineq.pdf).
    - **Improved Sensing Analysis:** The sensing time can be tightened. A more detailed analysis using "Robust Phase Estimation" is in Section V of [this paper](https://arxiv.org/pdf/1502.02677).

#### **Lecture 2: Sensing Lower Bounds & Quantum Many-Body Physics (Wed, Oct 1)**
* **Summary:** We established a lower bound on sensing time, concluding our analysis of the magnetic field problem. We then reviewed quantum many-body physics from a quantum information perspective, covering local Hamiltonians, ground states, and tensor networks.
* **Lecture Notes:** [Digitized Notes: From Quantum Sensing to Learning](./materials/From_Quantum_Sensing_to_Learning.pdf)
* **Reading & Resources:**
    - **Tensor Networks:** To understand the basic definitions and notation of tensor networks, read [Ch. 3: Tensor Networks](./materials/Chapter-TensorNetwork.pdf).
    - **Tensor Decomposition:** To see how a single tensor can be decomposed via SVD, review the [Bonus Note: Tensor Networks & SVD](./materials/BonusLecture-SVDandTN.pdf).
    - **Exercises:**
        1.  Prove that any 1D short-range entangled state can be represented as a Matrix Product State (MPS).
        2.  Prove that simulating a Z-basis measurement on an MPS with a polynomial bond dimension is classically efficient.

---

### **Week 2**

#### **Lecture 3: 1D Simulation & Complexity Classes (Mon, Oct 6)**
* **Summary:** We finished the classical simulation for sampling from 1D short-range entangled states and 1D shallow quantum neural networks using their Matrix Product State (MPS) representation. We also reviewed key complexity classes to establish that `PostBPP ≠ PostBQP`, assuming the Polynomial Hierarchy (PH) does not collapse.
* **Lecture Notes:**
    * [Digitized Notes: Classical Simulation & Complexity Review](./materials/Note_Review_of_Quantum_Complexity.pdf)
    * These notes provide an **algebraic proof** for the classical simulation of sampling from a 1D MPS, which is an alternative to the graphical proof from class.
    * They also include discussions to build intuition for why the Polynomial Hierarchy is believed not to collapse, covering topics like **NP vs. coNP** and the containment of **coNP in P^NP**.

#### **Lecture 4: Quantum Advantage in 2D & Intro to Tomography (Wed, Oct 8)**
* **Summary:** We used the conjecture that the Polynomial Hierarchy (PH) does not collapse, which implied `PostBPP ≠ PostBQP`, to establish classical hardness in simulating 2D short-range entangled states and 2D shallow QNNs. This shows a surprising sharp transition from 1D to 2D and provides the complexity-theoretic foundation for quantum advantages in shallow QNNs. We then began our journey to develop efficient algorithms for learning and predicting properties of unknown quantum systems.
* **Lecture Notes:**
    * [Digitized Notes: Review of Quantum Many-Body Physics](./materials/Note_Review_of_Quantum_Complexity.pdf)
    * [Digitized Notes: Learning and Predicting Properties of a Quantum State](./materials/Note_Learning_Predicting_States.pdf)

---

### **Week 4**

#### **Lecture 5: Randomized Measurements & Weingarten Calculus (Mon, Oct 13)**
* **Summary:** We introduced the randomized measurement scheme, defined Haar-random unitaries, and derived the famous Weingarten calculus using Schur-Weyl duality to analyze moments of Haar-random unitaries. This calculus is a powerful tool with broad applications, from randomized benchmarking to black hole physics.
* **Lecture Notes:**
    * [Digitized Notes: Learning and Predicting Properties of a Quantum State](./materials/Note_Learning_Predicting_States.pdf)

#### **Lecture 6: Predicting Properties via Randomized Measurements (Wed, Oct 15)**
* **Summary:** We built on Weingarten calculus to show how to predict many properties of an unknown quantum state from very few measurements. The protocol covered was the original classical shadow tomography based on random Clifford circuits.
* **Lecture Notes:**
    * [Digitized Notes: Learning and Predicting Properties of a Quantum State](./materials/Note_Learning_Predicting_States.pdf)
* **Reading & Resources:**
    * **Full Classical Shadow Formalism:** [Classical Shadows (Nature Physics)](./materials/Classical-Shadows-Nature-Physics.pdf)
    * **Probability Review:** For those unfamiliar with concentration inequalities or median-of-means, you can review this short note: [Bonus Lecture: Concentration Inequalities and Median of Means](./materials/BonusLecture-MedianOfMeans.pdf)


---

## Homeworks

There will be **five problem sets** for this course. The grade will be based on the correctness, completeness, and clarity of your proofs.

#### Homework Due Dates:
1.  **[HW 1](./materials/PSET_1_Caltech_Ph_220.pdf):** Friday, October 17th
2.  **HW 2:** Friday, October 31st
3.  **HW 3:** Friday, November 14th
4.  **HW 4:** Friday, November 28th
5.  **HW 5:** Friday, December 12th