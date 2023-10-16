
<img src="https://github.com/havahol/io-pages-test/assets/5363644/673ca82e-dc40-456b-8d49-4d29084f685a" width=500>

 
A GPU-accelerated simulation framework for running large ensembles of simplified ocean models for real-world domains.

GPU Ocean is a GPU-accelerated framework for running large ensembles of simplified ocean models for probabilistic drift trajectory forecasting. The ocean model is based on the shallow-water equations in a rotating frame of reference, and hence describes the barotropic dynamics of the ocean. This mathematical model is very well-suited for implementation on GPU, which enables efficient simulations and a well-suited model for investigating in ensemble-based probabilistic forecasting. It supports nesting within the results of operational 3D ocean models. This means that it uses the operational model for initial and boundary conditions, terrain data (bathymetry and coast line), and wind forcing, and online simulation of drift trajectories. Furthermore, the framework contains implementations of several ensemble-based data assimilation methods for efficient assimilation of point-based observations of ocean currents. 

The 

* GPU-accelerated implementations of state-of-the-art high-resolution finite-volume methods
* Initialisation, forcing and boundary conditions from NetCDF containing operational 3D ocean forecasts
* Running large ensembles with optional use of MPI for distributed memory parallelization
* Online drift trajectory of (ensembles of) drifting objects
* Tailored data-assimilation methods for sparse in-situ observations


## Academic publications using GPU Ocean
* H. Holm, F. Beiser, *Reducing Numerical Artifacts by Sacrificing Well-Balance for Rotational Shallow-Water Flow*. Accepted for publication in the proceedings of the conference Finite Volumes for Complex Applications 10, 2023
*	A. Brodtkorb, H. Holm, *Coastal Ocean Forecasting on the GPU using a Two-Dimensional Finite Volume Scheme*. Tellus A: Dynamic Meteorology and Oceanography, 73:1, 1-22, DOI: [10.1080/16000870.2021.1876341](https://doi.org/10.1080/16000870.2021.1876341) [Preprint: [arXiv:1912.02457](https://arxiv.org/abs/1912.02457)]
*	H. Holm, A. Brodtkorb, M. Sætra, *Data Assimilation for Ocean Drift Trajectories Using Massive Ensembles and GPUs*. In: Klöfkorn, R., Keilegavlen, E., Radu, F.A., Fuhrmann, J. (eds) Finite Volumes for Complex Applications IX - Methods, Theoretical Aspects, Examples. FVCA 2020. Springer Proceedings in Mathematics & Statistics, vol 323. Springer, Cham. DOI: [10.1007/978-3-030-43651-3_68](https://doi.org/10.1007/978-3-030-43651-3_68)
*	H. Holm, M. Sætra, P. van Leeuwen, *Massively parallel implicit-equal weights particle filter for ocean drift trajectory forecasting*. Journal of Computational Physics: X, volume 6, 100053, 2020. DOI: [10.1016/j.jcpx.2020.100053](https://doi.org/10.1016/j.jcpx.2020.100053) [Preprint: [arXiv:1910.01031](https://arxiv.org/abs/1910.01031)]
* 	H. Holm, A. Brodtkorb, K. Christensen, G. Broström, M. Sætra, *Evaluation of selected finite-difference and finite-volume approaches to rotational shallow-water flow*. Communications in Computational Physics, volume 27, pp. 1234-1274, 2020. DOI: [10.4208/cicp.OA-2019-0033](https://doi.org/10.4208/cicp.OA-2019-0033)
* H. Holm, A. Brodtkorb, M. Sætra, *GPU Computing with Python: Performance, Energy Efficiency and Usability*. Computation, volume 8, number 1:4, 2020 (Special issue on Energy-Efficient Computing on Parallel Architectures) DOI: [10.3390/computation8010004](https://doi.org/10.3390/computation8010004). [Preprint: [arXiv:1912.02607](https://arxiv.org/abs/1912.02607)]
*	H. Holm, A. Brodtkorb, M. Sætra, *Performance and energy efficiency of CUDA and OpenCL for GPU computing using Python*. Advances in Parallel Computing, volume 36, pp. 593-604, 2020. DOI: [10.3233/APC200089](https://doi.org/10.3233/APC200089)


**Preprints**
* F. Beiser, H. Holm, J. Eidsvik, *Comparison of Ensemble-Based Data Assimilation Methods for Sparse Oceanographic Data*, 2023, [arXiv:2302.07197](https://arxiv.org/abs/2302.07197)



## Development and funding
GPU Ocean is developed through a collaboration between the Norwegian Meteorological Institute and the Applied Computational Science research group at SINTEF Digital. We are greatful for the support from the Norwegian Research Council under grant numbers 250935 (GPU Ocean) and 310515 (Havvarsel).
