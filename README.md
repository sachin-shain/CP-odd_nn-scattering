# Python code of Renormalization of CP-violating nuclear force
This folder contains the python file used to produce the results in work [Renormalization of CP -violating nuclear force](https://journals.aps.org/prc/abstract/10.1103/PhysRevC.103.L012501). 

- The algorithm is split into two parts: 'CP Even' and 'CP Odd'.
- The program is written using jupyter notebooks
- The required packages are declared in the first cell of *init_.ipynb*
- For each function or class, an *Example* is given below

## CP Even
The jupyter notebook files calculates the CP-even data. The files are

- *init_.ipynb*: It declares the required packages, constants, grid points, and functions for printing and testing purposes. 
- *potential_num.ipynb*:   - calculate the CP-even leading order one-pion-exchange and contact potential
  - CP-even potential with the regulator.
- *LS.ipynb*: 
  - uses Lippmann-Schwinger equation to calculate the T-matrix and S-matrix. 
  - calculate phase shifts and mixing angles for given $\\{\alpha_i\\}$.
- *c0_calc.ipynb*:
  - calculate $C_0(\Lambda)$ by fitting to given $\delta_0$ at $E_{\rm lab} = 10\ {\rm MeV}$.
- *cp_even_plots.ipynb*: generate phase shifts vs $\Lambda$ plots and save as pdf in the folder **cp_even_plots**.
- *comparision_plot.ipynb*: generate phase shifts calculated and experimental values vs $E_{\rm lab}$ and save as pdf in the folder **comparison_plots**.

The files should be run in the order listed above. The results are stored in the folders
- **c0**: $C_0(\Lambda)$.
- **cp_even_plots**: phase-shifts/mixing-angles vs $\Lambda$. 
- **comparison_plots**: phase-shifts/mixing-angles calculated and experimental vs $E_{\rm lab}$. The experimental data files are stored in the subfolder **data**.

## CP Odd
The jupyter notebook files calculates the CP-odd data. The files are

- *init_.ipynb*: It declares the required packages, constants, grid points, and functions for printing and testing purposes. 
- *potential_num.ipynb*:   - calculate the CP-even(odd) leading order one-pion-exchange and contact potential
  - CP-even(odd) potential with the regulator.
- *LS.ipynb*: 
  - uses Lippmann-Schwinger equation to calculate the T-matrix and S-matrix. 
  - calculate phase shifts and CP-odd(even) mixing angles for given $\\{\alpha_i\\}$.
- *cpv_counterterm.ipynb*:
  - implement method_1 and method_2 for calculating CP-odd observables.
  - calculate CP-odd $C_0(\Lambda)$ by fitting to given $\delta_0=\\{0.01,0.11,-0.09\\}\bar g_0$ at $E_{\rm lab} = 10\ {\rm MeV}$ using method 1.
 - store the results in the folder **c0**.
- *cpv_plots.ipynb*: 
  - generate phase shifts vs $\Lambda$ plots and save as pdf in the folder **cp_odd_plots** for $j=0$.
  - generate data file to make phase shifts vs $\Lambda$ plots for $j=1$.

The results are stored in the folder
- **c0**: CP-even and CP-odd $C_0(\Lambda)$. CP-odd data is copied from the 'CP Even' folder. 
- **cp_even_plots**: phase-shifts/mixing-angles vs $\Lambda$ for  $\delta_0=\\{0.01,0.11,-0.09,0.00\\}\bar g_0$ at $E_{\rm lab} = \\{10,20,100,190\\}\ {\rm MeV}$.
