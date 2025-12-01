---
layout: default
---

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

### **Week 3**

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
### **Week 4**

#### **Lecture 7: Randomized Measurements & Quantum Data Analysis (Mon, Oct 20)**
* **Summary:** We concluded our chapter on randomized measurements, covering efficient prediction in the low-measurement regime and sample-optimal tomography in the high-measurement regime. We also found that predicting certain observables (like Pauli) is exponentially hard with single-copy measurements, a limitation we'll overcome later with quantum data analysis. We then introduced quantum data analysis, showing how coherent, entangling measurements can predict properties while protecting the quantum state.
* **Lecture Notes:**
    * [Digitized Notes: Learning and Predicting Properties of a Quantum State](./materials/Note_Learning_Predicting_States.pdf)
    * [Digitized Notes: Protecting Quantum Data](./materials/Note_Protecting_Quantum_Data.pdf)

#### **Lecture 8: Gentle Measurement & Quantum Threshold Search (Wed, Oct 22)**
* **Summary:** We continued developing our toolkit for protecting quantum data while using them. Building on Problem Set 1, we derived the powerful **Gentle Measurement Lemma** and the **Quantum Union Bound**. We concluded with an introduction to Quantum Threshold Search, a key tool for extracting information from quantum data with minimal disturbance.
* **Lecture Notes:**
    * [Digitized Notes: Protecting Quantum Data](./materials/Note_Protecting_Quantum_Data.pdf)

---
### **Week 5**

#### **Lecture 9: Online Machine Learning (Mon, Oct 27)**
* **Summary:** We focused on Online Machine Learning, starting with the classical "prediction with experts" problem. We derived the "Follow the Regularized Leader" (FTRL) algorithm, which led to the Multiplicative Weight Update (MWU) rule, and showed it achieves sublinear regret. We then generalized this entire framework to the quantum domain.
* **Lecture Notes:**
    * [Digitized Notes: Protecting Quantum Data](./materials/Note_Protecting_Quantum_Data.pdf)

#### **Lecture 10: Full Shadow Tomography (Wed, Oct 29)**
* **Summary:** We developed an advanced version of Quantum Threshold Search to check if an observable is "close to" or "far from" a value while protecting the data. By combining this with our online learning tools for quantum states, we built the **Full Shadow Tomography** protocol, which can predict any M observables using only n poly(log M) samples.
* **Lecture Notes:**
    * [Digitized Notes: Protecting Quantum Data](./materials/Note_Protecting_Quantum_Data.pdf)

---
### **Week 6**

#### **Lecture 11: Learning Quantum Neural Networks (Mon, Nov 3)**
* **Summary:** We shifted focus to practical applications, specifically the difficulty of training QNNs. We examined failure mechanisms like barren plateaus, indistinguishability from random unitaries, and exponentially many bad local minima. We then introduced **parameterization by local inversion** as the missing ingredient for efficient learning.
* **Lecture Materials:**
    * [Slides: Learning QNNs](./materials/Slides-Learning-QNNs.pdf)
    * [Digitized Notes: Learning QNNs and SRE States](./materials/Note_Learning_QNN_SRE.pdf)  

#### **Lecture 12: Generative Quantum Advantage & SRE States (Wed, Nov 5)**
* **Summary:** We explored the complete solution for learning QNNs, including "sewing" local inversions to reconstruct shallow quantum circuits and short-range entangled (SRE) states. We demonstrated applications in establishing **generative quantum advantage** and compressing deep physical dynamics into low-depth circuits.
* **Lecture Materials:**
    * [Slides: Generative Quantum Advantage](./materials/Slides-Generative-Quantum-Advantage.pdf)
    * [Digitized Notes: Learning QNNs and SRE States](./materials/Note_Learning_QNN_SRE.pdf)

---
### **Week 7**

#### **Lecture 13: Learning Noisy Quantum Devices (Mon, Nov 10)**
* **Summary:** We explored the characterization of noisy devices, discussing the fundamental gauge freedom and the systematic approach of **Gate Set Tomography**. We also covered **noise twirling** to transform arbitrary channels into simple Pauli channels.
* **Lecture Materials:**
    * [Digitized Notes: Learning Noisy Quantum Device](./materials/Note_Learning_Noisy_Quantum_Device.pdf)

#### **Lecture 14: Learning Many-Body Hamiltonians (Wed, Nov 12)**
* **Summary:** We studied how to learn many-body Hamiltonians with **Heisenberg-limited scaling**. We developed the "reshaping" technique to simplify Hamiltonians into isolated islands of few-qubit Hamiltonians and combined this with quantum sensing protocols.
* **Lecture Materials:**
    * [Digitized Notes: Learning Many-Body Hamiltonians](./materials/Note_Learning_Many-Body_H.pdf)

---
### **Week 8**

#### **Lecture 15 & 16: Hardness of Learning & Pseudorandom States (Mon, Nov 17 & Wed, Nov 19)**
* **Summary:** We tackled the fundamental question of learning hardness. We demonstrated the existence of **Pseudorandom States (PRS)**: simple quantum states that are indistinguishable from Haar-random states by any polynomial-time quantum algorithm.
* **Lecture Materials:**
    * [Digitized Notes: Hardness of Learning and PRS](./materials/Note_PRS.pdf)
    * *Update:* The notes have been expanded to include foundations of statistical distinguishability, trace distance analysis, and the complete derivation of PRS existence.

---
### **Week 9**

#### **Lecture 17 & 18: Pseudorandom Unitaries (Mon, Nov 24 & Wed, Nov 26)**
* **Summary:** We proved the existence of **Pseudorandom Unitaries (PRU)**, a problem that had remained open since 2017 and closed in 2024. The proof utilizes tools from random unitaries, post-quantum cryptography, and purification.
* **Lecture Materials:**
    * [Digitized Notes: Pseudorandom Unitaries](./materials/Note_PRU.pdf)
    * *Update:* This file contains the full proof completed in Lecture 18.

---

## Homeworks

There will be **five problem sets** for this course. The grade will be based on the correctness, completeness, and clarity of your proofs.

#### Homework Due Dates:
1.  **[HW 1](./materials/PSET_1_Caltech_Ph_220.pdf):** Friday, October 17th
2.  **[HW 2](./materials/PSET_2_Caltech_Ph_220.pdf):** Friday, October 31st
3.  **[HW 3](./materials/PSET_3_Caltech_Ph_220.pdf):** Friday, November 14th
4.  **[HW 4](./materials/PSET_4_Caltech_Ph_220.pdf):** Friday, November 28th
5.  **[HW 5](./materials/PSET_5_Caltech_Ph_220.pdf):** Friday, December 12th