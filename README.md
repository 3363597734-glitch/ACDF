# Modeling an Artificial Dorsal Stream for Event-Based Vision
Modeling an Artificial Dorsal Stream for Event-Based Vision

![fk](https://github.com/user-attachments/assets/fd8fca1d-96bb-4e37-933b-cef65bd0c37d)

We are pleased to share that this work has been published at ICML.


##  Highlights
• We propose an event stream processing framework inspired by the brain’s dorsal visual pathway. We introduce the spatial-temporal information encoding mechanism of the brain’s dorsal pathway, also known as the ”where” pathway, into the event stream data processing framework, effectively establishing a high-order mapping fromevent streams to event frames.

• This framework utilize CCNN to encode constant polarity eventsequences as periodic signals and varying-polarity event sequences as chaotic signals, effectively achieving robust event representation. Combined with traditional deep neural network, the frame work successfully performs in object classification for event cameras.

• The proposed framework is evaluated on multiple datasets, achieving the state-of-the-art accuracy on specific benchmarks. It also demonstrates competi tive performance across a variety of datasets. The results demonstrate the framework’s strong generaliza tion across different data structures.

## Abstract
Event cameras are bio-inspired vision sensors that encode visual information with high dynamic range, high temporal resolution, and low latency. Current state-of-the-art event stream processing methods rely on end-to-end deep learning techniques. However, these models are heavily dependent on data structures, limiting their stability and generalization capabilities across tasks, thereby hindering their deployment in real-world scenarios. To address this issue, we propose a chaotic dynamics event signal processing framework inspired by the dorsal visual pathway of the brain. Specifically, we utilize Continuouscoupled Neural Network (CCNN) to encode the event stream. CCNN encodes polarity-invariant event sequences as periodic signals and polaritychanging event sequences as chaotic signals. We then use continuous wavelet transforms to analyze the dynamical states of CCNN neurons and establish the high-order mappings of the event stream.
The effectiveness of our method is validated through integration with conventional classification networks, achieving state-of-the-art classification accuracy on the N-Caltech101 and N-CARS datasets, with results of 84.3 % and 99.9 %, respectively. Our method improves the accuracy of event camera-based object classification while significantly enhancing the generalization and stability of event representation.

## Overall Architecture
<img width="1501" height="923" alt="微信图片_2026-10-14_094352_810" src="https://github.com/user-attachments/assets/e2b5ebcc-cd1a-491e-b8e2-44c85f4e256d" />
The human brain’s visual cortex recognizes moving objects through the dorsal and ventral pathways. Event cameras mimic the three-layer
structure of the peripheral retina in humans, encoding moving objects into event stream data. We utilize a chaotic dynamics framework, based on CCNN, to
map the event stream data into event representations inspired by the dorsal stream. Subsequently, the event representations are sent from the MT area to the IT
area, where recognition of moving objects is achieved through multiple layers of neural networks.



## Visualization
![vis](https://github.com/user-attachments/assets/2c4fa26f-03fa-4c64-94f7-eea2eab3b512)

## Installation
• Python 3.9+ and CUDA 12.0

• PyTorch 2.4.1+ and corresponding torchvision

## Quick Start
with data:
```python
python datasets/N-CAR.py
```

with train:
```python
 python demo/train.py
```

with test:
```python
 python demo/test.py
```
