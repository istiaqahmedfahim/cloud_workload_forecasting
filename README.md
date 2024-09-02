# Hybrid RNN with Attention Mechanism for Cloud VM Workload Prediction

## Overview

This repository contains the implementation of a novel hybrid Recurrent Neural Network (RNN) model designed to accurately forecast the disk usage workload of Virtual Machines (VMs) in the cloud. Our model integrates an attention-based mechanism with a combination of 1D Convolutional Neural Network (CNN), Stacked Long Short Term Memory (LSTM), Bi-directional LSTM (Bi-LSTM), and Gated Recurrent Unit (GRU). The hybrid approach leverages the strengths of these architectures, along with optimal hyperparameter settings, to effectively learn workload patterns using both past and future data.

## Key Contributions

1. **Proposed Hybrid RNN Model**: We introduce a unique hybrid RNN-based prediction model that combines CNN, LSTM, Bi-LSTM, GRU, and an attention mechanism to predict the future disk usage of cloud VMs.

2. **Comprehensive Performance Comparison**: The proposed model's performance is compared with standalone LSTM, GRU, Bi-LSTM models, and existing high-performance hybrid models for both short-term and long-term predictions, demonstrating its superior accuracy.

3. **Analysis of Model Parameters**: We explore the impact of varying historical window sizes and training-testing data sizes on the model’s performance, providing insights into optimizing these parameters.

## Model Architecture

1. **Pre-processing Layer**: Handles the input data through normalization, scaling, and feature extraction to enhance data quality for subsequent learning processes.

2. **1D Convolutional Neural Network (CNN) Layer**: Extracts spatial relationships within sequential workload data by applying convolution filters across the input sequence. The spatial features obtained from this layer significantly improve prediction accuracy.

3. **Stacked Long Short-Term Memory (LSTM) Layer**: Captures temporal dependencies and long-range patterns in the workload data. The stacked LSTM architecture effectively replicates complex temporal relationships inherent in the data.

4. **Attention Mechanism**: The attention layer dynamically assigns weights to time stamps based on their relevance, improving the model's ability to focus on salient information and thereby enhancing prediction accuracy.

5. **Bi-directional LSTM (BiLSTM) Layer**: Processes input sequences in both forward and backward directions, capturing contextual information from past and future time steps simultaneously.

6. **Gated Recurrent Unit (GRU) Layer**: Optimizes the model by improving training efficiency and reducing complexity without sacrificing performance. The GRU layer accelerates convergence and reduces memory usage, contributing to the overall effectiveness of the predictive system.

7. **Fully Connected Layer**: Acts as the final component, synthesizing information from all preceding layers to generate the final workload forecasts.
