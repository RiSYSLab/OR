This dataset contains the city color matrices of the instances used for the experiments in the papers:  
[1] Lin, Z., Li, J.* & Li, Y., "A cloud computing approach to superscale colored traveling salesman problems," Journal of Supercomputing, 2024, 80 (19), pp.27340-27369.  
[2] X Xu, J Li*, and MC Zhou, “Delaunay-triangulation-based variable neighborhood search to solve large-scale general colored traveling salesman problems,” IEEE Transactions on Intelligent Transportation Systems, 2020, 22 (3): 1583-1593.  
[3] Zhicheng Lin and Jun Li*, “A hybrid genetic algorithm with cycle reassembly for solving colored traveling salesman problems,” Journal of King Saud University Computer and Information Sciences, 2025, 37(7): 1-23.  
Each city color file storing a city color matrix in .txt format is named “number of cities_number of colors (number of salesmen).” Such a file corresponds to a TSPLIB case with the same number of cities.  
Each element of the initial row in the city color file indicates whether a city has multiple colors or a single color. If the value of an element is greater than 1, the corresponding city is multicolored; otherwise, it is single-colored. 
In our case, each salesman considers an arbitrary city that carries only his color as his depot.
