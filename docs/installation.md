---
sidebar_position: 2
---

# Installation

OpenVIMO has two depedencies:

- The [Covfee framework](https://josedvq.github.io/covfee/docs) which takes care of experiment management. Covfee is a Python package and server that will read a study specification coded in Python and generate web pages and URLs that can be sent to the study participants.
- The [OpenVIDU framework](https://docs.openvidu.io/en/stable/getting-started/) which takes care of video communication and recording. For our purposes OpenVIDU is a video communication server that will run alongside the Covfee server and will take care of WebRTC communication specifically. Covfee will communicate with the OpenVIDU server under the hood.

The set them up in your local PC follow these steps:

1. Create a virtual environment for covfee. We recommend a conda environment:

   ```
   conda create --name covfee python=3.10
   conda activate covfee
   ```

2. Install covfee:

   ```
   git clone https://github.com/josedvq/covfee.git
   cd covfee
   python -m pip install -e .
   ```

3. Make sure it works. Covfee includes [sample projects](https://github.com/josedvq/covfee/tree/master/samples). Try running one:

   ```
   cd samples/basic
   covfee make basic.py
   ```

4. Run OpenVIDU
