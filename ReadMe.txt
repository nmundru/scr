===
The code implements the ideas outlined in the manuscript by Dimitris Bertsimas and 
Nishanth Mundru titled "Sparse Convex Regression".

These are instructions for using the attached code and replicating the results.

The code was written by Nishanth Mundru, in collaboration with Prof. Dimitris Bertsimas.
===

1) This project requires the Gurobi solver, Julia with JuMP, and MATLAB (for comparing with the ADMM algorithm).

2) There are two zip files. 
a. Codes.zip file contains files with Julia and MATLAB code, 
b. Test_Instances.zip file (download link on the github page) contains test instances.

3). Details of files in Codes.zip:

admm_matlab.m - Implements ADMM algorithm in MATLAB.

admm_script.m - Runs admm_matlab given input data, and stores output.

agcp.jl -  Implements the augmented cutting plane algorithm.

convex_reg.jl  - Implements Algorithm 1, i.e., cutting plane algorithm for continuous 
	         least squares convex regression problem.

solve_comparison_admm.jl - Compare cutting planes with ADMM approach.

l1_convex_reg.jl - Implements the cutting plane algorithm for continuous l1 convex regression problem.

dual_sparse.jl - Implements Algorithm 3, i.e., the cutting plane algorithm for sparse convex regression problem
	         with Tikhonov regularization.

primal_sparse.jl - Implements Algorithm 2, i.e., the iterative MIO based algorithm for sparse convex regression 
	           problem with bounded subgradients.

Various function files:
functions.jl 
function_sparse_cuttingplane.jl
function_sparse_MIObigM.jl
function_sparse_MIObigM_LARGE.jl

Code for generating sparse data:
sparse_create_data.jl 
(Code for generating data for continuous problem is inluded in convex_reg.jl itself)

# Codes used in sections:
4.2, 4.3, 4,4: convex_reg.jl
4.5: admm_script.m, agcp.jl, solve_comparison_admm.jl, solve_comparison_agcp.jl
4.6: l1_convex_reg.jl
4.7: convex_reg.jl
4.8: sparse_create_data.jl, primal_sparse.jl, dual_sparse.jl

4). Details of files in Test_Instances:

a. sparse-dual.zip : Contains sparse instances used for testing the dual approach.

b. sparse-primal.zip: Contains sparse instances used for testing the primal approach.

