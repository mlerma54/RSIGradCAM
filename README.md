# Riemann-Stieltjes Integrated Grad-CAM (RSI-Grad-CAM)

This is an implementation of a variation of Grad-CAM in which gradients are replaced with integrated gradients at the layer level. Like Grad-CAM, it can be applied at the layer level, and like Integrated Gradients it is not affected by the problem of vanishing gradients when the (post-softmax) outputs get saturated. For efficiency, gradient integration is performed numerically at the layer level using a Riemann-Stieltjes sum approximation. Additional information can be found [here](https://arxiv.org/abs/2205.10900) and [here](https://link.springer.com/chapter/10.1007/978-3-031-20713-6_20). Note that this method uses post-softmax outputs of the network rather than the pre-softmax scores recommended for Grad-CAM - more on advantages and disadvantages of the use of pre and post-softmax scores can be found [here](https://arxiv.org/abs/2306.13197) and [here](https://arxiv.org/abs/2307.03305).

Files included:

- RSI_Grad_CAM.ipynb - implementation of RSI-Grad-CAM (on Keras over TensorFlow).

- RSI_Grad_CAM_w_autobaseline.ipynb - RSI-Grad-CAM with automatic computation of baseline.

- RSI_Grad_CAM_PyTorch_w_VGG19.ipynb - implementation of RSI-Grad-CAM in PyTorch for use on a VGG19 classifier network.

- RSI_Grad_CAM_PyTorch_w_ResNet50.ipynb - implementation of RSI-Grad-CAM in PyTorch for use on a ResNet50 classifier network.

- RSI_Grad_CAM_w_path_selection_PyTorch_w_ResNet50.ipynb - implementation of RSI-Grad-CAM with integration path selection in PyTorch for use on a ResNet50 classifier network. Integration path selection allows e.g. to integrate in the latent space of a VAE rather than using a plain linear interpolation of images from a baseline.

- imagenet_classes.txt - list of ImageNet classes.

Related papers: 

- Mirtha Lucas, Miguel Lerma, Jacob Furst and Daniela Raicu (2022): Visual Explanations from Deep Networks via Riemann-Stieltjes Integrated Gradient-based Localization - https://arxiv.org/abs/2205.10900

- Lucas, M., Lerma, M., Furst, J., Raicu, D. (2022). RSI-Grad-CAM: Visual Explanations from Deep Networks via Riemann-Stieltjes Integrated Gradient-Based Localization. In: Bebis, G., et al. Advances in Visual Computing. ISVC 2022. Lecture Notes in Computer Science, vol 13598. Springer, Cham. https://doi.org/10.1007/978-3-031-20713-6_20

