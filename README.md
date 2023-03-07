# BNN Traffic Signal Detection System using PYNQ Board

This project implements a binary neural network (BNN) based traffic signal detection system using the PYNQ-Z1 board. The system uses a low-power BNN model to detect traffic signals in real-time, and it can be deployed on edge devices with limited computational resources.

## Table of Contents
1. [Introduction](#Introduction)
2. [Requirements](#Requirements)
3. [Quick Start](#Quick-Start)
4. [Installation](#Installation)
5. [Usage](#Usage)
6. [Dataset Information](#Dataset-Information)
    
## Introduction

Traffic signal detection is a crucial task for autonomous driving and traffic management systems. Traditional approaches for traffic signal detection rely on complex computer vision algorithms, which are computationally expensive and require high-end hardware. In contrast, BNNs are lightweight neural networks that can be deployed on edge devices with limited computational resources.

This project implements a BNN-based traffic signal detection system using the PYNQ-Z1 board. The system uses a pre-trained BNN model to detect traffic signals in real-time. The BNN model has been trained on a dataset of traffic signal images using the Brevitas framework. The PYNQ board is used to perform inference on the BNN model, which allows for low-latency and real-time detection of traffic signals.

## Requirements

* PYNQ-Z1 board
* SD card (minimum 8GB)
* Ethernet cable
* USB-to-UART cable
* Vivado Design Suite (version 2019.1 or later)
* Python (version 3.6 or later)
* PYNQ package (version 2.6.1 or later)

## Quick Start

Download the pre-trained BNN model using this repository [here](https://github.com/Xilinx/BNN-PYNQ) and save it.

In order to install it to your PYNQ, connect to the board, open a terminal and type:

```
sudo pip3 install git+https://github.com/Xilinx/BNN-PYNQ.git (on PYNQ v2.3)
sudo pip3.6 install git+https://github.com/Xilinx/BNN-PYNQ.git (on PYNQ v2.2 and earlier)
```

This will install the BNN package to your board, and create a **bnn** directory in the Jupyter home area. You will find the Jupyter notebooks to test the networks in this directory.

## Installation

1. Clone this repository to your local machine using the following command:

```
git clone https://github.com/username/bnn-traffic-signal-detection.git
```

2. 

3. Insert the SD card into your computer and format it using the FAT32 file system.

4. Download the PYNQ-Z1 image from here and write it to the SD card using a tool like Etcher.

5. Insert the SD card into the PYNQ board and connect it to your computer using an Ethernet cable.

6. Connect the USB-to-UART cable to the JTAG port of the PYNQ board and your computer.

7. Open Vivado Design Suite and create a new project using the bnn-traffic-signal-detection/vivado/pynq-z1/pynq-z1.xpr file.

8. Generate the bitstream and export the hardware design to the bnn-traffic-signal-detection/pynq/traffic_signal_detection directory.

9. Copy the bnn-traffic-signal-detection/pynq directory to the root of the SD card.

10. Eject the SD card from your computer and insert it into the PYNQ board.

## Usage

   1. Connect to the PYNQ board using SSH:

```
ssh xilinx@<PYNQ-IP-ADDRESS>
```

   2. Navigate to the traffic_signal_detection directory:

```
cd /home/xilinx/pynq/traffic_signal_detection
```

   3. Run the traffic_signal_detection.py script:

python3 traffic_signal

## Dataset Information

The dataset used in this project is confidential and cannot be shared publicly due to legal and ethical reasons. The dataset contains traffic signal images captured from various locations in a city, and it was used to train and test our BNN Traffic Signal Detection System.

The dataset consists of 10,000 traffic signal images in the JPEG format, with a resolution of 1280x720 pixels. The dataset also includes annotations for the traffic signals, indicating their location and type.

Access to the dataset was obtained through a collaboration with a private organization that wishes to remain anonymous.

To replicate the experiment using a public dataset, we recommend using the German Traffic Sign Recognition Benchmark (GTSRB) dataset, which is similar in size and content to the confidential dataset. However, some modifications or adjustments may be necessary to adapt our model to the GTSRB dataset.

I acknowledge that using a different dataset may have limitations and may affect the performance of the model. However, due to the confidentiality of the original dataset, I believe that this is the best alternative for replicating our experiment.
