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
* **Lecture Notes:** [Digitized Notes: From Quantum Sensing to Learning](./materials/From_Quantum_Sensing_to_Learning.pdf)
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
    - **Tensor Decomposition:** To see how a single tensor can be decomposed via SVD, review the [Bonus Lecture: Tensor Networks & SVD](./materials/BonusLecture-SVDandTN.pdf).
    - **Exercises:**
        1.  Prove that any 1D short-range entangled state can be represented as a Matrix Product State (MPS).
        2.  Prove that simulating a Z-basis measurement on an MPS with a polynomial bond dimension is classically efficient.

---

## Homeworks

There will be **five problem sets** for this course. The grade will be based on the correctness, completeness, and clarity of your proofs.

#### Homework Due Dates:
1.  **HW 1:** Friday, October 17th
2.  **HW 2:** Friday, October 31st
3.  **HW 3:** Friday, November 14th
4.  **HW 4:** Friday, November 28th
5.  **HW 5:** Friday, December 12th