# PINNs With Adaptive Weighing

---

## Overview

Physics-Informed Neural Networks (PINNs) combine neural networks with the governing physics of a system by embedding PDE residuals into the training objective.  

A key challenge in **inverse PDE problems** is that the data-driven loss converges much faster than the physics-informed loss, leading to poor parameter recovery.  

In this project, we explore **adaptive weighing strategies** that gradually shift emphasis from data fitting to physics consistency during training. This improves PDE residual convergence and yields more accurate parameter estimation.

For more details, see the full PDF: [Optimization_PINN](Optimization_Project__PINN.pdf) 

---

## Key Features
- Jupyter notebooks implementing PINNs for:
  - **Burgers’ equation**  
  - **Allen–Cahn equation**  
- Comparison of:
  - Standard PINNs (no weighing)  
  - Uniform/adaptive weighing of loss terms  
  - Sequential training (data loss → physics loss)  
- Experiments with both clean and noisy training data.

---

## Running the code
1. Clone the repository:
   ```bash
   git clone https://github.com/abhilash-neog/PINNs-With-Adaptive-Weighing.git
   cd PINNs-With-Adaptive-Weighing
2. Open a notebook in Jupyter, Colab, or VS Code. For example:
   ```bash
   jupyter notebook Burgers_PINN.ipynb
3. Run the cells to reproduce training and evaluation results.

## Results

- Adaptive weighing significantly reduces PDE parameter estimation errors compared to unweighted training.  
- Joint training with adaptive weighing outperforms sequential training.  
- Interestingly, PINNs sometimes converge better on noisy data than on perfectly clean synthetic data.  
