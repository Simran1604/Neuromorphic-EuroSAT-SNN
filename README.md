# Neuromorphic-EuroSAT: Low-Power Satellite Image Classification

An exploration into Hardware-Aware Artificial Intelligence, replacing standard energy-heavy CNNs with a Convolutional Spiking Neural Network (CSNN) to classify EuroSAT land cover data. 

## Overview
Traditional Deep Learning models rely on dense, energy-intensive Multiply-Accumulate (MAC) operations. This project bridges standard software machine learning with neuromorphic engineering principles. By utilizing Leaky Integrate-and-Fire (LIF) neurons and rate-coding, the network processes discrete temporal spikes, relying entirely on sparse Synaptic Operations (SynOps) to drastically reduce computational overhead.

* **Frameworks:** PyTorch, snnTorch, Torchvision
* **Dataset:** EuroSAT (RGB Satellite Imagery)
* **Architecture:** Convolutional Spiking Neural Network (CSNN) with Surrogate Gradient Descent

## Hardware Efficiency Results
The primary objective of this project is proving computational sparsity. When evaluated on standard 45nm CMOS hardware benchmarks (4.6 pJ/MAC vs. 0.9 pJ/SynOp), the SNN demonstrates massive energy savings due to its low firing rate.

| Metric | Standard Dense ANN | Sparse CSNN (This Project) |
| :--- | :--- | :--- |
| **Compute Operations** | MACs | SynOps |
| **Estimated Energy** | 100% (Baseline) | ~15% - 30% (Estimated) |
| **Total Energy Saved** | **0%** | **~70% - 85%** |

## Quick Start (Run on Google Colab)
This project is designed to be lightweight and train efficiently on free-tier cloud GPUs.
1. Clone this repository.
2. Upload the `Neuromorphic_EuroSAT.ipynb` notebook to Google Colab.
3. Set the runtime to **T4 GPU** and run all cells.
