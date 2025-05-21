
# Improving Transferability of Network Intrusion Detection in a Federated Learning Setup

## Project Overview
This project focuses on improving the **transferability** of **Intrusion Detection Systems (IDS)** using **Federated Learning**. The goal is to detect **unseen attack types** by training models across **distributed nodes** without sharing raw data. Techniques like **Bootstrapping** (for class balancing) and **Temporal Averaging** (for smoothing data) are used to enhance the model’s generalization ability.

## Preprocessing Techniques
- **Bootstrapping**: Applied to balance the dataset by oversampling attack samples, addressing **class imbalance**.
- **Temporal Averaging**: Smooths the data by averaging consecutive samples, capturing **time-dependent attack patterns**.

## Federated Learning
- **FedAvg** is used to aggregate model updates across nodes and update the global model. The project supports:
  - **5-Node IID Mode**: A balanced mode with similar data distribution across nodes.
  - **11-Node Non-IID Mode**: Nodes specialize in one attack type, making it a more **realistic** transferability setup.

## Run the Project
To run the model in **Federated Learning** mode, use:
```bash
python main.py --n_classes 2 --n_rounds 20 --epochs 1
```

For **Bootstrapping** and **Temporal Averaging**:
```bash
python main_bootstrap.py --n_classes 2 --n_rounds 20 --epochs 1 --tmp True
```
