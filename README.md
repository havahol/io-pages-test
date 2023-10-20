
<img src="https://github.com/havahol/io-pages-test/assets/5363644/673ca82e-dc40-456b-8d49-4d29084f685a" width=500>

 
**A GPU-accelerated simulation framework for running large ensembles of simplified ocean models for real-world domains.**

Operational ocean forecasting models are computationally expensive and are therefore often run as a single deterministic simulation at given intervals. This means that often lack information about forecast uncertainties, which are significant given that there are relative few observations of the ocean compared to its sheer size. Information on uncertainty is, however, vital for various applications, including search-and-rescue operations at sea.

### What is GPU Ocean?
GPU Ocean is a simulation framework designed to explore the short-term uncertainty in forecasted ocean currents. It achieves this by running ensembles of simplified ocean models nested within operational ocean forecasts. These simplified models efficiently solve barotropic dynamics described by the shallow-water equations using GPUs.

### Key Features:

* **Efficient simulation:** GPU Ocean utilizes GPU acceleration and state-of-the-art finite-volume methods to solve shallow-water equations efficiently.
* **Model nesting:**  Easily import initialization data, terrain information, forcing, and boundary conditions from NetCDF files containing operational 3D ocean forecasts.
* **Drift trajectory prediction:** Conduct online drift trajectory simulations for drifting objects within the ocean models, directly assessing uncertainty in drift trajectories concerning ocean current uncertainties.
* **Data Assimilation**: GPU Ocean includes tailored data-assimilation methods for sparse in-situ observations.
* **Python with CUDA Performance**: Rapid prototyping and easy orchestration, pre-, and post-processing using Python while getting the computational performance of CUDA.
* **Parallel Processing:** MPI support for running even larger ensembles on multiple GPUs. 


GPU Ocean aims to be a powerful tool to complement ocean current forecasts through estimating and accounting for forecast uncertainties. By combining local observations and advanced data assimilation methods, users can make more informed decisions based on the latest oceanic data.

# First draft below:

<img src="https://github.com/havahol/io-pages-test/assets/5363644/673ca82e-dc40-456b-8d49-4d29084f685a" width=500>


Operational ocean forecasting models are computationally expensive and are therefore often run as a single deterministic simulation at given intervals. This means that there are no information about the uncertainties associated to the forecast. Such uncertainties are of critical importance, for instance when the currents in the forecast is used to predict drift trajectories for search-and-rescue operations at sea.

The idea behind GPU Ocean is to explore the short-term uncertainty in the forecasted ocean currents through running ensembles of simplified ocean models nested into the operational ocean forecast.
The simplified ocean models contain barotropic dynamics as described by the rotating shallow-water equations, which can be solved very efficiently using GPUs. 
This means that the ensemble prediction can be made very fast, and makes it possible to take advantage of available local observations of the real currents and adjusting the ensemble accordingly through appropriate data assimilation methods.
Furthermore, drift trajectories can be computed directly within the ocean models themselves, meaning that we explore the uncertainty in the drift trajectories with respect to the uncertainty in the ocean currents directly. 

Highlights:
* GPU-accelerated implementations of state-of-the-art high-resolution finite-volume methods for solving the shallow-water equations
* Initialisation, terrain data, forcing and boundary conditions can be read directly from NetCDF files containing operational 3D ocean forecasts
* Running large ensembles with optional use of MPI for distributed memory parallelization
* Online drift trajectory of (ensembles of) drifting objects
* Tailored data-assimilation methods for sparse in-situ observations
* Python code base with CUDA performance

## Installation
See here.

## Academic publications using GPU Ocean
* H. Holm, F. Beiser, *Reducing Numerical Artifacts by Sacrificing Well-Balance for Rotating Shallow-Water Flow*. In: Franck, E., Fuhrmann, J., Michel-Dansac, V., Navoret, L. (eds) Finite Volumes for Complex Applications X — Volume 2, Hyperbolic and Related Problems. FVCA 2023. Springer Proceedings in Mathematics & Statistics, vol 433. Springer, Cham. DOI: [10.1007/978-3-031-40860-1_19](https://doi.org/10.1007/978-3-031-40860-1_19)
*	A. Brodtkorb, H. Holm, *Coastal Ocean Forecasting on the GPU using a Two-Dimensional Finite Volume Scheme*. Tellus A: Dynamic Meteorology and Oceanography, 73:1, 1-22, DOI: [10.1080/16000870.2021.1876341](https://doi.org/10.1080/16000870.2021.1876341) [Preprint: [arXiv:1912.02457](https://arxiv.org/abs/1912.02457)]
*	H. Holm, A. Brodtkorb, M. Sætra, *Data Assimilation for Ocean Drift Trajectories Using Massive Ensembles and GPUs*. In: Klöfkorn, R., Keilegavlen, E., Radu, F.A., Fuhrmann, J. (eds) Finite Volumes for Complex Applications IX - Methods, Theoretical Aspects, Examples. FVCA 2020. Springer Proceedings in Mathematics & Statistics, vol 323. Springer, Cham. DOI: [10.1007/978-3-030-43651-3_68](https://doi.org/10.1007/978-3-030-43651-3_68)
*	H. Holm, M. Sætra, P. van Leeuwen, *Massively parallel implicit-equal weights particle filter for ocean drift trajectory forecasting*. Journal of Computational Physics: X, volume 6, 100053, 2020. DOI: [10.1016/j.jcpx.2020.100053](https://doi.org/10.1016/j.jcpx.2020.100053) [Preprint: [arXiv:1910.01031](https://arxiv.org/abs/1910.01031)]
* H. Holm, A. Brodtkorb, K. Christensen, G. Broström, M. Sætra, *Evaluation of selected finite-difference and finite-volume approaches to rotational shallow-water flow*. Communications in Computational Physics, volume 27, pp. 1234-1274, 2020. DOI: [10.4208/cicp.OA-2019-0033](https://doi.org/10.4208/cicp.OA-2019-0033)
* H. Holm, A. Brodtkorb, M. Sætra, *GPU Computing with Python: Performance, Energy Efficiency and Usability*. Computation, volume 8, number 1:4, 2020 (Special issue on Energy-Efficient Computing on Parallel Architectures) DOI: [10.3390/computation8010004](https://doi.org/10.3390/computation8010004). [Preprint: [arXiv:1912.02607](https://arxiv.org/abs/1912.02607)]
*	H. Holm, A. Brodtkorb, M. Sætra, *Performance and energy efficiency of CUDA and OpenCL for GPU computing using Python*. Advances in Parallel Computing, volume 36, pp. 593-604, 2020. DOI: [10.3233/APC200089](https://doi.org/10.3233/APC200089)


**Preprints**
* F. Beiser, H. Holm, J. Eidsvik, *Comparison of Ensemble-Based Data Assimilation Methods for Sparse Oceanographic Data*, 2023, [arXiv:2302.07197](https://arxiv.org/abs/2302.07197)



## Development and funding
GPU Ocean is developed through a collaboration between the Norwegian Meteorological Institute and the Applied Computational Science research group at SINTEF Digital. We are greatful for the support from the Norwegian Research Council under grant numbers 250935 (GPU Ocean) and 310515 (Havvarsel).
