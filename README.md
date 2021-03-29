# Riemann-Stieltjes Integreated Grad-CAM (RSI-Grad-CAM)

This is a implementation of a variation of Grad-CAM in which gradients are replaced with integrated gradients at the layer level. Like Grad-CAM, it can be applied at the layer level, and like Integrated Gradients it is not affected by the problem of vanishing gradients. For efficiency, gradient integration is performed numerically at the layer level using a Riemann-Stieltjes sum approximation.
