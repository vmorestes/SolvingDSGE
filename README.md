# Replication Code for A Framework for Solving Non-Linear DSGE Models

This code replicates the results of the paper [A Framework for Solving Non-Linear DSGE Models](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3414589)

### Authors
* [Ricardo Masini](https://sites.google.com/site/ricardomasini/) (Center for Statistics and Machine Learning, Princeton University)
* Victor Orestes (Economics Department, MIT)


### Example

We employ our solution method to solve the model presented by [Fernández-Villaverde, J., Gordon, G., Guerrón-Quintana, P., & Rubio-Ramírez, J. F. (2015)](https://www.sciencedirect.com/science/article/abs/pii/S0165188915000949) . It consists of a baseline New Keynesian model with a Zero Lower Bound on the nominal interest rate. In the original paper the [Smolyak](https://www.sciencedirect.com/science/article/abs/pii/S0165188914000621?via%3Dihub) method is used  to solve the model. Particularly, our solution indicates that the ZLB binds less often and has lesser impact on the variables2. Moreover, our solution achieves smaller Euler Equation Errors, indicating that it has more precision than the Smolyak’s solution, which may suffer from a poor performance of Polynomial based approximations to capture the sharp changes around the ZLB. 

### Code

We implement the algorithm in matlab.  The man execution file is "DSGEZLB.m", which can find the optimal policy functions and compute the graphs and tables presented in the paper. We already stored the final solution, to find it, as in [Fernández-Villaverde, J., Gordon, G., Guerrón-Quintana, P., & Rubio-Ramírez, J. F. (2015)](https://www.sciencedirect.com/science/article/abs/pii/S0165188915000949), it is necessary an appropriate initial guess. We start in an economy where the zero lower bound never binds (by setting the persistence of the discount rate shock to 0) and gradually increase the persistence to the desired value, using the previous solution as an initial guess

