This code is a workflow for generating a calibration scheme for CLM-FATES.

The workflow has three stages

1. Generate parameter files to create an ensemble of runs:found in
 nocomp_parameter_modification_python/scripts_for_parameter_ensemble using the jupyter notebook *make_param_files_LHC_NOCOMP.ipynb* for the latin hypercube and *make_param_files_OAAT_NOCOMP.ipynb* for the one at a time.  

2. Create and run the ensemble. Using the scripts fround in *bash_scripts_ensemble/NOCOMP_FBG_LHC*
 (for the latin hypercube) or *bash_scripts_ensemble/NOCOMP_FBG_OAAT* for the one at a time.
   There are three main kinds of file. 'setup', clone_case and submot_ensemble. These need to be modified according to your needs. 

3. Analyse the output, create surrogate models, resample these, compare to observations and select target parameter sets accordingly. These all happen in the
*gaussian_emulator/NOCOMP_LHC_emulator.ipynb* jupyter notebook, 
5.  
