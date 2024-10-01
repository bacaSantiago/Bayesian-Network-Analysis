# Bayesian Network Analysis of Cardiopulmonary Diseases and Symptoms Caused by Smoking and COVID-19

---

## Overview

This project presents a comprehensive analysis of cardiopulmonary diseases, their symptoms, and the influence of smoking and COVID-19 using a **Bayesian Network**. The system models probabilistic relationships between risk factors such as smoking and diseases like **heart disease**, **lung cancer**, and **COVID-19**. It utilizes **Bayesian Inference** to assess the likelihood of developing these conditions based on observed symptoms, offering a powerful tool for medical diagnostics. The model allows for the integration of uncertainties through **Conditional Probability Distributions (CPDs)** and is designed to assist in real-time decision-making processes.

The project leverages **mathematical** and **computational concepts**, including Bayesian Networks,Probabilistic Inference, Directed Acyclic Graphs (DAGs), Conditional Probability Tables (CPTs), and, Variable Elimination. Additionally, the project incorporates **case studies** focused on diagnosing **COVID-19** based on patient symptoms, providing a real-world application of the Bayesian network model.

---

## Introduction

Cardiopulmonary diseases, such as **heart disease** and **lung cancer**, are leading causes of death worldwide, and the emergence of **COVID-19** has added complexity to the diagnostic landscape. Smoking is a known risk factor for these diseases, making it imperative to understand the interplay between smoking, cardiopulmonary conditions, and viral infections like COVID-19.

**Bayesian Networks** provide a framework to model these relationships probabilistically, allowing healthcare providers to account for uncertainties in patient data and symptoms. By integrating observed evidence—such as whether a patient has a cough or fatigue—into the Bayesian network, clinicians can calculate the likelihood of different diagnoses, including flu, pneumonia, and COVID-19.

This project constructs a **Bayesian Network** that models the relationships between:

- **Smoking** and its influence on **lung cancer** and **heart disease**.
- Symptoms such as **cough**, **fatigue**, **tachycardia**, and **COVID-19 symptoms**.
The system is designed to dynamically update its predictions based on incoming patient data, making it a valuable diagnostic tool.

---

## Theoretical Framework

### 1. **Bayesian Networks:**

A **Bayesian Network** is a type of probabilistic model that represents variables and their conditional dependencies using a **Directed Acyclic Graph (DAG)**. Each node represents a variable, while the directed edges between nodes represent conditional dependencies. These models allow for the incorporation of uncertainty and provide a powerful mechanism for reasoning under uncertainty, particularly in medical diagnosis.

At the core of Bayesian networks is **Bayes’ Theorem**, which computes the posterior probability of a hypothesis given observed evidence. In this project, the network updates the probability of diseases (such as **lung cancer**, **heart disease**, or **COVID-19**) given symptoms such as **cough** or **fatigue**.

- **Bayes’ Theorem**:
  $$ P(H | E) = \frac{P(E | H) \cdot P(H)}{P(E)} $$
  
  Where:
  - $P(H|E)$ is the posterior probability of the hypothesis (e.g., the disease) given the evidence (e.g., symptoms).
  - $P(E|H)$ is the likelihood of the evidence given the hypothesis.
  - $P(H)$ is the prior probability of the hypothesis.
  - $P(E)$ is the marginal probability of the evidence.

### 2. **Conditional Probability Distributions (CPDs);**

In Bayesian networks, each node is associated with a **Conditional Probability Distribution (CPD)** that quantifies the effect of its parents. For instance, the CPD for **heart disease** will depend on whether the patient is a smoker. These tables allow the network to model the likelihood of a disease given observed risk factors and symptoms.

### 3. **Variable Elimination:**

**Variable Elimination** is an exact inference algorithm used in Bayesian networks to compute marginal probabilities. It systematically eliminates irrelevant variables, simplifying the computation of posterior probabilities based on observed symptoms.

---

## Methodology

### 1. **Bayesian Network Construction:**

The Bayesian network includes variables representing **smoking**, **heart disease**, **lung cancer**, and symptoms associated with **COVID-19**. The structure of the network was designed using clinical knowledge, and **Conditional Probability Tables (CPTs)** were constructed to model the relationships between the variables.

The key variables in the network are:

- **Smoking**: A risk factor for both heart disease and lung cancer.
- **Heart Disease**: Condition linked to symptoms like **fatigue** and **tachycardia**.
- **Lung Cancer**: Condition that increases the likelihood of symptoms like **cough**.
- **COVID-19 Symptoms**: These include **fever**, **dry cough**, **fatigue**, and **loss of taste or smell**.

### 2. **Probabilistic Inference:**

Once the network is constructed, **inference** is performed using the **Variable Elimination** algorithm. By inputting observed symptoms, the network computes the **posterior probabilities** of diseases like heart disease, lung cancer, or COVID-19. The model dynamically updates its predictions based on the evidence provided.

### 3. **Case Study on COVID-19 Symptoms:**

The model was applied to real-world case studies involving patients with COVID-19 symptoms. By analyzing symptoms such as **cough**, **fever**, and **fatigue**, the Bayesian network was used to diagnose the likelihood of **COVID-19** versus other respiratory conditions like **pneumonia** or **flu**.

---

## Dependencies

This project uses the following libraries and tools:

- **Python**: Version 3.x
- **pgmpy**: A Python library used for **probabilistic graphical models** and **Bayesian networks**. It provides tools for defining the structure of Bayesian networks, specifying CPDs, and performing inference using algorithms like **Variable Elimination**.
- **NumPy**: Essential for numerical computations.
- **Matplotlib**: Used for visualizing **graphs** and **probability distributions**.
- **Pandas**: For managing and processing patient data and symptoms.
- **Scikit-learn**: For auxiliary machine learning tasks that may be used in preprocessing medical data.

---

## Resources

- **pgmpy Documentation**: [pgmpy Documentation](https://pgmpy.org/)
- **COVID-19 Symptom Dataset**: Simulated patient data containing symptoms and risk factors.
- **Matplotlib Documentation**: [Matplotlib](https://matplotlib.org/)

---

## Summary

This project presents an application of **Bayesian networks** to model the probabilistic relationships between **smoking**, **cardiopulmonary diseases**, and **COVID-19** symptoms. The network incorporates multiple risk factors and symptoms, allowing for real-time **medical diagnosis** based on observed data. Through case studies, the model demonstrates its ability to provide meaningful predictions, enabling healthcare providers to make more informed decisions.

By leveraging **Bayes' Theorem** and **Variable Elimination**, the model efficiently computes **posterior probabilities** and offers a dynamic framework for diagnosing complex medical conditions. The project serves as a foundational tool for integrating probabilistic reasoning into medical decision-making systems, with potential applications in diagnosing emerging health threats like COVID-19.
