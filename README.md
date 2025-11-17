# Amigo Example Notebooks!

Welcome to the [Amigo](https://github.com/LouisDesdoigts/amigo) example notebooks repository! Here, you'll find a collection of Jupyter notebooks that demonstrate how to use Amigo for various tasks related to astronomical imaging and analysis. Amigo is designed to be very user-friendly, but also enables advanced users to customise and extend its functionality almost without limit. 

Note that you will need the calibration files in order to run these notebooks. You can find them in the [Amigo Calibration Repository](https://github.com/LouisDesdoigts/amigo_files). Please download the calibration files that correspond to your version of Amigo.

Here we provide a set of examples of recovering high-contrast companions to get you started. The workflow is broken down into a few different steps, each of which is covered in a separate notebook:

### User Workflow Notebooks

1. [Data Processing](https://github.com/LouisDesdoigts/amigo_notebooks/blob/main/data_processing.ipynb): Amigo predicts the raw uncalibrated data produced by JWST, so this notebook converts the raw `.uncal` files into the Amgio-compatible `.calslope` format. This is one cell long and should only require users to point to the correct files.
2. [Data Fitting](https://github.com/LouisDesdoigts/amigo_notebooks/blob/main/data_fitting.ipynb): This notebook is the core of the Amigo workflow, taking in the `.calslope` files and fitting interferometric visibilities to the data set. While it is relatively long, for the majority of users it should be sufficient to simply run the notebook as-is.
3. [Visibility Reduction](https://github.com/LouisDesdoigts/amigo_notebooks/blob/main/vis_reduction.ipynb): This notebook takes the raw visibilities that were recovered from some data set, calibrates them, and makes them insensitive to any remaining Wavefront and instrumental errors. In most cases, this notebook requires users to simply define which stars are the science targets and which are the calibrators.
4. [Visibility Analysis](https://github.com/LouisDesdoigts/amigo_notebooks/blob/main/vis_analysis.ipynb): This notebook is not strictly part of Amgio, which is designed to recover calibrated visibilities. However, it provides a simple example of how to use the calibrated visibilities to search for companions, and shows how to work with the unique data products that are produced by Amigo.

### Developer Notebooks

1. [Model Calibration]: (under development) This notebook is here simply for posterity, showing how the calibration process of Amigo is done, as well as how the validation of the models are done.
2. [Visibility Basis](https://github.com/LouisDesdoigts/amigo_notebooks/blob/main/vis_basis.ipynb): This notebook shows how Amigo's unique latent visibility basis is constructed. 
3. [Jacobian Caching](https://github.com/LouisDesdoigts/amigo_notebooks/blob/main/jac_caching.ipynb): This notebook pre-calculates and caches the Jacobian matrices that are used in the fitting process, enabling an auto-normalisation of the gradients for the optimiser.