# ACTIVE

## Recognizing Actions from Robotic View for Natural Human-Robot Interaction

[ [Project Page](https://active2750.github.io/) ]

Official code for "Recognizing Actions from Robotic View for Natural Human-Robot Interaction", ICCV, 2025.

![image](assets/image.png)

## Introduction

Natural Human-Robot Interaction (N-HRI) requires robots to recognize human actions at various distances and states, while the robot itself may be in motion or stationary. This setup is more flexible and practical than traditional human action recognition tasks. However, existing benchmarks are designed for conventional human action recognition and fail to address the complexities of understanding human action in N-HRI, given the limited data, data modalities, task categories, and diversity in subjects and environments. To understand human behavior in N-HRI, we introduce ACTIVE (Action from Robotic View), a large-scale human action dataset for N-HRI. ACTIVE includes 30 composite action categories with labels, 80 participants, and 46,868 video instances, covering both point cloud and RGB modalities. During data capture, participants perform various human actions in diverse environments at different distances (from 3m to 50m), with the camera platform also in motion to simulate varying robot states. This comprehensive and challenging benchmark aims to advance research on human action understanding in N-HRI, such as action recognition and attribute recognition. For recognizing actions from robotic view, we propose ACTIVE-PC, which achieves accurate perception of human actions at long distances through Multilevel Neighborhood Sampling, Layered Recognizers and Elastic Ellipse Query, along with precise decoupling of kinematic interference and human actions. Experiments demonstrate the effectiveness of this method on the ACTIVE dataset.

## Requirements

To set up the environment for this repository, ensure you have the following dependencies:

You can install all the necessary Python packages by running:

```bash
pip install -r requirements.txt
```

### Additional Dependencies

1. **CUDA Layers for PointNet++**  

   ```bash
   cd modules
   python setup.py install
   ```

2. **kNN**  

   ```bash
   pip install --upgrade https://github.com/unlimblue/KNN_CUDA/releases/download/0.2/KNN_CUDA-0.2-py3-none-any.whl
   ```

For more detailed settings, you can refer to the `requirements.yml` file.（Tested on: PyTorch 1.12.0 Python3.8 CUDA11.3）

## Acknowledgement
This work is built upon the [PSTNet](https://github.com/hehefan/Point-Spatio-Temporal-Convolution)
