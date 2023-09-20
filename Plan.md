
### Using deep-learning to propagate measurement uncertainty in coordinate transforms for radio astronomy

*Astronomical measurements require observers to transform between Earth/ground-based coordinate systems and astronomical coordinate systems as standard. 
The transforms between these systems are governed by a set of rotations on the sphere and can be calculated analytically; however, the propagation of 
measurement uncertainties from one frame to another is rarely (if ever) taken into account. In this project the students will train neural network 
(deep-learning) models to learn the transformations between common astronomical coordinate systems. They will then investigate the different types of 
uncertainty inherent in these models, as well as methods for propagating uncertainties in the input  positions into uncertainties on the output transformed 
coordinates. They will compare these uncertainties to those obtained through more conventional methods, as well as the computational complexity involved.*

https://www.degruyter.com/document/doi/10.1515/jisys-2022-0033/html?lang=en

---

### Work Plan

* Set up simple neural network to learn a coordinate transform as a regression problem. Our target transform will be transforming from ground-based antenna locations in an ENU frame to Fourier coordinates in a UVW frame.
* Introduce a Bayesian approximation to understand the degree of *epistemic uncertainty* in the model itself. The simplest approximation would be MCDropout.
* Develop a method to incorporate measurement uncertainties on the ENU input data and propagate it through to the UVW outputs. This could be done (for example) as:
    - using both the measurement and the uncertainty as inputs to learn a transform and its analytic uncertainty directly;
    - setting up a sampling approach using VI or MCMC to train a Bayesian model;
    - something else
* Compare the model uncertainties (separating the epistemic uncertainty from the overall uncertainty) to the uncertainties expected from an analytic/numerical estimate of propagated uncertainty.
  
