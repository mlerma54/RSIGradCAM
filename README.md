# Riemann-Stieltjes Integrated Grad-CAM (RSI-Grad-CAM)

This is a implementation of a variation of Grad-CAM in which gradients are replaced with integrated gradients at the layer level. Like Grad-CAM, it can be applied at the layer level, and like Integrated Gradients it is not affected by the problem of vanishing gradients. For efficiency, gradient integration is performed numerically at the layer level using a Riemann-Stieltjes sum approximation. Additional information can be found [here](https://arxiv.org/abs/2205.10900). 

Files included:

- RSI_Grad_CAM.ipynb - implementation of RSI-Grad-CAM (on Keras over TensorFlow)

- RSI_Grad_CAM_w_autobaseline.ipynb - RSI-Grad-CAM with automatic computation of baseline

- RSI_Grad_CAM_pytorch.ipynb - implementation of RSI-Grad-CAM in PyTorch

- imagenet_classes.txt - list of Imagenet classes
